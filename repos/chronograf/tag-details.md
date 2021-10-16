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
$ docker pull chronograf@sha256:34f145f70451cc95087011e0dbd66885de35f878e9df7bf3af39c484cd7e1221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:9b6e45461a6131f427dec3561927653a30acbe6351537c3e1705be8407c3a7f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2787aa994425d922e88d7df5d8cbaab33084fd24aec062ed91fb6a6075b24885`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:13:27 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 15:13:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:13:36 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:13:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:13:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66087bf7be5c579789511a21c106da28de5de4dab61cb75b514b4c737e403764`  
		Last Modified: Tue, 12 Oct 2021 15:15:17 GMT  
		Size: 20.0 MB (20045112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d39018c54114d2d1c74266bc1843a885fa863defaa88b75222c7ee282278598`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9c0274b2fa67c68a28d02c8ec15be12be755ad04061e31050cfb1086cdf45d`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80da8236c0c6d1017f54ab63d7807fa4419ddf39eb0bfd3e691a845465ed51`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2f7ab4550c5a33718fbc57ace9e323139261d26d24f7964438b807f6aa54aa21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43941727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b6928c30816e270273153010070663706e2fc23d2bbf28e0aeb515c6f9cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:38:55 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 19:39:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:39:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:39:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:39:15 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:39:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:39:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:39:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:39:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062e4eca0454a6b55d5ed50bff4c7deb791c7d22de226597152334d9bb073e`  
		Last Modified: Tue, 12 Oct 2021 19:42:41 GMT  
		Size: 18.8 MB (18820372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd9dd16d2c73dd4fd0238fdc97b81a2d79b2506c51c187351cd7ac5da3c5719`  
		Last Modified: Tue, 12 Oct 2021 19:42:33 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108f35c398f2e1184fc422610949e17eca7c582e770dd0afbdfa19fd1bca1a71`  
		Last Modified: Tue, 12 Oct 2021 19:42:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c80b9aa5ed4f16409267c0781b4830096e20ec938021f2d257d52ea25ae9e4`  
		Last Modified: Tue, 12 Oct 2021 19:42:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d053219bcb69b0b4189b842e38552c4b3d2cce62033c0d04a8052026107f7bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45421708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678fdefa9908af0e74277d9cc128e873cb7f875453cc3c8d805178ceb56331f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Fri, 15 Oct 2021 23:39:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:40:00 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 15 Oct 2021 23:40:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:40:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:40:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:40:11 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:40:12 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:40:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:40:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:40:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb2fb42b7dda7650316db4bf6a352d35897e7520ee69babe99504a3017934c5`  
		Last Modified: Fri, 15 Oct 2021 23:42:00 GMT  
		Size: 6.0 MB (6046748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2ee07be3f8b130f8504245a4e3a763790226755a6d5e703c19312307e4120`  
		Last Modified: Fri, 15 Oct 2021 23:42:02 GMT  
		Size: 19.0 MB (18961112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff8fabd86d11f08f5e9a2394c0bcd2951150b48da98d4a0a0e65498d294d425`  
		Last Modified: Fri, 15 Oct 2021 23:41:59 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba012a2c0c6d79446a2fe030f6e325e4b8b44a3a48c44585089a1f2937ef7b69`  
		Last Modified: Fri, 15 Oct 2021 23:41:59 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf702259c90f2ae855bc8fe5c6f0ac06d9f589f6628916cfde8ae42544f650a`  
		Last Modified: Fri, 15 Oct 2021 23:41:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:104b36e0e2cbf6dde2a8c2ad34c26fe743bc16d5448199bcb83f83f8e4ca9ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:901c492269dcbe051348d08f16cbea911cef31475bbe741919471747b5c982be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14857887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f46642356d29fb20e7de12cbf1be4aae7fc749df4f8a239b859f8542848d5d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 15 Oct 2021 23:19:31 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 15 Oct 2021 23:19:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 15 Oct 2021 23:19:44 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:19:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:19:45 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:19:45 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:19:45 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 15 Oct 2021 23:19:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:19:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc18a66a76502d3b3dbd80a017b1c3e8c3703fac2b474322ce8fbc1986ff041`  
		Last Modified: Fri, 15 Oct 2021 23:21:23 GMT  
		Size: 11.7 MB (11737380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bd5decdc8262528303f8f7e9ffe06813b7320310d263b03dbee79ac04b3957`  
		Last Modified: Fri, 15 Oct 2021 23:21:20 GMT  
		Size: 12.3 KB (12270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe807fb22d931a97c1c72282fba08e034968bfe1ce5f5752fa714a876022f78`  
		Last Modified: Fri, 15 Oct 2021 23:21:21 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441a29190d85b50796d11144437e789ab0af981c1ff5ca5cc76318c796fce10`  
		Last Modified: Fri, 15 Oct 2021 23:21:20 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:34f145f70451cc95087011e0dbd66885de35f878e9df7bf3af39c484cd7e1221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:9b6e45461a6131f427dec3561927653a30acbe6351537c3e1705be8407c3a7f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2787aa994425d922e88d7df5d8cbaab33084fd24aec062ed91fb6a6075b24885`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:13:27 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 15:13:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:13:36 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:13:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:13:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:13:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:13:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66087bf7be5c579789511a21c106da28de5de4dab61cb75b514b4c737e403764`  
		Last Modified: Tue, 12 Oct 2021 15:15:17 GMT  
		Size: 20.0 MB (20045112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d39018c54114d2d1c74266bc1843a885fa863defaa88b75222c7ee282278598`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9c0274b2fa67c68a28d02c8ec15be12be755ad04061e31050cfb1086cdf45d`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80da8236c0c6d1017f54ab63d7807fa4419ddf39eb0bfd3e691a845465ed51`  
		Last Modified: Tue, 12 Oct 2021 15:15:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2f7ab4550c5a33718fbc57ace9e323139261d26d24f7964438b807f6aa54aa21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43941727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3b6928c30816e270273153010070663706e2fc23d2bbf28e0aeb515c6f9cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:38:55 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 19:39:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:39:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:39:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:39:15 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:39:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:39:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:39:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:39:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90062e4eca0454a6b55d5ed50bff4c7deb791c7d22de226597152334d9bb073e`  
		Last Modified: Tue, 12 Oct 2021 19:42:41 GMT  
		Size: 18.8 MB (18820372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd9dd16d2c73dd4fd0238fdc97b81a2d79b2506c51c187351cd7ac5da3c5719`  
		Last Modified: Tue, 12 Oct 2021 19:42:33 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108f35c398f2e1184fc422610949e17eca7c582e770dd0afbdfa19fd1bca1a71`  
		Last Modified: Tue, 12 Oct 2021 19:42:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c80b9aa5ed4f16409267c0781b4830096e20ec938021f2d257d52ea25ae9e4`  
		Last Modified: Tue, 12 Oct 2021 19:42:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d053219bcb69b0b4189b842e38552c4b3d2cce62033c0d04a8052026107f7bd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45421708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678fdefa9908af0e74277d9cc128e873cb7f875453cc3c8d805178ceb56331f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Fri, 15 Oct 2021 23:39:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:40:00 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 15 Oct 2021 23:40:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:40:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:40:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:40:11 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:40:12 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:40:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:40:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:40:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb2fb42b7dda7650316db4bf6a352d35897e7520ee69babe99504a3017934c5`  
		Last Modified: Fri, 15 Oct 2021 23:42:00 GMT  
		Size: 6.0 MB (6046748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d2ee07be3f8b130f8504245a4e3a763790226755a6d5e703c19312307e4120`  
		Last Modified: Fri, 15 Oct 2021 23:42:02 GMT  
		Size: 19.0 MB (18961112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff8fabd86d11f08f5e9a2394c0bcd2951150b48da98d4a0a0e65498d294d425`  
		Last Modified: Fri, 15 Oct 2021 23:41:59 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba012a2c0c6d79446a2fe030f6e325e4b8b44a3a48c44585089a1f2937ef7b69`  
		Last Modified: Fri, 15 Oct 2021 23:41:59 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf702259c90f2ae855bc8fe5c6f0ac06d9f589f6628916cfde8ae42544f650a`  
		Last Modified: Fri, 15 Oct 2021 23:41:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:104b36e0e2cbf6dde2a8c2ad34c26fe743bc16d5448199bcb83f83f8e4ca9ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:901c492269dcbe051348d08f16cbea911cef31475bbe741919471747b5c982be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14857887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f46642356d29fb20e7de12cbf1be4aae7fc749df4f8a239b859f8542848d5d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 15 Oct 2021 23:19:31 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 15 Oct 2021 23:19:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 15 Oct 2021 23:19:44 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:19:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:19:45 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:19:45 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:19:45 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 15 Oct 2021 23:19:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:19:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc18a66a76502d3b3dbd80a017b1c3e8c3703fac2b474322ce8fbc1986ff041`  
		Last Modified: Fri, 15 Oct 2021 23:21:23 GMT  
		Size: 11.7 MB (11737380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bd5decdc8262528303f8f7e9ffe06813b7320310d263b03dbee79ac04b3957`  
		Last Modified: Fri, 15 Oct 2021 23:21:20 GMT  
		Size: 12.3 KB (12270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe807fb22d931a97c1c72282fba08e034968bfe1ce5f5752fa714a876022f78`  
		Last Modified: Fri, 15 Oct 2021 23:21:21 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441a29190d85b50796d11144437e789ab0af981c1ff5ca5cc76318c796fce10`  
		Last Modified: Fri, 15 Oct 2021 23:21:20 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:71ceeae235bb0989c31e734e21302b758173ed24b507fe7ffa227d42e7484eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:2bd89c8e3321704209756d371908d7d67c8ff11a44742ebda71bbb55f59b2f0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65386514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4cc46bc95e6eb6fff4e2ef999885e2a7877ae4c81faaccf2b55b85c643da3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:14:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 15:14:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:12 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff71fee6d1c6f643c4ff577353f7241f074a2e1172c48bc55d6069c83fda780`  
		Last Modified: Tue, 12 Oct 2021 15:15:28 GMT  
		Size: 4.5 MB (4506496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc48f5a7983e6c90de97e53279aefdbcb8f04b16c695b8b3c0c8d11006a03c36`  
		Last Modified: Tue, 12 Oct 2021 15:15:33 GMT  
		Size: 38.3 MB (38328059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631c77fffd0c1adcabc4c422f0b54c61947831f4a30ef756ab4cd8e1cc32e092`  
		Last Modified: Tue, 12 Oct 2021 15:15:27 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b08426d08ca99f1b410b47ea2acae8115f8f14ce88a2e0e8c944d9a45e5251a`  
		Last Modified: Tue, 12 Oct 2021 15:15:28 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad5dc2c1b79f0561fd3a3850dbedf5b3aadc0f829a1e252d3a62117c28b7958`  
		Last Modified: Tue, 12 Oct 2021 15:15:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:24c953f15124e44d5f380ab57393ba63f756b3ae00178b8c9a80b57e60da7d0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59004035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0990e576b5aa23f88bb3470e9f41d66329abb0ea617ce2265caf4fe0a962b36e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:39:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:39:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 19:40:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:40:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:40:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:40:24 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:40:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:40:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:40:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:40:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba93e163db4e24fdc0b61e5985bc4b17555fa24b26c0fe4f12f9128c2f84eaf0`  
		Last Modified: Tue, 12 Oct 2021 19:42:54 GMT  
		Size: 3.9 MB (3879899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5062c1f70209ac4f7642c34d34e5595e27b46dd3c3613e650f066bbfc95e12`  
		Last Modified: Tue, 12 Oct 2021 19:43:10 GMT  
		Size: 35.8 MB (35783266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fb47a33ac1e78d667ef6f96865c0f0ff850f8ba7ff43cea2ed8402d499fdc6`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ef10a515dcd0452d9b9afd8d115f464770476846c5a040fe3bd2e6dd7b45e`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefacd9f6d476b458a8a581c78ccacd7d528d4615b8f9d031c4ab3032f416438`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:85d9adf8def7878662c1f7d5daf42e95285e002e5fb59f06542d9b114839cec1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb65837fa9fb512ec3e483d74be1808fe83da88fa3aad2dfd15ce3697fe2091e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Fri, 15 Oct 2021 23:40:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:40:36 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Oct 2021 23:40:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:40:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:40:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:40:50 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:40:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:40:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:40:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:40:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1753f7d911f7c12d2f6f87198a1b7bb67cfa5b14b09bcdbbf4e579c625bd4cd`  
		Last Modified: Fri, 15 Oct 2021 23:42:12 GMT  
		Size: 3.9 MB (3893772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c7d9e61ab7e54f02dd0edf0facc03b597e3baa98e13ee79a9ebe7cb05d86b2`  
		Last Modified: Fri, 15 Oct 2021 23:42:18 GMT  
		Size: 36.0 MB (35986604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e3b7c8f8a26b8cef12083b4b4df3bc544200352d6f9e2d1999b79b9b62d5a4`  
		Last Modified: Fri, 15 Oct 2021 23:42:12 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadb2575b900bfede49df8e3299612665df2ec0f7ae8b8fad74ff5cf41b57bba`  
		Last Modified: Fri, 15 Oct 2021 23:42:12 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f14e0ac90d74259cf5ff732b1e5212db9b050d693c2cbb03c86918488bf3071`  
		Last Modified: Fri, 15 Oct 2021 23:42:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:052ec9ed73c22a5133e8dd18c6dd9c149b00cb2ca053b1c87dfc49bf33f772b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:61814e65a9d409e7796f6c8472a4902cb11ac1dcc5b672f2c2395880ed55ce0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22676454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2308e2915f4050377ece443295d417273bcca66fae08163470349385a00cc386`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 15 Oct 2021 23:19:52 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Oct 2021 23:20:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 15 Oct 2021 23:20:04 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:04 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:04 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:04 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:05 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de7162e4de1902915c167b5c94fbd464257573490603ff01688397c40e34e63`  
		Last Modified: Fri, 15 Oct 2021 23:21:37 GMT  
		Size: 19.6 MB (19555959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e2f4d107a90a814f2afa77369947f25c30a1a736f7eddceda093a189c5a717`  
		Last Modified: Fri, 15 Oct 2021 23:21:34 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b6ef4336ad7466b9b0334e12c4b37da188fe7d46b149c3681ef40d45bd22e9`  
		Last Modified: Fri, 15 Oct 2021 23:21:34 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17694fd4e2f2ef396839d6b9b94e46961fea0188ae8ea6b53222337fc1e6dc3f`  
		Last Modified: Fri, 15 Oct 2021 23:21:34 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:71ceeae235bb0989c31e734e21302b758173ed24b507fe7ffa227d42e7484eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:2bd89c8e3321704209756d371908d7d67c8ff11a44742ebda71bbb55f59b2f0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65386514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4cc46bc95e6eb6fff4e2ef999885e2a7877ae4c81faaccf2b55b85c643da3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:14:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 15:14:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:12 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff71fee6d1c6f643c4ff577353f7241f074a2e1172c48bc55d6069c83fda780`  
		Last Modified: Tue, 12 Oct 2021 15:15:28 GMT  
		Size: 4.5 MB (4506496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc48f5a7983e6c90de97e53279aefdbcb8f04b16c695b8b3c0c8d11006a03c36`  
		Last Modified: Tue, 12 Oct 2021 15:15:33 GMT  
		Size: 38.3 MB (38328059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631c77fffd0c1adcabc4c422f0b54c61947831f4a30ef756ab4cd8e1cc32e092`  
		Last Modified: Tue, 12 Oct 2021 15:15:27 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b08426d08ca99f1b410b47ea2acae8115f8f14ce88a2e0e8c944d9a45e5251a`  
		Last Modified: Tue, 12 Oct 2021 15:15:28 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad5dc2c1b79f0561fd3a3850dbedf5b3aadc0f829a1e252d3a62117c28b7958`  
		Last Modified: Tue, 12 Oct 2021 15:15:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:24c953f15124e44d5f380ab57393ba63f756b3ae00178b8c9a80b57e60da7d0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59004035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0990e576b5aa23f88bb3470e9f41d66329abb0ea617ce2265caf4fe0a962b36e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:39:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:39:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 19:40:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:40:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:40:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:40:24 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:40:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:40:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:40:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:40:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba93e163db4e24fdc0b61e5985bc4b17555fa24b26c0fe4f12f9128c2f84eaf0`  
		Last Modified: Tue, 12 Oct 2021 19:42:54 GMT  
		Size: 3.9 MB (3879899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5062c1f70209ac4f7642c34d34e5595e27b46dd3c3613e650f066bbfc95e12`  
		Last Modified: Tue, 12 Oct 2021 19:43:10 GMT  
		Size: 35.8 MB (35783266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fb47a33ac1e78d667ef6f96865c0f0ff850f8ba7ff43cea2ed8402d499fdc6`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843ef10a515dcd0452d9b9afd8d115f464770476846c5a040fe3bd2e6dd7b45e`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefacd9f6d476b458a8a581c78ccacd7d528d4615b8f9d031c4ab3032f416438`  
		Last Modified: Tue, 12 Oct 2021 19:42:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:85d9adf8def7878662c1f7d5daf42e95285e002e5fb59f06542d9b114839cec1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb65837fa9fb512ec3e483d74be1808fe83da88fa3aad2dfd15ce3697fe2091e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Fri, 15 Oct 2021 23:40:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:40:36 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Oct 2021 23:40:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:40:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:40:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:40:50 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:40:51 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:40:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:40:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:40:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1753f7d911f7c12d2f6f87198a1b7bb67cfa5b14b09bcdbbf4e579c625bd4cd`  
		Last Modified: Fri, 15 Oct 2021 23:42:12 GMT  
		Size: 3.9 MB (3893772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c7d9e61ab7e54f02dd0edf0facc03b597e3baa98e13ee79a9ebe7cb05d86b2`  
		Last Modified: Fri, 15 Oct 2021 23:42:18 GMT  
		Size: 36.0 MB (35986604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e3b7c8f8a26b8cef12083b4b4df3bc544200352d6f9e2d1999b79b9b62d5a4`  
		Last Modified: Fri, 15 Oct 2021 23:42:12 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadb2575b900bfede49df8e3299612665df2ec0f7ae8b8fad74ff5cf41b57bba`  
		Last Modified: Fri, 15 Oct 2021 23:42:12 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f14e0ac90d74259cf5ff732b1e5212db9b050d693c2cbb03c86918488bf3071`  
		Last Modified: Fri, 15 Oct 2021 23:42:12 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:052ec9ed73c22a5133e8dd18c6dd9c149b00cb2ca053b1c87dfc49bf33f772b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:61814e65a9d409e7796f6c8472a4902cb11ac1dcc5b672f2c2395880ed55ce0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22676454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2308e2915f4050377ece443295d417273bcca66fae08163470349385a00cc386`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 15 Oct 2021 23:19:52 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Oct 2021 23:20:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 15 Oct 2021 23:20:04 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:04 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:04 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:04 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:05 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de7162e4de1902915c167b5c94fbd464257573490603ff01688397c40e34e63`  
		Last Modified: Fri, 15 Oct 2021 23:21:37 GMT  
		Size: 19.6 MB (19555959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e2f4d107a90a814f2afa77369947f25c30a1a736f7eddceda093a189c5a717`  
		Last Modified: Fri, 15 Oct 2021 23:21:34 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b6ef4336ad7466b9b0334e12c4b37da188fe7d46b149c3681ef40d45bd22e9`  
		Last Modified: Fri, 15 Oct 2021 23:21:34 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17694fd4e2f2ef396839d6b9b94e46961fea0188ae8ea6b53222337fc1e6dc3f`  
		Last Modified: Fri, 15 Oct 2021 23:21:34 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:5b8b1f515fc44b859369ed01f575412f03039b211422828b3808bf49dba24b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:28d78f7ebfd70cabe87f092c5711214b6430d593fa97ae0d07b4ca085eac0089
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e668a013e2d920330790522771b175609cbad9cb9e1fd69f02238c5b84c54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:21 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 15:14:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:30 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8953df3cc8defa8f66bec30576de86c6eae2d8b1adcf5d303730f4032ade0047`  
		Last Modified: Tue, 12 Oct 2021 15:15:49 GMT  
		Size: 36.9 MB (36925919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22d923a6658e9d6073c1138d027503b4bd19690c1929beaa6edb6dbec4d32a`  
		Last Modified: Tue, 12 Oct 2021 15:15:43 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97056842c271762da86131f848a0cf5e2e501646a00a81b72d101895d6017ff2`  
		Last Modified: Tue, 12 Oct 2021 15:15:43 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79854fc9d1645faa1753c703bf21bf54fa0c6452b3e31fdf34058a37503372b3`  
		Last Modified: Tue, 12 Oct 2021 15:15:44 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e605529e9949cebced87e772262e32d25cc7174b90fa331199d39d3e6d1bfdf1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59632513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9547985998cd5c863f3d75b3a9bf95979fd0aef9eafbe631993a0149d453825`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:40:42 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 19:41:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:41:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:41:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:41:02 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:41:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:41:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:41:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:41:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abebde07ee5067581f728ce1049bfb321ae8aa8a50c6badf7c2d260eb793285`  
		Last Modified: Tue, 12 Oct 2021 19:43:40 GMT  
		Size: 34.5 MB (34511153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b85ed73208be7b2083812316441639b1345bfaf23d14c53d5f48e62d237bc6a`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f255471ddc5f6979184f7e99a330c28cefb293a081ce7cdfeba51540dcd893e`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf7931f243ffa449d28bb79868493276ea0e146b34e6e33d4d50bc5241da366`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:4caac1619b98cecde24d418ec32c5c39f5cca36f5a4e0b7dde464f2a97005242
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60891834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2be38cbabc41b2e6267c17f91a256b97e5710c55afc30587d81299a1a5a346b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Fri, 15 Oct 2021 23:39:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:40:59 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Oct 2021 23:41:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:41:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:41:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:41:10 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:41:11 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:41:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:41:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:41:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb2fb42b7dda7650316db4bf6a352d35897e7520ee69babe99504a3017934c5`  
		Last Modified: Fri, 15 Oct 2021 23:42:00 GMT  
		Size: 6.0 MB (6046748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a69ccd2c1141a43aae9d16273140b168885a0df9d6062e3d7f19ba859cb274`  
		Last Modified: Fri, 15 Oct 2021 23:42:34 GMT  
		Size: 34.4 MB (34431242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea94d4d1b1c4a8c399de456d256d5817dc57055d82f1bb03178c25d41fc51829`  
		Last Modified: Fri, 15 Oct 2021 23:42:29 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60134bb09078d3967a1291e22c18ce72374172a21e58543b1a23208a6b9bdcf`  
		Last Modified: Fri, 15 Oct 2021 23:42:29 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4aec6efe079a96e7d7b0dde2482d0853494b6c7944cc0b6d57a13487423042`  
		Last Modified: Fri, 15 Oct 2021 23:42:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:eac18e11806ecf057e0606df2fe27f722ba1fac45ead1b8da351561b83fef346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:52f79440ab713788e0aad4790da0f1325362abe28028c66518c4c70cda43c1cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22324214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57a1ca3ec2949f6f7df051f4744e959030f2cd0b937900618ff331b5a90488f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 15 Oct 2021 23:20:10 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Oct 2021 23:20:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 15 Oct 2021 23:20:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:23 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:24 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7140b56cdab53c0b40bb65e9b32334356ac7a87fb113aeb629a615daf77ce4b9`  
		Last Modified: Fri, 15 Oct 2021 23:21:51 GMT  
		Size: 19.2 MB (19203714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6f48915476e3cd542cce993d4959ec7b4b0fc356575472fb1913ef91f13b01`  
		Last Modified: Fri, 15 Oct 2021 23:21:48 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ff0536ba42965323742366f0ac67aca755ac02b2461b042b71986b60fb03a4`  
		Last Modified: Fri, 15 Oct 2021 23:21:48 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56093eb1399dc32fcc9bf5f807bfdee2377d47338d1e06e7210310a9853bf72`  
		Last Modified: Fri, 15 Oct 2021 23:21:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:5b8b1f515fc44b859369ed01f575412f03039b211422828b3808bf49dba24b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:28d78f7ebfd70cabe87f092c5711214b6430d593fa97ae0d07b4ca085eac0089
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e668a013e2d920330790522771b175609cbad9cb9e1fd69f02238c5b84c54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:21 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 15:14:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:30 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:30 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:30 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8953df3cc8defa8f66bec30576de86c6eae2d8b1adcf5d303730f4032ade0047`  
		Last Modified: Tue, 12 Oct 2021 15:15:49 GMT  
		Size: 36.9 MB (36925919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22d923a6658e9d6073c1138d027503b4bd19690c1929beaa6edb6dbec4d32a`  
		Last Modified: Tue, 12 Oct 2021 15:15:43 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97056842c271762da86131f848a0cf5e2e501646a00a81b72d101895d6017ff2`  
		Last Modified: Tue, 12 Oct 2021 15:15:43 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79854fc9d1645faa1753c703bf21bf54fa0c6452b3e31fdf34058a37503372b3`  
		Last Modified: Tue, 12 Oct 2021 15:15:44 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e605529e9949cebced87e772262e32d25cc7174b90fa331199d39d3e6d1bfdf1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59632513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9547985998cd5c863f3d75b3a9bf95979fd0aef9eafbe631993a0149d453825`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 19:40:42 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 19:41:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 19:41:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 19:41:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 19:41:02 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 19:41:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 19:41:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 19:41:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 19:41:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abebde07ee5067581f728ce1049bfb321ae8aa8a50c6badf7c2d260eb793285`  
		Last Modified: Tue, 12 Oct 2021 19:43:40 GMT  
		Size: 34.5 MB (34511153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b85ed73208be7b2083812316441639b1345bfaf23d14c53d5f48e62d237bc6a`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f255471ddc5f6979184f7e99a330c28cefb293a081ce7cdfeba51540dcd893e`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf7931f243ffa449d28bb79868493276ea0e146b34e6e33d4d50bc5241da366`  
		Last Modified: Tue, 12 Oct 2021 19:43:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:4caac1619b98cecde24d418ec32c5c39f5cca36f5a4e0b7dde464f2a97005242
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60891834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2be38cbabc41b2e6267c17f91a256b97e5710c55afc30587d81299a1a5a346b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Fri, 15 Oct 2021 23:39:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:40:59 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Oct 2021 23:41:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:41:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:41:10 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:41:10 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:41:11 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:41:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:41:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:41:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb2fb42b7dda7650316db4bf6a352d35897e7520ee69babe99504a3017934c5`  
		Last Modified: Fri, 15 Oct 2021 23:42:00 GMT  
		Size: 6.0 MB (6046748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a69ccd2c1141a43aae9d16273140b168885a0df9d6062e3d7f19ba859cb274`  
		Last Modified: Fri, 15 Oct 2021 23:42:34 GMT  
		Size: 34.4 MB (34431242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea94d4d1b1c4a8c399de456d256d5817dc57055d82f1bb03178c25d41fc51829`  
		Last Modified: Fri, 15 Oct 2021 23:42:29 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60134bb09078d3967a1291e22c18ce72374172a21e58543b1a23208a6b9bdcf`  
		Last Modified: Fri, 15 Oct 2021 23:42:29 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4aec6efe079a96e7d7b0dde2482d0853494b6c7944cc0b6d57a13487423042`  
		Last Modified: Fri, 15 Oct 2021 23:42:29 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:eac18e11806ecf057e0606df2fe27f722ba1fac45ead1b8da351561b83fef346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:52f79440ab713788e0aad4790da0f1325362abe28028c66518c4c70cda43c1cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22324214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57a1ca3ec2949f6f7df051f4744e959030f2cd0b937900618ff331b5a90488f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 15 Oct 2021 23:20:10 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Oct 2021 23:20:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 15 Oct 2021 23:20:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:23 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:24 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7140b56cdab53c0b40bb65e9b32334356ac7a87fb113aeb629a615daf77ce4b9`  
		Last Modified: Fri, 15 Oct 2021 23:21:51 GMT  
		Size: 19.2 MB (19203714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6f48915476e3cd542cce993d4959ec7b4b0fc356575472fb1913ef91f13b01`  
		Last Modified: Fri, 15 Oct 2021 23:21:48 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ff0536ba42965323742366f0ac67aca755ac02b2461b042b71986b60fb03a4`  
		Last Modified: Fri, 15 Oct 2021 23:21:48 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56093eb1399dc32fcc9bf5f807bfdee2377d47338d1e06e7210310a9853bf72`  
		Last Modified: Fri, 15 Oct 2021 23:21:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:17d519622282734b62a18f658fc3e21be5135a10a4a058e881b2c82883969aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:a3feb36e84015278971594338ac6458ca0381625e5596f192b490a6abde48138
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66880161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed16b33ccc60bc2c329bc15b720a64c8ad6fa0223df860923c821d5ecc7ab59e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:20:27 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 23:20:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:20:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:37 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:37 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d98bf61fb358e014064d2fa4ec0aa8d382188df6feb209ba77fe4d1e6c03938`  
		Last Modified: Fri, 15 Oct 2021 23:22:06 GMT  
		Size: 37.6 MB (37567991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8e8d54ec064a127bbaf70ae6ba002b81b173670e881c2f7b41dad92e475240`  
		Last Modified: Fri, 15 Oct 2021 23:22:01 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c166081eb2c445e41c35f4020401f51ab14f6d73a11acfd3d581f3a5538b5a1`  
		Last Modified: Fri, 15 Oct 2021 23:22:01 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dd00009bd2f62125ed1c65af31ef89e76b1d981ba87b41ee5d910a09975d2`  
		Last Modified: Fri, 15 Oct 2021 23:22:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3fb18999dd46d064947de88c86f049f7ce677b11db15a4d4cf87c15b8b0d1321
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60400450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa55eda148d3b9748e46d3bc19063b771b86359c6f629fe806c3e5afb1bb58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 22:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 22:58:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 22:58:35 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 22:58:35 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 22:58:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 22:58:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 22:58:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb66a9a95b28e3a240c450633d5421211135b4312de046bce206afbb0f30edf9`  
		Last Modified: Fri, 15 Oct 2021 22:59:56 GMT  
		Size: 35.3 MB (35279095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec2c2711c3377ce218bad44c96856e245d745faa65f1687a85c49b1f8a56538`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e65825543156a066468a039c1e306c2c2db19fc435de2dcd52973ad8a56f97d`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8291978c4564a4ffcbd216ab5bc6155061ae9c2b94b78ea4b685708808d67891`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:3bf66aa371a463bf3755718761d7c4c2584c04f3397539ff038f2dc9d619506c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61623284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02056a288c12c80e4361860062646ffc0d7cb946e3db2f673f88f408fe9c0fbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Fri, 15 Oct 2021 23:39:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:41:19 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 23:41:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:41:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:41:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:41:30 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:41:31 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:41:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:41:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:41:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb2fb42b7dda7650316db4bf6a352d35897e7520ee69babe99504a3017934c5`  
		Last Modified: Fri, 15 Oct 2021 23:42:00 GMT  
		Size: 6.0 MB (6046748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5fceb18faed77a0ad8ba0aefd92945a7a956ba63fd53c5ecb02120d200f3ee`  
		Last Modified: Fri, 15 Oct 2021 23:42:49 GMT  
		Size: 35.2 MB (35162696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78ce95fda35ee2d27a666b7b98f9794ce1cfb6b6247ea3e9f1a66e81aaf524`  
		Last Modified: Fri, 15 Oct 2021 23:42:44 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d76d8a0e394a23628d990878a20a7ecd15075fd8672ba117c62ce9e2c5e19e`  
		Last Modified: Fri, 15 Oct 2021 23:42:44 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e60834fe1ab1f1135de6cfe04e065dd03b639e91f03846cf857bc584697cf7`  
		Last Modified: Fri, 15 Oct 2021 23:42:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:63d7879b58cca75f5961dc69f60f665618d889a1e2e54c722527d58ae8cc9baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:56918ca02f9aafdef034d5ebb4d4d27d172d2fe407b7085877a0fcd980d6a087
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22781488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92876e8600b72256911a0e2bb66260442484e928f6552e9f486114127fb9a83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 15 Oct 2021 23:20:40 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 23:20:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 15 Oct 2021 23:20:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:55 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:55 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1855f6b30493f4425878a9c2578728ef59be0f47e5ebd3b2ee5705ef8487ff6d`  
		Last Modified: Fri, 15 Oct 2021 23:22:22 GMT  
		Size: 19.7 MB (19660985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7869e8e2f8fdc6a74f446d5fa09127eb6ba48b8defa7e5c2ee0b83b3887e9582`  
		Last Modified: Fri, 15 Oct 2021 23:22:19 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa06ec7f410f79822928222337c67928b3f9fa0b9072d72c0789b3e2ce1e4b8`  
		Last Modified: Fri, 15 Oct 2021 23:22:19 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ef6c14488be545954546e2fb33b487457876021d12904a913f1875671ae625`  
		Last Modified: Fri, 15 Oct 2021 23:22:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.1`

```console
$ docker pull chronograf@sha256:17d519622282734b62a18f658fc3e21be5135a10a4a058e881b2c82883969aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.1` - linux; amd64

```console
$ docker pull chronograf@sha256:a3feb36e84015278971594338ac6458ca0381625e5596f192b490a6abde48138
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66880161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed16b33ccc60bc2c329bc15b720a64c8ad6fa0223df860923c821d5ecc7ab59e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:20:27 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 23:20:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:20:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:37 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:37 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d98bf61fb358e014064d2fa4ec0aa8d382188df6feb209ba77fe4d1e6c03938`  
		Last Modified: Fri, 15 Oct 2021 23:22:06 GMT  
		Size: 37.6 MB (37567991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8e8d54ec064a127bbaf70ae6ba002b81b173670e881c2f7b41dad92e475240`  
		Last Modified: Fri, 15 Oct 2021 23:22:01 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c166081eb2c445e41c35f4020401f51ab14f6d73a11acfd3d581f3a5538b5a1`  
		Last Modified: Fri, 15 Oct 2021 23:22:01 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dd00009bd2f62125ed1c65af31ef89e76b1d981ba87b41ee5d910a09975d2`  
		Last Modified: Fri, 15 Oct 2021 23:22:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.1` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3fb18999dd46d064947de88c86f049f7ce677b11db15a4d4cf87c15b8b0d1321
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60400450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa55eda148d3b9748e46d3bc19063b771b86359c6f629fe806c3e5afb1bb58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 22:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 22:58:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 22:58:35 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 22:58:35 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 22:58:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 22:58:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 22:58:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb66a9a95b28e3a240c450633d5421211135b4312de046bce206afbb0f30edf9`  
		Last Modified: Fri, 15 Oct 2021 22:59:56 GMT  
		Size: 35.3 MB (35279095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec2c2711c3377ce218bad44c96856e245d745faa65f1687a85c49b1f8a56538`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e65825543156a066468a039c1e306c2c2db19fc435de2dcd52973ad8a56f97d`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8291978c4564a4ffcbd216ab5bc6155061ae9c2b94b78ea4b685708808d67891`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.1` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:3bf66aa371a463bf3755718761d7c4c2584c04f3397539ff038f2dc9d619506c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61623284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02056a288c12c80e4361860062646ffc0d7cb946e3db2f673f88f408fe9c0fbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Fri, 15 Oct 2021 23:39:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:41:19 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 23:41:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:41:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:41:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:41:30 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:41:31 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:41:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:41:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:41:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb2fb42b7dda7650316db4bf6a352d35897e7520ee69babe99504a3017934c5`  
		Last Modified: Fri, 15 Oct 2021 23:42:00 GMT  
		Size: 6.0 MB (6046748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5fceb18faed77a0ad8ba0aefd92945a7a956ba63fd53c5ecb02120d200f3ee`  
		Last Modified: Fri, 15 Oct 2021 23:42:49 GMT  
		Size: 35.2 MB (35162696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78ce95fda35ee2d27a666b7b98f9794ce1cfb6b6247ea3e9f1a66e81aaf524`  
		Last Modified: Fri, 15 Oct 2021 23:42:44 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d76d8a0e394a23628d990878a20a7ecd15075fd8672ba117c62ce9e2c5e19e`  
		Last Modified: Fri, 15 Oct 2021 23:42:44 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e60834fe1ab1f1135de6cfe04e065dd03b639e91f03846cf857bc584697cf7`  
		Last Modified: Fri, 15 Oct 2021 23:42:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.1-alpine`

```console
$ docker pull chronograf@sha256:63d7879b58cca75f5961dc69f60f665618d889a1e2e54c722527d58ae8cc9baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.1-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:56918ca02f9aafdef034d5ebb4d4d27d172d2fe407b7085877a0fcd980d6a087
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22781488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92876e8600b72256911a0e2bb66260442484e928f6552e9f486114127fb9a83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 15 Oct 2021 23:20:40 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 23:20:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 15 Oct 2021 23:20:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:55 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:55 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1855f6b30493f4425878a9c2578728ef59be0f47e5ebd3b2ee5705ef8487ff6d`  
		Last Modified: Fri, 15 Oct 2021 23:22:22 GMT  
		Size: 19.7 MB (19660985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7869e8e2f8fdc6a74f446d5fa09127eb6ba48b8defa7e5c2ee0b83b3887e9582`  
		Last Modified: Fri, 15 Oct 2021 23:22:19 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa06ec7f410f79822928222337c67928b3f9fa0b9072d72c0789b3e2ce1e4b8`  
		Last Modified: Fri, 15 Oct 2021 23:22:19 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ef6c14488be545954546e2fb33b487457876021d12904a913f1875671ae625`  
		Last Modified: Fri, 15 Oct 2021 23:22:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:63d7879b58cca75f5961dc69f60f665618d889a1e2e54c722527d58ae8cc9baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:56918ca02f9aafdef034d5ebb4d4d27d172d2fe407b7085877a0fcd980d6a087
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22781488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92876e8600b72256911a0e2bb66260442484e928f6552e9f486114127fb9a83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 15 Oct 2021 23:20:40 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 23:20:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 15 Oct 2021 23:20:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:55 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:55 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:55 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:56 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1855f6b30493f4425878a9c2578728ef59be0f47e5ebd3b2ee5705ef8487ff6d`  
		Last Modified: Fri, 15 Oct 2021 23:22:22 GMT  
		Size: 19.7 MB (19660985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7869e8e2f8fdc6a74f446d5fa09127eb6ba48b8defa7e5c2ee0b83b3887e9582`  
		Last Modified: Fri, 15 Oct 2021 23:22:19 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa06ec7f410f79822928222337c67928b3f9fa0b9072d72c0789b3e2ce1e4b8`  
		Last Modified: Fri, 15 Oct 2021 23:22:19 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ef6c14488be545954546e2fb33b487457876021d12904a913f1875671ae625`  
		Last Modified: Fri, 15 Oct 2021 23:22:19 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:17d519622282734b62a18f658fc3e21be5135a10a4a058e881b2c82883969aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:a3feb36e84015278971594338ac6458ca0381625e5596f192b490a6abde48138
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66880161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed16b33ccc60bc2c329bc15b720a64c8ad6fa0223df860923c821d5ecc7ab59e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:20:27 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 23:20:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:20:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:20:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:20:37 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:20:37 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:20:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:20:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:20:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d98bf61fb358e014064d2fa4ec0aa8d382188df6feb209ba77fe4d1e6c03938`  
		Last Modified: Fri, 15 Oct 2021 23:22:06 GMT  
		Size: 37.6 MB (37567991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8e8d54ec064a127bbaf70ae6ba002b81b173670e881c2f7b41dad92e475240`  
		Last Modified: Fri, 15 Oct 2021 23:22:01 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c166081eb2c445e41c35f4020401f51ab14f6d73a11acfd3d581f3a5538b5a1`  
		Last Modified: Fri, 15 Oct 2021 23:22:01 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dd00009bd2f62125ed1c65af31ef89e76b1d981ba87b41ee5d910a09975d2`  
		Last Modified: Fri, 15 Oct 2021 23:22:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3fb18999dd46d064947de88c86f049f7ce677b11db15a4d4cf87c15b8b0d1321
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60400450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa55eda148d3b9748e46d3bc19063b771b86359c6f629fe806c3e5afb1bb58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:34:42 GMT
ADD file:9bfcfd0aaac802b902b0e842e040a6599c461c90b73579bcacc2fbdda7ec39cb in / 
# Tue, 12 Oct 2021 01:34:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 19:38:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 22:58:13 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 22:58:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 22:58:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 22:58:35 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 22:58:35 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 22:58:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 22:58:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 22:58:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:a1a3620b17011bd36d6f64dfcc8fd7c4cb3da78d19a59efb1b35afcadaf3f6a8`  
		Last Modified: Tue, 12 Oct 2021 01:51:59 GMT  
		Size: 19.3 MB (19316474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc2f2b4d96b348e56cf5179e6a1d2f89538251124d2659dcb521c5c19e51bb`  
		Last Modified: Tue, 12 Oct 2021 19:42:36 GMT  
		Size: 5.8 MB (5780488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb66a9a95b28e3a240c450633d5421211135b4312de046bce206afbb0f30edf9`  
		Last Modified: Fri, 15 Oct 2021 22:59:56 GMT  
		Size: 35.3 MB (35279095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec2c2711c3377ce218bad44c96856e245d745faa65f1687a85c49b1f8a56538`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e65825543156a066468a039c1e306c2c2db19fc435de2dcd52973ad8a56f97d`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8291978c4564a4ffcbd216ab5bc6155061ae9c2b94b78ea4b685708808d67891`  
		Last Modified: Fri, 15 Oct 2021 22:59:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:3bf66aa371a463bf3755718761d7c4c2584c04f3397539ff038f2dc9d619506c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61623284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02056a288c12c80e4361860062646ffc0d7cb946e3db2f673f88f408fe9c0fbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Fri, 15 Oct 2021 23:39:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 15 Oct 2021 23:41:19 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 15 Oct 2021 23:41:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 15 Oct 2021 23:41:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 15 Oct 2021 23:41:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 15 Oct 2021 23:41:30 GMT
EXPOSE 8888
# Fri, 15 Oct 2021 23:41:31 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Oct 2021 23:41:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 15 Oct 2021 23:41:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Oct 2021 23:41:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb2fb42b7dda7650316db4bf6a352d35897e7520ee69babe99504a3017934c5`  
		Last Modified: Fri, 15 Oct 2021 23:42:00 GMT  
		Size: 6.0 MB (6046748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5fceb18faed77a0ad8ba0aefd92945a7a956ba63fd53c5ecb02120d200f3ee`  
		Last Modified: Fri, 15 Oct 2021 23:42:49 GMT  
		Size: 35.2 MB (35162696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78ce95fda35ee2d27a666b7b98f9794ce1cfb6b6247ea3e9f1a66e81aaf524`  
		Last Modified: Fri, 15 Oct 2021 23:42:44 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d76d8a0e394a23628d990878a20a7ecd15075fd8672ba117c62ce9e2c5e19e`  
		Last Modified: Fri, 15 Oct 2021 23:42:44 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e60834fe1ab1f1135de6cfe04e065dd03b639e91f03846cf857bc584697cf7`  
		Last Modified: Fri, 15 Oct 2021 23:42:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
