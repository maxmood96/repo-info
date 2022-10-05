<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.0`](#chronograf1100)
-	[`chronograf:1.10.0-alpine`](#chronograf1100-alpine)
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
$ docker pull chronograf@sha256:4d886086f35aa1f0819a453252356e4e79d2aff6ce7ac65e2c4dc5dd66e801a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:0131956c284642aa5046d24151f4c62239af3e7dbfba6b344647c7d883d68c21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81242412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6c386352e5d3d8acedc1b7778f7016879414197db6bd43b691ba41db62e1c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:58 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:05 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5465fc1b879a85d93348bfabdfcdefbb0690206998bead3c44f8d6c22cd0d42a`  
		Last Modified: Tue, 20 Sep 2022 20:23:29 GMT  
		Size: 44.6 MB (44587136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb13e1bf85984003fc04f672635ce3823c659d7a0256ecb8f4bf05818263c11`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b396867a07f1e6c1663ed3f2f1fce140e3f25d0e1b220ec844910e28d75a7dc`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bc49be513cee5763ad65b584f9dc6dda843bd132432ee82a4e99cf3af6a830`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:74369d6a1722549033636ff6deae2ad8a6b22032830073fb7eceba29d595f1ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73562035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c9aa985715d42e51fb74c1747427e927611ff0013d7f6e6d1e3cb6608334e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:04:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 01:04:39 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 05 Oct 2022 01:04:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 01:04:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 01:04:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 01:04:51 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 01:04:51 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 01:04:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 01:04:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 01:04:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc14fee07560a2936b1d20d8255a4bd556e62f7fbc6f6315b40f6414a1e4cc7a`  
		Last Modified: Wed, 05 Oct 2022 01:05:41 GMT  
		Size: 4.5 MB (4493786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5165c7780555fbc9f43e71ea6eb27a6bab287a68d2d802985d54f0da110fe045`  
		Last Modified: Wed, 05 Oct 2022 01:06:24 GMT  
		Size: 42.5 MB (42464659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e18bc5a8fc51c5e1207e5a000659db2c321522baaa001df2da8a2921dd16e`  
		Last Modified: Wed, 05 Oct 2022 01:06:15 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd30d77fb4c42b51b944e736258a7bc25bce848283ba633ac7317f69d9e6457a`  
		Last Modified: Wed, 05 Oct 2022 01:06:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01214c89af7978821fdaa181b1c762c2e3336d1f89584134b888dbdd3892ec61`  
		Last Modified: Wed, 05 Oct 2022 01:06:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab8645fbd8402ce07d268e98499311ffbb24d00e5a5363ab624561379243ed72
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77493472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d613a28bbc4f092549d7d95bc3eeb003b22ed879746050114afca2cfa421f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:45:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 00:46:33 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 05 Oct 2022 00:46:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 00:46:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 00:46:44 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 00:46:44 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 00:46:45 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 00:46:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 00:46:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 00:46:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dbe41e7f952c059f146b958dd11b6c38b9d59877811c4e18d0a39f68d60a8d`  
		Last Modified: Wed, 05 Oct 2022 00:47:31 GMT  
		Size: 5.0 MB (5004266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257b0dd82526de2a4ac4f4f98a2ac04007cf38c90ce431be31b6be1388116ea`  
		Last Modified: Wed, 05 Oct 2022 00:48:07 GMT  
		Size: 42.4 MB (42400420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227ef1fa822f9c77d8a5391f76b66e3e7ca1a891773cbb4aa4fde663a40ca8ac`  
		Last Modified: Wed, 05 Oct 2022 00:48:01 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da492be9085c913497b9f19970b5f7b6f87ac1a56205f95a292239a9adc84614`  
		Last Modified: Wed, 05 Oct 2022 00:48:01 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7ae266ac1469c396b608504f87dc74708ad757ebc00aa30023fbc52f5c4335`  
		Last Modified: Wed, 05 Oct 2022 00:48:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:10db860523fe5eebdf4890773b3e7f2e03aaa709bc7728a5acf0444b06f26217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:716811ca8465a91cf9ee2ec75857611e7859c0fbb9a2569ebc840720317be46e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30311121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e472a1f7b448779d264ff1d5a2d3e0711a25c41260fbf237eecb091cbd66b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 20 Sep 2022 20:22:08 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:14 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:14 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:15 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ea195aa67f5544afe9744fdcb50f8426f7c9e78f1d2852eedf8a4f25abe5f3`  
		Last Modified: Tue, 20 Sep 2022 20:23:46 GMT  
		Size: 27.2 MB (27174514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6442c946b6fb9dbfb0fade5a61bacb47071521acdb42ff9cfc3c786f281099de`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcf32ffd08f927f5984bcd48dce204c61e8a41cb17c10bbebe8ab5fdb8b441a`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac10f24f91124d09ad041e5953607fa76cb06490cf6412aecbf309a0ab9317d`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.0`

```console
$ docker pull chronograf@sha256:4d886086f35aa1f0819a453252356e4e79d2aff6ce7ac65e2c4dc5dd66e801a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.0` - linux; amd64

```console
$ docker pull chronograf@sha256:0131956c284642aa5046d24151f4c62239af3e7dbfba6b344647c7d883d68c21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81242412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6c386352e5d3d8acedc1b7778f7016879414197db6bd43b691ba41db62e1c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:58 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:05 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5465fc1b879a85d93348bfabdfcdefbb0690206998bead3c44f8d6c22cd0d42a`  
		Last Modified: Tue, 20 Sep 2022 20:23:29 GMT  
		Size: 44.6 MB (44587136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb13e1bf85984003fc04f672635ce3823c659d7a0256ecb8f4bf05818263c11`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b396867a07f1e6c1663ed3f2f1fce140e3f25d0e1b220ec844910e28d75a7dc`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bc49be513cee5763ad65b584f9dc6dda843bd132432ee82a4e99cf3af6a830`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:74369d6a1722549033636ff6deae2ad8a6b22032830073fb7eceba29d595f1ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73562035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c9aa985715d42e51fb74c1747427e927611ff0013d7f6e6d1e3cb6608334e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:04:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 01:04:39 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 05 Oct 2022 01:04:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 01:04:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 01:04:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 01:04:51 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 01:04:51 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 01:04:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 01:04:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 01:04:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc14fee07560a2936b1d20d8255a4bd556e62f7fbc6f6315b40f6414a1e4cc7a`  
		Last Modified: Wed, 05 Oct 2022 01:05:41 GMT  
		Size: 4.5 MB (4493786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5165c7780555fbc9f43e71ea6eb27a6bab287a68d2d802985d54f0da110fe045`  
		Last Modified: Wed, 05 Oct 2022 01:06:24 GMT  
		Size: 42.5 MB (42464659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e18bc5a8fc51c5e1207e5a000659db2c321522baaa001df2da8a2921dd16e`  
		Last Modified: Wed, 05 Oct 2022 01:06:15 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd30d77fb4c42b51b944e736258a7bc25bce848283ba633ac7317f69d9e6457a`  
		Last Modified: Wed, 05 Oct 2022 01:06:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01214c89af7978821fdaa181b1c762c2e3336d1f89584134b888dbdd3892ec61`  
		Last Modified: Wed, 05 Oct 2022 01:06:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab8645fbd8402ce07d268e98499311ffbb24d00e5a5363ab624561379243ed72
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77493472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d613a28bbc4f092549d7d95bc3eeb003b22ed879746050114afca2cfa421f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:45:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 00:46:33 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 05 Oct 2022 00:46:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 00:46:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 00:46:44 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 00:46:44 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 00:46:45 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 00:46:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 00:46:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 00:46:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dbe41e7f952c059f146b958dd11b6c38b9d59877811c4e18d0a39f68d60a8d`  
		Last Modified: Wed, 05 Oct 2022 00:47:31 GMT  
		Size: 5.0 MB (5004266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257b0dd82526de2a4ac4f4f98a2ac04007cf38c90ce431be31b6be1388116ea`  
		Last Modified: Wed, 05 Oct 2022 00:48:07 GMT  
		Size: 42.4 MB (42400420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227ef1fa822f9c77d8a5391f76b66e3e7ca1a891773cbb4aa4fde663a40ca8ac`  
		Last Modified: Wed, 05 Oct 2022 00:48:01 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da492be9085c913497b9f19970b5f7b6f87ac1a56205f95a292239a9adc84614`  
		Last Modified: Wed, 05 Oct 2022 00:48:01 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7ae266ac1469c396b608504f87dc74708ad757ebc00aa30023fbc52f5c4335`  
		Last Modified: Wed, 05 Oct 2022 00:48:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.0-alpine`

```console
$ docker pull chronograf@sha256:10db860523fe5eebdf4890773b3e7f2e03aaa709bc7728a5acf0444b06f26217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:716811ca8465a91cf9ee2ec75857611e7859c0fbb9a2569ebc840720317be46e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30311121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e472a1f7b448779d264ff1d5a2d3e0711a25c41260fbf237eecb091cbd66b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 20 Sep 2022 20:22:08 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:14 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:14 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:15 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ea195aa67f5544afe9744fdcb50f8426f7c9e78f1d2852eedf8a4f25abe5f3`  
		Last Modified: Tue, 20 Sep 2022 20:23:46 GMT  
		Size: 27.2 MB (27174514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6442c946b6fb9dbfb0fade5a61bacb47071521acdb42ff9cfc3c786f281099de`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcf32ffd08f927f5984bcd48dce204c61e8a41cb17c10bbebe8ab5fdb8b441a`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac10f24f91124d09ad041e5953607fa76cb06490cf6412aecbf309a0ab9317d`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:8ebae203f1f4187a1d0760d3093e9deef6d039f6792f6f8f8eda2fe777c053f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:d4fc995ab43dc980fde76e69903f1e7ff5bc878562ac72f0effb01c21970fc39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70584232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b71a417eed3c6b8945f33c176113cdf78a76f8ca01ee83e54caead0e1325d4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:10 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 20 Sep 2022 20:21:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:19 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fd61de5a1f4038cdacc54b6da13d30688f3110745089b278d74b40637374e9`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 4.4 MB (4418266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4b17ce7c02eeb425f2748e43546145eb3aa07d07d4285d7132738ea8460b89`  
		Last Modified: Tue, 20 Sep 2022 20:22:41 GMT  
		Size: 34.7 MB (34737452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ded8123f40f6e2139bdd178422d6cfec96a45042b0cb152a177067ddc479073`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d796f65b4868b3a4c9b3e367b950ea3c05a297d718aec4fe8beb925ec69edc52`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72071f4621e392cda688d9ecf9ea6eeb6ecb64a163d6c24327afa3203a1ad201`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4084c2b18a39914d1c000cea7bfecfdd2dc8c9b3c73abf49db5ac1860fc11b2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63420490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134a2a9ec07e16fa4402f8c415e7ce22120ff13896d31b7244d4fd9760c04f4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:03:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 01:03:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 05 Oct 2022 01:03:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 01:03:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 01:03:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 01:03:53 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 01:03:53 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 01:03:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 01:03:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 01:03:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e931f11d426389e45fd322323a3fe72a6011130c994318a8c88895eb403850b`  
		Last Modified: Wed, 05 Oct 2022 01:05:23 GMT  
		Size: 3.7 MB (3719646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e0d82c52c830b705e888c215329505bff540007ed58cc748ccf9212f5ad2e9`  
		Last Modified: Wed, 05 Oct 2022 01:05:28 GMT  
		Size: 33.1 MB (33097253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c53a3be0ec39c7d345cec125bfe633e90c666573f43186004fded74f35b2f1`  
		Last Modified: Wed, 05 Oct 2022 01:05:22 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ef0dcd6863600d8f216d50916bab30a4e763eaaee67aa124ae5f18c959c4d8`  
		Last Modified: Wed, 05 Oct 2022 01:05:22 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31090a231a7599fcfdf16ba32ab0acf19a1d44af130216b85bc871a8da844992`  
		Last Modified: Wed, 05 Oct 2022 01:05:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5b01f415476a448413268a327e51815f3bf28c749e7904e431c7479e77bc8931
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67330678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df70009ff272bd4f20603c1d3eb6417697d959cf682667337d0166c6d72e9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:45:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 00:45:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 05 Oct 2022 00:45:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 00:45:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 00:45:35 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 00:45:35 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 00:45:36 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 00:45:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 00:45:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 00:45:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c247b250948b56a735fe4dab127b1af668dd096ad230a94ee0a521187e6c923`  
		Last Modified: Wed, 05 Oct 2022 00:47:16 GMT  
		Size: 4.2 MB (4211174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b41a6bf45f4414515340b8fb736e8c18d703680373ea1d0e5e40e6278a13d76`  
		Last Modified: Wed, 05 Oct 2022 00:47:19 GMT  
		Size: 33.0 MB (33030717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3a7838b164987eeed60587e2b95200f505b563edd2d3623385248c991eaf2f`  
		Last Modified: Wed, 05 Oct 2022 00:47:15 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39297a9cd1cb6e1a169361dc32d0419b8a083d9b40efa6452709e2d8921394b`  
		Last Modified: Wed, 05 Oct 2022 00:47:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d1c2ac34db6e412347c93349601daf5ee0a21ac7fe755e8c526ce873f2f3e1`  
		Last Modified: Wed, 05 Oct 2022 00:47:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:fea4948a9d212c423a391a04a0fa1a744bab2201b04f25d28a664324916f2166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6e99be2a7bac5d79785429c530f776f1b9c4962f98ca89eba9da3accc2e0149b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22693411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613fc9f1aee33747b3623b95a2c4e433e694a02bf99b2603842cad9cd95350eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:18 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Aug 2022 18:17:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:23 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:23 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d588c7a740f6a0231b7e4eef9c215c7d86c3ee2c7629f86608c0da729d296b4`  
		Last Modified: Tue, 09 Aug 2022 18:18:23 GMT  
		Size: 19.6 MB (19556805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2285853c8534cea7724c2b4e7c863c0ca3077cea5440d2ab2a1057b3b2ae40`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 12.3 KB (12261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5295b9363991edc0b91ca76c2202f61857fa2130afd1918b477a969afba18311`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961531905b194ca826eec578c91b790b266e5c429a5969e7afb0a17a674fee7c`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:8ebae203f1f4187a1d0760d3093e9deef6d039f6792f6f8f8eda2fe777c053f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:d4fc995ab43dc980fde76e69903f1e7ff5bc878562ac72f0effb01c21970fc39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70584232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b71a417eed3c6b8945f33c176113cdf78a76f8ca01ee83e54caead0e1325d4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:10 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 20 Sep 2022 20:21:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:19 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fd61de5a1f4038cdacc54b6da13d30688f3110745089b278d74b40637374e9`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 4.4 MB (4418266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4b17ce7c02eeb425f2748e43546145eb3aa07d07d4285d7132738ea8460b89`  
		Last Modified: Tue, 20 Sep 2022 20:22:41 GMT  
		Size: 34.7 MB (34737452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ded8123f40f6e2139bdd178422d6cfec96a45042b0cb152a177067ddc479073`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d796f65b4868b3a4c9b3e367b950ea3c05a297d718aec4fe8beb925ec69edc52`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72071f4621e392cda688d9ecf9ea6eeb6ecb64a163d6c24327afa3203a1ad201`  
		Last Modified: Tue, 20 Sep 2022 20:22:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4084c2b18a39914d1c000cea7bfecfdd2dc8c9b3c73abf49db5ac1860fc11b2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63420490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134a2a9ec07e16fa4402f8c415e7ce22120ff13896d31b7244d4fd9760c04f4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:03:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 01:03:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 05 Oct 2022 01:03:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 01:03:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 01:03:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 01:03:53 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 01:03:53 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 01:03:53 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 01:03:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 01:03:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e931f11d426389e45fd322323a3fe72a6011130c994318a8c88895eb403850b`  
		Last Modified: Wed, 05 Oct 2022 01:05:23 GMT  
		Size: 3.7 MB (3719646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e0d82c52c830b705e888c215329505bff540007ed58cc748ccf9212f5ad2e9`  
		Last Modified: Wed, 05 Oct 2022 01:05:28 GMT  
		Size: 33.1 MB (33097253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c53a3be0ec39c7d345cec125bfe633e90c666573f43186004fded74f35b2f1`  
		Last Modified: Wed, 05 Oct 2022 01:05:22 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ef0dcd6863600d8f216d50916bab30a4e763eaaee67aa124ae5f18c959c4d8`  
		Last Modified: Wed, 05 Oct 2022 01:05:22 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31090a231a7599fcfdf16ba32ab0acf19a1d44af130216b85bc871a8da844992`  
		Last Modified: Wed, 05 Oct 2022 01:05:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5b01f415476a448413268a327e51815f3bf28c749e7904e431c7479e77bc8931
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67330678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df70009ff272bd4f20603c1d3eb6417697d959cf682667337d0166c6d72e9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:45:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 00:45:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 05 Oct 2022 00:45:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 00:45:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 00:45:35 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 00:45:35 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 00:45:36 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 00:45:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 00:45:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 00:45:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c247b250948b56a735fe4dab127b1af668dd096ad230a94ee0a521187e6c923`  
		Last Modified: Wed, 05 Oct 2022 00:47:16 GMT  
		Size: 4.2 MB (4211174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b41a6bf45f4414515340b8fb736e8c18d703680373ea1d0e5e40e6278a13d76`  
		Last Modified: Wed, 05 Oct 2022 00:47:19 GMT  
		Size: 33.0 MB (33030717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3a7838b164987eeed60587e2b95200f505b563edd2d3623385248c991eaf2f`  
		Last Modified: Wed, 05 Oct 2022 00:47:15 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39297a9cd1cb6e1a169361dc32d0419b8a083d9b40efa6452709e2d8921394b`  
		Last Modified: Wed, 05 Oct 2022 00:47:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d1c2ac34db6e412347c93349601daf5ee0a21ac7fe755e8c526ce873f2f3e1`  
		Last Modified: Wed, 05 Oct 2022 00:47:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:fea4948a9d212c423a391a04a0fa1a744bab2201b04f25d28a664324916f2166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6e99be2a7bac5d79785429c530f776f1b9c4962f98ca89eba9da3accc2e0149b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22693411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613fc9f1aee33747b3623b95a2c4e433e694a02bf99b2603842cad9cd95350eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:18 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 09 Aug 2022 18:17:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:23 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:23 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:23 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d588c7a740f6a0231b7e4eef9c215c7d86c3ee2c7629f86608c0da729d296b4`  
		Last Modified: Tue, 09 Aug 2022 18:18:23 GMT  
		Size: 19.6 MB (19556805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2285853c8534cea7724c2b4e7c863c0ca3077cea5440d2ab2a1057b3b2ae40`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 12.3 KB (12261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5295b9363991edc0b91ca76c2202f61857fa2130afd1918b477a969afba18311`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961531905b194ca826eec578c91b790b266e5c429a5969e7afb0a17a674fee7c`  
		Last Modified: Tue, 09 Aug 2022 18:18:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:0eb5dec159edc04d9a7e6c6c3239eb9b99823b4ffa4546d236824363a1b514a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:2b3d294298fe9a8ee83c5e01a1817489aebd1188a227da1ffaa3516632216069
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71234152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f35393ef903f1ffd2ca4858a879e4734b2f24ac99d9fa3cdd8b038212517126`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:33 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 20 Sep 2022 20:21:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:39 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee3ff3c6a1c52657ad4dde45705a73f429be88cc5b6db147420452c72f62df7`  
		Last Modified: Tue, 20 Sep 2022 20:22:57 GMT  
		Size: 34.6 MB (34578879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a73ee43124d2b0639702f98d659ae1eebb5c39681050a3d53d76373c67b390`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69ead3ae8eb920e459fbe639f0029c1d746145f8c5a569c8a034ded08a5d30`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220ca2357529bb81f6a11ef219baf2813d5e05281c27d6887652ba267811a597`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1eb3df82708a4cfd5be0ce5de63b0cb4700cc42502770560e36647c43000b8fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63847714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421cda6a39820ab3b2b72a3c9440ddbb709fdbce85e0f398dc3506657249b0eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:04:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 01:04:08 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 05 Oct 2022 01:04:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 01:04:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 01:04:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 01:04:18 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 01:04:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 01:04:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 01:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 01:04:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc14fee07560a2936b1d20d8255a4bd556e62f7fbc6f6315b40f6414a1e4cc7a`  
		Last Modified: Wed, 05 Oct 2022 01:05:41 GMT  
		Size: 4.5 MB (4493786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c7d73bdff2efca9ccc47f7b35473b6788d6b44facbe7778b1955f1dac2ad61`  
		Last Modified: Wed, 05 Oct 2022 01:05:46 GMT  
		Size: 32.8 MB (32750327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13a6d0ef7f2a508ad4df2b6d9732b431322a0846c7b365d21d112d6a3f70ca`  
		Last Modified: Wed, 05 Oct 2022 01:05:40 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bea0b0f754b0e8d66654fbf099f74d76e8ca7170e50b2f8b702ded7f5cf4dc`  
		Last Modified: Wed, 05 Oct 2022 01:05:40 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d262c7510b45c672d0de187e3ecdd70810801f22a407dc33f2e0bf4d4460245`  
		Last Modified: Wed, 05 Oct 2022 01:05:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:30f3713d9c4e563a003895b5d3f5d6c44379fbf9b42833ccdf4b140b6f6774e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67521146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffce56c52f0c5f84e9455faed01012b6bfc37a42455e36e6b5b0b5416e363bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:45:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 00:45:55 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 05 Oct 2022 00:46:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 00:46:04 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 00:46:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 00:46:05 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 00:46:06 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 00:46:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 00:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 00:46:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dbe41e7f952c059f146b958dd11b6c38b9d59877811c4e18d0a39f68d60a8d`  
		Last Modified: Wed, 05 Oct 2022 00:47:31 GMT  
		Size: 5.0 MB (5004266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290dc5a65327d6c4bce61c30a2bc726c45d57780b49933cfdf2f676521f2fde`  
		Last Modified: Wed, 05 Oct 2022 00:47:34 GMT  
		Size: 32.4 MB (32428092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c37883d573ce741de94800940caee21f906412e04da29f3b30dd40594e252`  
		Last Modified: Wed, 05 Oct 2022 00:47:30 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3aac2d484d90e6266db1a9e32852821dba849707e6d6ffd8ffa89255896465`  
		Last Modified: Wed, 05 Oct 2022 00:47:30 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8b27a47095599b776e2485c574d0a257feb20d4466383805b699467b058f39`  
		Last Modified: Wed, 05 Oct 2022 00:47:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:e21c2df83074058f591e400db598e2f2e0db991c065b382002f19a57036d65b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fbff7c953dd88ff517c74a639c8fab663fe9365b302d1e6414bea67cb3a79a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22340814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e17e2be70c7462109bc2188a05c987ba18caac5fdbe12032d9b157b5e466809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:28 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 09 Aug 2022 18:17:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:33 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:33 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf91dd373292f741fe4469ec76e73a80420fbc2da4bdc8d4d3e2f14c4cca7607`  
		Last Modified: Tue, 09 Aug 2022 18:18:37 GMT  
		Size: 19.2 MB (19204195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686071ec84727f65defe0a32dc8401552bc4e3d88c84a6e35829f0da6fb5db30`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a1a0c949f66345474da08be2eb9ad15e11a935b421d5d4d52e509861a46bf7`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae01956999004409f2013989dc7bc0d92b2ca8b9079486ad1eb081d55e5b6ae7`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:0eb5dec159edc04d9a7e6c6c3239eb9b99823b4ffa4546d236824363a1b514a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:2b3d294298fe9a8ee83c5e01a1817489aebd1188a227da1ffaa3516632216069
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71234152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f35393ef903f1ffd2ca4858a879e4734b2f24ac99d9fa3cdd8b038212517126`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:33 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 20 Sep 2022 20:21:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:39 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee3ff3c6a1c52657ad4dde45705a73f429be88cc5b6db147420452c72f62df7`  
		Last Modified: Tue, 20 Sep 2022 20:22:57 GMT  
		Size: 34.6 MB (34578879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a73ee43124d2b0639702f98d659ae1eebb5c39681050a3d53d76373c67b390`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de69ead3ae8eb920e459fbe639f0029c1d746145f8c5a569c8a034ded08a5d30`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220ca2357529bb81f6a11ef219baf2813d5e05281c27d6887652ba267811a597`  
		Last Modified: Tue, 20 Sep 2022 20:22:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1eb3df82708a4cfd5be0ce5de63b0cb4700cc42502770560e36647c43000b8fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63847714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421cda6a39820ab3b2b72a3c9440ddbb709fdbce85e0f398dc3506657249b0eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:04:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 01:04:08 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 05 Oct 2022 01:04:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 01:04:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 01:04:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 01:04:18 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 01:04:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 01:04:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 01:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 01:04:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc14fee07560a2936b1d20d8255a4bd556e62f7fbc6f6315b40f6414a1e4cc7a`  
		Last Modified: Wed, 05 Oct 2022 01:05:41 GMT  
		Size: 4.5 MB (4493786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c7d73bdff2efca9ccc47f7b35473b6788d6b44facbe7778b1955f1dac2ad61`  
		Last Modified: Wed, 05 Oct 2022 01:05:46 GMT  
		Size: 32.8 MB (32750327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd13a6d0ef7f2a508ad4df2b6d9732b431322a0846c7b365d21d112d6a3f70ca`  
		Last Modified: Wed, 05 Oct 2022 01:05:40 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bea0b0f754b0e8d66654fbf099f74d76e8ca7170e50b2f8b702ded7f5cf4dc`  
		Last Modified: Wed, 05 Oct 2022 01:05:40 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d262c7510b45c672d0de187e3ecdd70810801f22a407dc33f2e0bf4d4460245`  
		Last Modified: Wed, 05 Oct 2022 01:05:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:30f3713d9c4e563a003895b5d3f5d6c44379fbf9b42833ccdf4b140b6f6774e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67521146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffce56c52f0c5f84e9455faed01012b6bfc37a42455e36e6b5b0b5416e363bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:45:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 00:45:55 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 05 Oct 2022 00:46:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 00:46:04 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 00:46:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 00:46:05 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 00:46:06 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 00:46:08 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 00:46:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 00:46:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dbe41e7f952c059f146b958dd11b6c38b9d59877811c4e18d0a39f68d60a8d`  
		Last Modified: Wed, 05 Oct 2022 00:47:31 GMT  
		Size: 5.0 MB (5004266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290dc5a65327d6c4bce61c30a2bc726c45d57780b49933cfdf2f676521f2fde`  
		Last Modified: Wed, 05 Oct 2022 00:47:34 GMT  
		Size: 32.4 MB (32428092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c37883d573ce741de94800940caee21f906412e04da29f3b30dd40594e252`  
		Last Modified: Wed, 05 Oct 2022 00:47:30 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3aac2d484d90e6266db1a9e32852821dba849707e6d6ffd8ffa89255896465`  
		Last Modified: Wed, 05 Oct 2022 00:47:30 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8b27a47095599b776e2485c574d0a257feb20d4466383805b699467b058f39`  
		Last Modified: Wed, 05 Oct 2022 00:47:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:e21c2df83074058f591e400db598e2f2e0db991c065b382002f19a57036d65b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fbff7c953dd88ff517c74a639c8fab663fe9365b302d1e6414bea67cb3a79a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22340814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e17e2be70c7462109bc2188a05c987ba18caac5fdbe12032d9b157b5e466809`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:28 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 09 Aug 2022 18:17:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:33 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:33 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf91dd373292f741fe4469ec76e73a80420fbc2da4bdc8d4d3e2f14c4cca7607`  
		Last Modified: Tue, 09 Aug 2022 18:18:37 GMT  
		Size: 19.2 MB (19204195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686071ec84727f65defe0a32dc8401552bc4e3d88c84a6e35829f0da6fb5db30`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a1a0c949f66345474da08be2eb9ad15e11a935b421d5d4d52e509861a46bf7`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae01956999004409f2013989dc7bc0d92b2ca8b9079486ad1eb081d55e5b6ae7`  
		Last Modified: Tue, 09 Aug 2022 18:18:33 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:f91f63b7fd46cdff4fa253aae6c4fa246c7f1d564e846e5c5721692eefd11f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:694e8bab6ae3f4dd646af688f4c790cac097f7bfbebedc107036e276e9c12bec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71881717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ca8d13890b91f922f80a688845b9bdd913e1e6cdfb009e36cc8a7869eaa54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 20 Sep 2022 20:21:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:52 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:52 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f858f98c2fc7b84ac4e4e724df28aa1d1693d5ba7452b2101f450c2e1b1c8d`  
		Last Modified: Tue, 20 Sep 2022 20:23:12 GMT  
		Size: 35.2 MB (35226456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815a8049be7c95fbba36555b3d74548442f444aa4d031f194455721d8dbd735a`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94818bc4ad21b22a74a469b5fd43191967deba02360d18d9dc4a3677e445db4b`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34cc276b85549aa84243a3588344e5737bcea8a1cdd1c137e18f71f679ca0a1`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a3ea835845566de7e46098dac2788ccaea86e3ba60324ad33db22c50bdb7af43
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64623938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4976d6dabea20fb462daf1a7484441d4a1e392e86f1cba5a2b1ad0d761328756`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:04:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 01:04:24 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 05 Oct 2022 01:04:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 01:04:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 01:04:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 01:04:33 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 01:04:34 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 01:04:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 01:04:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 01:04:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc14fee07560a2936b1d20d8255a4bd556e62f7fbc6f6315b40f6414a1e4cc7a`  
		Last Modified: Wed, 05 Oct 2022 01:05:41 GMT  
		Size: 4.5 MB (4493786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1a7989fd5466c4811e805213425dc0d14330f0743bb66edc3a23ac0caaa30c`  
		Last Modified: Wed, 05 Oct 2022 01:06:04 GMT  
		Size: 33.5 MB (33526559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdf18cf6ee1467d616e2e9c58cbebde414818beb542e4af0e3165f16b9e279a`  
		Last Modified: Wed, 05 Oct 2022 01:05:58 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905a01f7abbe00038cca3087de0603252f9ec9b72f419c0cb35e35d2fe748aab`  
		Last Modified: Wed, 05 Oct 2022 01:05:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e002105531f7862e0d8e2595e56d0d9ef416c19900bd7600a430e93d521dada4`  
		Last Modified: Wed, 05 Oct 2022 01:05:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:664925066dacbf84865cc305cbaa59458e13bafd552fe49e9e809ef19cb46656
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68272322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d070c58efe6be41ad2dcad5dea7d880f0bd26bdedb6ec32c5b1633581ca6f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:45:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 00:46:14 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 05 Oct 2022 00:46:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 00:46:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 00:46:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 00:46:23 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 00:46:24 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 00:46:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 00:46:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 00:46:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dbe41e7f952c059f146b958dd11b6c38b9d59877811c4e18d0a39f68d60a8d`  
		Last Modified: Wed, 05 Oct 2022 00:47:31 GMT  
		Size: 5.0 MB (5004266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0337b1ec723076faec02f7099b2df121d8873f66a0c382bcc6e25ee47634a7a`  
		Last Modified: Wed, 05 Oct 2022 00:47:50 GMT  
		Size: 33.2 MB (33179267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29aceb288b7ad8513eb030c2af903f5a5a72f1fa367a94647af2dbce005e03a7`  
		Last Modified: Wed, 05 Oct 2022 00:47:45 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58189d45abd113f8e15a7d26ecf12e47915e2008ac7b3af2517beaaaad1edea0`  
		Last Modified: Wed, 05 Oct 2022 00:47:45 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8aaa63ceb4ecd783e409e13c38229f7bc762f245a246561f410aafcfe83983`  
		Last Modified: Wed, 05 Oct 2022 00:47:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:cf92fc3cc4691bd74be8d509e1daca31c444deeda4f588d763a6dbf938b01403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:38373234e15d1c93f102793597e9bf12e862d1c6aa7585a0bcba9c07ebc77621
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22808785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced3757bcaca9904d45cc79b6978e0aa53759fa9d16a4fb13fa24be010091f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:38 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 09 Aug 2022 18:17:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:43 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63ea984c81d9a176e87bff3e349d81ffb7375a5fbb71f461b755a13a4e2ab17`  
		Last Modified: Tue, 09 Aug 2022 18:18:51 GMT  
		Size: 19.7 MB (19672179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8828c26e16c48e93e2262d948136dc8b4f87b0a28d6a7b29b71e7a18844c1a34`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015194f0f71e31bae9c869e9a3a8d1ceca19267c54f9cc06ac3e2a9236a89f57`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0585391111ba79d1f1c74c4c722494c1e3378ab7694b9df14300c55ff270fe0`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:f91f63b7fd46cdff4fa253aae6c4fa246c7f1d564e846e5c5721692eefd11f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:694e8bab6ae3f4dd646af688f4c790cac097f7bfbebedc107036e276e9c12bec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71881717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ca8d13890b91f922f80a688845b9bdd913e1e6cdfb009e36cc8a7869eaa54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:44 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 20 Sep 2022 20:21:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:21:52 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:21:52 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:21:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:21:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:21:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f858f98c2fc7b84ac4e4e724df28aa1d1693d5ba7452b2101f450c2e1b1c8d`  
		Last Modified: Tue, 20 Sep 2022 20:23:12 GMT  
		Size: 35.2 MB (35226456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815a8049be7c95fbba36555b3d74548442f444aa4d031f194455721d8dbd735a`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94818bc4ad21b22a74a469b5fd43191967deba02360d18d9dc4a3677e445db4b`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34cc276b85549aa84243a3588344e5737bcea8a1cdd1c137e18f71f679ca0a1`  
		Last Modified: Tue, 20 Sep 2022 20:23:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a3ea835845566de7e46098dac2788ccaea86e3ba60324ad33db22c50bdb7af43
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64623938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4976d6dabea20fb462daf1a7484441d4a1e392e86f1cba5a2b1ad0d761328756`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:04:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 01:04:24 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 05 Oct 2022 01:04:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 01:04:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 01:04:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 01:04:33 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 01:04:34 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 01:04:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 01:04:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 01:04:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc14fee07560a2936b1d20d8255a4bd556e62f7fbc6f6315b40f6414a1e4cc7a`  
		Last Modified: Wed, 05 Oct 2022 01:05:41 GMT  
		Size: 4.5 MB (4493786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1a7989fd5466c4811e805213425dc0d14330f0743bb66edc3a23ac0caaa30c`  
		Last Modified: Wed, 05 Oct 2022 01:06:04 GMT  
		Size: 33.5 MB (33526559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdf18cf6ee1467d616e2e9c58cbebde414818beb542e4af0e3165f16b9e279a`  
		Last Modified: Wed, 05 Oct 2022 01:05:58 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905a01f7abbe00038cca3087de0603252f9ec9b72f419c0cb35e35d2fe748aab`  
		Last Modified: Wed, 05 Oct 2022 01:05:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e002105531f7862e0d8e2595e56d0d9ef416c19900bd7600a430e93d521dada4`  
		Last Modified: Wed, 05 Oct 2022 01:05:58 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:664925066dacbf84865cc305cbaa59458e13bafd552fe49e9e809ef19cb46656
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68272322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d070c58efe6be41ad2dcad5dea7d880f0bd26bdedb6ec32c5b1633581ca6f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:45:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 00:46:14 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 05 Oct 2022 00:46:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 00:46:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 00:46:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 00:46:23 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 00:46:24 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 00:46:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 00:46:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 00:46:27 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dbe41e7f952c059f146b958dd11b6c38b9d59877811c4e18d0a39f68d60a8d`  
		Last Modified: Wed, 05 Oct 2022 00:47:31 GMT  
		Size: 5.0 MB (5004266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0337b1ec723076faec02f7099b2df121d8873f66a0c382bcc6e25ee47634a7a`  
		Last Modified: Wed, 05 Oct 2022 00:47:50 GMT  
		Size: 33.2 MB (33179267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29aceb288b7ad8513eb030c2af903f5a5a72f1fa367a94647af2dbce005e03a7`  
		Last Modified: Wed, 05 Oct 2022 00:47:45 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58189d45abd113f8e15a7d26ecf12e47915e2008ac7b3af2517beaaaad1edea0`  
		Last Modified: Wed, 05 Oct 2022 00:47:45 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8aaa63ceb4ecd783e409e13c38229f7bc762f245a246561f410aafcfe83983`  
		Last Modified: Wed, 05 Oct 2022 00:47:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:cf92fc3cc4691bd74be8d509e1daca31c444deeda4f588d763a6dbf938b01403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:38373234e15d1c93f102793597e9bf12e862d1c6aa7585a0bcba9c07ebc77621
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22808785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced3757bcaca9904d45cc79b6978e0aa53759fa9d16a4fb13fa24be010091f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 09 Aug 2022 18:17:38 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 09 Aug 2022 18:17:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Aug 2022 18:17:43 GMT
EXPOSE 8888
# Tue, 09 Aug 2022 18:17:43 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Aug 2022 18:17:43 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 09 Aug 2022 18:17:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Aug 2022 18:17:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63ea984c81d9a176e87bff3e349d81ffb7375a5fbb71f461b755a13a4e2ab17`  
		Last Modified: Tue, 09 Aug 2022 18:18:51 GMT  
		Size: 19.7 MB (19672179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8828c26e16c48e93e2262d948136dc8b4f87b0a28d6a7b29b71e7a18844c1a34`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015194f0f71e31bae9c869e9a3a8d1ceca19267c54f9cc06ac3e2a9236a89f57`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0585391111ba79d1f1c74c4c722494c1e3378ab7694b9df14300c55ff270fe0`  
		Last Modified: Tue, 09 Aug 2022 18:18:47 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:10db860523fe5eebdf4890773b3e7f2e03aaa709bc7728a5acf0444b06f26217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:716811ca8465a91cf9ee2ec75857611e7859c0fbb9a2569ebc840720317be46e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30311121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e472a1f7b448779d264ff1d5a2d3e0711a25c41260fbf237eecb091cbd66b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 09 Aug 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 20 Sep 2022 20:22:08 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:14 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:14 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:14 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:15 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86aedf0b86f2f672427bd99edb4d53285ee3f072fdd5e4ea92fd315f1f9d2bb8`  
		Last Modified: Tue, 09 Aug 2022 18:18:07 GMT  
		Size: 284.6 KB (284571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ea195aa67f5544afe9744fdcb50f8426f7c9e78f1d2852eedf8a4f25abe5f3`  
		Last Modified: Tue, 20 Sep 2022 20:23:46 GMT  
		Size: 27.2 MB (27174514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6442c946b6fb9dbfb0fade5a61bacb47071521acdb42ff9cfc3c786f281099de`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcf32ffd08f927f5984bcd48dce204c61e8a41cb17c10bbebe8ab5fdb8b441a`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac10f24f91124d09ad041e5953607fa76cb06490cf6412aecbf309a0ab9317d`  
		Last Modified: Tue, 20 Sep 2022 20:23:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:4d886086f35aa1f0819a453252356e4e79d2aff6ce7ac65e2c4dc5dd66e801a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:0131956c284642aa5046d24151f4c62239af3e7dbfba6b344647c7d883d68c21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81242412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6c386352e5d3d8acedc1b7778f7016879414197db6bd43b691ba41db62e1c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 20 Sep 2022 20:21:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 20 Sep 2022 20:21:58 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 20 Sep 2022 20:22:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 20 Sep 2022 20:22:05 GMT
EXPOSE 8888
# Tue, 20 Sep 2022 20:22:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 20 Sep 2022 20:22:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 20 Sep 2022 20:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 Sep 2022 20:22:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9912bf5b6c0d0a8c9f83f63b25e9d2594eba49ae7977f589f65cb3c6db68ee`  
		Last Modified: Tue, 20 Sep 2022 20:22:53 GMT  
		Size: 5.2 MB (5226757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5465fc1b879a85d93348bfabdfcdefbb0690206998bead3c44f8d6c22cd0d42a`  
		Last Modified: Tue, 20 Sep 2022 20:23:29 GMT  
		Size: 44.6 MB (44587136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb13e1bf85984003fc04f672635ce3823c659d7a0256ecb8f4bf05818263c11`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b396867a07f1e6c1663ed3f2f1fce140e3f25d0e1b220ec844910e28d75a7dc`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bc49be513cee5763ad65b584f9dc6dda843bd132432ee82a4e99cf3af6a830`  
		Last Modified: Tue, 20 Sep 2022 20:23:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:74369d6a1722549033636ff6deae2ad8a6b22032830073fb7eceba29d595f1ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73562035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c9aa985715d42e51fb74c1747427e927611ff0013d7f6e6d1e3cb6608334e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:04:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 01:04:39 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 05 Oct 2022 01:04:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 01:04:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 01:04:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 01:04:51 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 01:04:51 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 01:04:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 01:04:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 01:04:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc14fee07560a2936b1d20d8255a4bd556e62f7fbc6f6315b40f6414a1e4cc7a`  
		Last Modified: Wed, 05 Oct 2022 01:05:41 GMT  
		Size: 4.5 MB (4493786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5165c7780555fbc9f43e71ea6eb27a6bab287a68d2d802985d54f0da110fe045`  
		Last Modified: Wed, 05 Oct 2022 01:06:24 GMT  
		Size: 42.5 MB (42464659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e18bc5a8fc51c5e1207e5a000659db2c321522baaa001df2da8a2921dd16e`  
		Last Modified: Wed, 05 Oct 2022 01:06:15 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd30d77fb4c42b51b944e736258a7bc25bce848283ba633ac7317f69d9e6457a`  
		Last Modified: Wed, 05 Oct 2022 01:06:15 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01214c89af7978821fdaa181b1c762c2e3336d1f89584134b888dbdd3892ec61`  
		Last Modified: Wed, 05 Oct 2022 01:06:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab8645fbd8402ce07d268e98499311ffbb24d00e5a5363ab624561379243ed72
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77493472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d613a28bbc4f092549d7d95bc3eeb003b22ed879746050114afca2cfa421f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:45:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 05 Oct 2022 00:46:33 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 05 Oct 2022 00:46:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 00:46:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 05 Oct 2022 00:46:44 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 05 Oct 2022 00:46:44 GMT
EXPOSE 8888
# Wed, 05 Oct 2022 00:46:45 GMT
VOLUME [/var/lib/chronograf]
# Wed, 05 Oct 2022 00:46:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 05 Oct 2022 00:46:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 00:46:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dbe41e7f952c059f146b958dd11b6c38b9d59877811c4e18d0a39f68d60a8d`  
		Last Modified: Wed, 05 Oct 2022 00:47:31 GMT  
		Size: 5.0 MB (5004266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257b0dd82526de2a4ac4f4f98a2ac04007cf38c90ce431be31b6be1388116ea`  
		Last Modified: Wed, 05 Oct 2022 00:48:07 GMT  
		Size: 42.4 MB (42400420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227ef1fa822f9c77d8a5391f76b66e3e7ca1a891773cbb4aa4fde663a40ca8ac`  
		Last Modified: Wed, 05 Oct 2022 00:48:01 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da492be9085c913497b9f19970b5f7b6f87ac1a56205f95a292239a9adc84614`  
		Last Modified: Wed, 05 Oct 2022 00:48:01 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7ae266ac1469c396b608504f87dc74708ad757ebc00aa30023fbc52f5c4335`  
		Last Modified: Wed, 05 Oct 2022 00:48:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
