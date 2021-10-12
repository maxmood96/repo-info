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
-	[`chronograf:1.9.0`](#chronograf190)
-	[`chronograf:1.9.0-alpine`](#chronograf190-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:7fe753307fe3bff506ce98de2480dd70db1329db6db169543a33e70d455e33c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:9b0f729ff1371373ba6f9d1bed45ae4ad3881e8cf85d5fe1bd30eb492b4703d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8c0908ff7bf9a519cc3373ce797e72ab7b740a2a6f94c640064fe1ba042f64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:04:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 28 Sep 2021 02:04:42 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 28 Sep 2021 02:04:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Sep 2021 02:04:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 28 Sep 2021 02:04:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 28 Sep 2021 02:04:51 GMT
EXPOSE 8888
# Tue, 28 Sep 2021 02:04:51 GMT
VOLUME [/var/lib/chronograf]
# Tue, 28 Sep 2021 02:04:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 28 Sep 2021 02:04:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 02:04:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac1653626616a642c9b955388bec4fd6ccb341a84db6586a598c818bf9aec99`  
		Last Modified: Tue, 28 Sep 2021 02:06:27 GMT  
		Size: 6.8 MB (6760226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e2acb47dc7cda9eaa30e5257757378078dd91753e92028419170d9dd3871eb`  
		Last Modified: Tue, 28 Sep 2021 02:06:29 GMT  
		Size: 20.0 MB (20045059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a8f3d41e2448728a82ba90cbe2dbb4b358eb58b1637b18997e5b5bd30edc2d`  
		Last Modified: Tue, 28 Sep 2021 02:06:25 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e44d43187a5d460ea3f0405e09b1045ebf6d25a6d90ad75e429d6af422fb758`  
		Last Modified: Tue, 28 Sep 2021 02:06:26 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a634154af899da447bb8c433b89c83ac6daf7e5e59aac7fe048368c7ecadbf6`  
		Last Modified: Tue, 28 Sep 2021 02:06:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:de3f574ce12e56ed95fff2dfe66f8e197e216e159688c486f9570574ffea6800
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43941734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e64cdcfde2ba1437d6cb482917144760fdc0b0bc72e73cba43c4685155ab79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:16:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:16:45 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 01 Oct 2021 05:17:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:17:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:17:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:17:04 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:17:04 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:17:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:17:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:17:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746784bfad62d65116943e0e010a50702ae1fb03d897851e36ad6b7b9fb15f4f`  
		Last Modified: Fri, 01 Oct 2021 05:20:27 GMT  
		Size: 5.8 MB (5780591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92850ca52c11f3783ad24715e8c592afdd61d1a04f7e0a68e2d36690c8b53f2`  
		Last Modified: Fri, 01 Oct 2021 05:20:37 GMT  
		Size: 18.8 MB (18820292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1f145f7751c287f8a157115897c9cc770e6cce530516edc69e64923ef6a239`  
		Last Modified: Fri, 01 Oct 2021 05:20:24 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ca58671a9920283df121d4d9f5c67063ed00e7e7703fc215b3701ea86bc43`  
		Last Modified: Fri, 01 Oct 2021 05:20:24 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6b6906b42d639c5d1fda14068987acff10a56374cec47b964b5786269a131`  
		Last Modified: Fri, 01 Oct 2021 05:20:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f3f94b901f49e9126af4b6764a613041372c241862f143f41f841842b0d02198
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d822691295a3377b2e34a1a8d951ea6f95ab88442e4e023708fce26aa0a47a7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:24:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 02:24:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:24:57 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:24:57 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:24:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c80a13875d1601dda5709f1d69a00589cf3ce58b12f53fa1f724cd72014207`  
		Last Modified: Tue, 12 Oct 2021 02:26:25 GMT  
		Size: 19.0 MB (18961773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385e3003b1770a74069520dd203b4146211b03893fe9e3cb1128bbec6988f20e`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c20fad82f79c98ea608757c45478eee61b9bd857812b095623c2765c82e5f8f`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d145d4d4dbcb7a3f9c5ed61739d22752a3376db5bef7dd9939b863381d500426`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:a3dea9fd70283af740db184d94417ee4c3fc1375532175d597122c325b664c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b14ee1822937fb01816a97288646858f187d0f02f9fd6eeeb448b30d07b2617c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14843918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c622c45336d64ee0a6e08ce97bc55bf23712e39ca3061372e2000223e9cf6a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:23:43 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 01 Sep 2021 00:23:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:23:53 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:23:53 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:23:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:23:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62726903f0c0c59223b83affe0ace7300a908ba6fcea73b6c79ae3a146d2b5af`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 11.7 MB (11736770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4336cfd351b47edce706376e043d71589101d40dce396d37efca10babe80d`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 12.3 KB (12273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbb150a469535e39e060b4b33bcad3378c611bded830e04ccb39c1942fb50de`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3550bbef48514edb6130449969746fb016808bb6c02b3e838ac98278f8869df1`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:7fe753307fe3bff506ce98de2480dd70db1329db6db169543a33e70d455e33c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:9b0f729ff1371373ba6f9d1bed45ae4ad3881e8cf85d5fe1bd30eb492b4703d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49357381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8c0908ff7bf9a519cc3373ce797e72ab7b740a2a6f94c640064fe1ba042f64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:04:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 28 Sep 2021 02:04:42 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 28 Sep 2021 02:04:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Sep 2021 02:04:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 28 Sep 2021 02:04:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 28 Sep 2021 02:04:51 GMT
EXPOSE 8888
# Tue, 28 Sep 2021 02:04:51 GMT
VOLUME [/var/lib/chronograf]
# Tue, 28 Sep 2021 02:04:51 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 28 Sep 2021 02:04:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 02:04:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac1653626616a642c9b955388bec4fd6ccb341a84db6586a598c818bf9aec99`  
		Last Modified: Tue, 28 Sep 2021 02:06:27 GMT  
		Size: 6.8 MB (6760226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e2acb47dc7cda9eaa30e5257757378078dd91753e92028419170d9dd3871eb`  
		Last Modified: Tue, 28 Sep 2021 02:06:29 GMT  
		Size: 20.0 MB (20045059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a8f3d41e2448728a82ba90cbe2dbb4b358eb58b1637b18997e5b5bd30edc2d`  
		Last Modified: Tue, 28 Sep 2021 02:06:25 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e44d43187a5d460ea3f0405e09b1045ebf6d25a6d90ad75e429d6af422fb758`  
		Last Modified: Tue, 28 Sep 2021 02:06:26 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a634154af899da447bb8c433b89c83ac6daf7e5e59aac7fe048368c7ecadbf6`  
		Last Modified: Tue, 28 Sep 2021 02:06:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:de3f574ce12e56ed95fff2dfe66f8e197e216e159688c486f9570574ffea6800
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43941734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e64cdcfde2ba1437d6cb482917144760fdc0b0bc72e73cba43c4685155ab79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:16:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:16:45 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 01 Oct 2021 05:17:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:17:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:17:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:17:04 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:17:04 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:17:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:17:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:17:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746784bfad62d65116943e0e010a50702ae1fb03d897851e36ad6b7b9fb15f4f`  
		Last Modified: Fri, 01 Oct 2021 05:20:27 GMT  
		Size: 5.8 MB (5780591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92850ca52c11f3783ad24715e8c592afdd61d1a04f7e0a68e2d36690c8b53f2`  
		Last Modified: Fri, 01 Oct 2021 05:20:37 GMT  
		Size: 18.8 MB (18820292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1f145f7751c287f8a157115897c9cc770e6cce530516edc69e64923ef6a239`  
		Last Modified: Fri, 01 Oct 2021 05:20:24 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ca58671a9920283df121d4d9f5c67063ed00e7e7703fc215b3701ea86bc43`  
		Last Modified: Fri, 01 Oct 2021 05:20:24 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c6b6906b42d639c5d1fda14068987acff10a56374cec47b964b5786269a131`  
		Last Modified: Fri, 01 Oct 2021 05:20:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f3f94b901f49e9126af4b6764a613041372c241862f143f41f841842b0d02198
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d822691295a3377b2e34a1a8d951ea6f95ab88442e4e023708fce26aa0a47a7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:24:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 12 Oct 2021 02:24:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:24:57 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:24:57 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:24:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:24:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c80a13875d1601dda5709f1d69a00589cf3ce58b12f53fa1f724cd72014207`  
		Last Modified: Tue, 12 Oct 2021 02:26:25 GMT  
		Size: 19.0 MB (18961773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385e3003b1770a74069520dd203b4146211b03893fe9e3cb1128bbec6988f20e`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c20fad82f79c98ea608757c45478eee61b9bd857812b095623c2765c82e5f8f`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d145d4d4dbcb7a3f9c5ed61739d22752a3376db5bef7dd9939b863381d500426`  
		Last Modified: Tue, 12 Oct 2021 02:26:21 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:a3dea9fd70283af740db184d94417ee4c3fc1375532175d597122c325b664c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b14ee1822937fb01816a97288646858f187d0f02f9fd6eeeb448b30d07b2617c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14843918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c622c45336d64ee0a6e08ce97bc55bf23712e39ca3061372e2000223e9cf6a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:23:43 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 01 Sep 2021 00:23:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:23:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:23:53 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:23:53 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:23:53 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:23:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62726903f0c0c59223b83affe0ace7300a908ba6fcea73b6c79ae3a146d2b5af`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 11.7 MB (11736770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4336cfd351b47edce706376e043d71589101d40dce396d37efca10babe80d`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 12.3 KB (12273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbb150a469535e39e060b4b33bcad3378c611bded830e04ccb39c1942fb50de`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3550bbef48514edb6130449969746fb016808bb6c02b3e838ac98278f8869df1`  
		Last Modified: Wed, 01 Sep 2021 00:25:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:5db1b8f6d8a535143a5e7b5c80dabf741daad035d77a2e4658de52baf1cd7dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:a7ee375b357ba11c357519c0fca28150f5a603ae71086749ea9ceb4161889673
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65386520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7e48b3270c2962c5ccb411c6ddaf8a69c6db2874a4eea8af4ed9c9c8f6001e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:05:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 28 Sep 2021 02:05:13 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 28 Sep 2021 02:05:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Sep 2021 02:05:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 28 Sep 2021 02:05:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 28 Sep 2021 02:05:25 GMT
EXPOSE 8888
# Tue, 28 Sep 2021 02:05:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 28 Sep 2021 02:05:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 28 Sep 2021 02:05:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 02:05:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2853a945a7cf9c6206d8e7c8f360ccd0fa4d343948250279ad4842575b58938`  
		Last Modified: Tue, 28 Sep 2021 02:06:41 GMT  
		Size: 4.5 MB (4506508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69529055d5b5cde5cd2e1378f4923e9184c5ea887a1e7e24ac942bfe1df273e3`  
		Last Modified: Tue, 28 Sep 2021 02:06:45 GMT  
		Size: 38.3 MB (38327919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7406ffbe0e96e9d6ee063447eaabb94667a35872714e46ceb670e4f260b0183`  
		Last Modified: Tue, 28 Sep 2021 02:06:40 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c8601cc064b6cf959ea083710d462ef3767d7577468f125ff1de0afb9fc57c`  
		Last Modified: Tue, 28 Sep 2021 02:06:40 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef6ad82f5f9b570365828e7576c0ff535087a748dc1268b185c880390defd4`  
		Last Modified: Tue, 28 Sep 2021 02:06:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ecdf4764bcfa1390c80aead710685879c8005b62d3a1494a5eafecf30b1b3ca0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59004012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c0c06dd732d8aa3110b75a75c0b77dc4cd1df27d39dc823b145be17fc0c366`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:17:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:17:42 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 01 Oct 2021 05:18:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:18:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:18:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:18:15 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:18:16 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:18:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:18:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9765b095f27b0c50afae66c3dd0e27bbefe1b0a823ac79ced9868d0419c365e`  
		Last Modified: Fri, 01 Oct 2021 05:20:51 GMT  
		Size: 3.9 MB (3879881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190cb25c4ca68724115fb71b13938fb8ca58f18c7056a6b5965a396c12a07e1b`  
		Last Modified: Fri, 01 Oct 2021 05:21:08 GMT  
		Size: 35.8 MB (35783272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf0852e5a9f412591b4fe17c26253a3cec476493bfa9cc552d0aad2d071b471`  
		Last Modified: Fri, 01 Oct 2021 05:20:50 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fb6bcc94e2a9eb3c2f12aac4a1d1ba022aa903e566a910087251f97d6d44ce`  
		Last Modified: Fri, 01 Oct 2021 05:20:49 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aba384b697f50b0c22b4b6722d1f62fc2bd79bbf9a14f87028f91c6e0826b1`  
		Last Modified: Fri, 01 Oct 2021 05:20:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:adeac5d4387c7576c8579eaad716e24486db0062c58fb80ef7d8192615d5a944
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60483654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd33a9716e9e3159b09ae9cfc8740db8727600c4e5bff17fc22df6ec8dfd2a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:25:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:14 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 02:25:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:24 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f76b6a4b9313ee67027ac38a67f4f5f5af946bfcab3f702b4c663ccca1d7e5`  
		Last Modified: Tue, 12 Oct 2021 02:26:37 GMT  
		Size: 4.1 MB (4082592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca94d0146c32da4f5e1d8c0bbfb32fbc13d56a6bdeff65499ac569e504608c3`  
		Last Modified: Tue, 12 Oct 2021 02:26:41 GMT  
		Size: 36.0 MB (35987214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392069b3957ad6611f447e44730a5f67aea67ebc67e2b5061e21cda77ea09de7`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770e379656b239a44ddc6963f4d9225f45c07df1cc9e25297bb7bfddff3a2fd9`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9246ed914e241e65ac16ea65cf8a04e0c8b15487a71ab33fe11ea72278f6ee`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:9b177c70e25de297b100d46ba7eb922ac167a8e65f698480e2785b1886cb94a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c3a41e489e87268456b3ac8beea5f7c2a516dc7d43af6f7066be8b9675492d70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22662384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a94fa13b711dbb3a88df7489d3353cc6e4777a37a87a0788d36cef2fdc64c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 01 Sep 2021 00:24:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:15 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:15 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a1ffa92682ef14beba92c11f3c21d02b50a70f56f234ab814e604f678b2b31`  
		Last Modified: Wed, 01 Sep 2021 00:25:49 GMT  
		Size: 19.6 MB (19555249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dbb12c4afee159bb53c97f3d0cb65034efe2713363365b1f7f5f7affb916fe`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ba26fb8530e7520df76f60ae8b3f9e317561d15deea2b4738f5c3e4b47e11`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9b8b115b6329338ab5fea52358a641fbb017ecd917613643e4cbce6b3f081f`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:5db1b8f6d8a535143a5e7b5c80dabf741daad035d77a2e4658de52baf1cd7dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:a7ee375b357ba11c357519c0fca28150f5a603ae71086749ea9ceb4161889673
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65386520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7e48b3270c2962c5ccb411c6ddaf8a69c6db2874a4eea8af4ed9c9c8f6001e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:05:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 28 Sep 2021 02:05:13 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 28 Sep 2021 02:05:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Sep 2021 02:05:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 28 Sep 2021 02:05:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 28 Sep 2021 02:05:25 GMT
EXPOSE 8888
# Tue, 28 Sep 2021 02:05:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 28 Sep 2021 02:05:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 28 Sep 2021 02:05:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 02:05:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2853a945a7cf9c6206d8e7c8f360ccd0fa4d343948250279ad4842575b58938`  
		Last Modified: Tue, 28 Sep 2021 02:06:41 GMT  
		Size: 4.5 MB (4506508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69529055d5b5cde5cd2e1378f4923e9184c5ea887a1e7e24ac942bfe1df273e3`  
		Last Modified: Tue, 28 Sep 2021 02:06:45 GMT  
		Size: 38.3 MB (38327919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7406ffbe0e96e9d6ee063447eaabb94667a35872714e46ceb670e4f260b0183`  
		Last Modified: Tue, 28 Sep 2021 02:06:40 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c8601cc064b6cf959ea083710d462ef3767d7577468f125ff1de0afb9fc57c`  
		Last Modified: Tue, 28 Sep 2021 02:06:40 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef6ad82f5f9b570365828e7576c0ff535087a748dc1268b185c880390defd4`  
		Last Modified: Tue, 28 Sep 2021 02:06:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ecdf4764bcfa1390c80aead710685879c8005b62d3a1494a5eafecf30b1b3ca0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59004012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c0c06dd732d8aa3110b75a75c0b77dc4cd1df27d39dc823b145be17fc0c366`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:17:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:17:42 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 01 Oct 2021 05:18:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:18:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:18:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:18:15 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:18:16 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:18:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:18:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9765b095f27b0c50afae66c3dd0e27bbefe1b0a823ac79ced9868d0419c365e`  
		Last Modified: Fri, 01 Oct 2021 05:20:51 GMT  
		Size: 3.9 MB (3879881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190cb25c4ca68724115fb71b13938fb8ca58f18c7056a6b5965a396c12a07e1b`  
		Last Modified: Fri, 01 Oct 2021 05:21:08 GMT  
		Size: 35.8 MB (35783272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf0852e5a9f412591b4fe17c26253a3cec476493bfa9cc552d0aad2d071b471`  
		Last Modified: Fri, 01 Oct 2021 05:20:50 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fb6bcc94e2a9eb3c2f12aac4a1d1ba022aa903e566a910087251f97d6d44ce`  
		Last Modified: Fri, 01 Oct 2021 05:20:49 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aba384b697f50b0c22b4b6722d1f62fc2bd79bbf9a14f87028f91c6e0826b1`  
		Last Modified: Fri, 01 Oct 2021 05:20:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:adeac5d4387c7576c8579eaad716e24486db0062c58fb80ef7d8192615d5a944
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60483654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd33a9716e9e3159b09ae9cfc8740db8727600c4e5bff17fc22df6ec8dfd2a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:25:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:14 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Oct 2021 02:25:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:23 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:24 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f76b6a4b9313ee67027ac38a67f4f5f5af946bfcab3f702b4c663ccca1d7e5`  
		Last Modified: Tue, 12 Oct 2021 02:26:37 GMT  
		Size: 4.1 MB (4082592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca94d0146c32da4f5e1d8c0bbfb32fbc13d56a6bdeff65499ac569e504608c3`  
		Last Modified: Tue, 12 Oct 2021 02:26:41 GMT  
		Size: 36.0 MB (35987214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392069b3957ad6611f447e44730a5f67aea67ebc67e2b5061e21cda77ea09de7`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770e379656b239a44ddc6963f4d9225f45c07df1cc9e25297bb7bfddff3a2fd9`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9246ed914e241e65ac16ea65cf8a04e0c8b15487a71ab33fe11ea72278f6ee`  
		Last Modified: Tue, 12 Oct 2021 02:26:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:9b177c70e25de297b100d46ba7eb922ac167a8e65f698480e2785b1886cb94a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c3a41e489e87268456b3ac8beea5f7c2a516dc7d43af6f7066be8b9675492d70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22662384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a94fa13b711dbb3a88df7489d3353cc6e4777a37a87a0788d36cef2fdc64c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 01 Sep 2021 00:24:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:14 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:15 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:15 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:16 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a1ffa92682ef14beba92c11f3c21d02b50a70f56f234ab814e604f678b2b31`  
		Last Modified: Wed, 01 Sep 2021 00:25:49 GMT  
		Size: 19.6 MB (19555249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dbb12c4afee159bb53c97f3d0cb65034efe2713363365b1f7f5f7affb916fe`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ba26fb8530e7520df76f60ae8b3f9e317561d15deea2b4738f5c3e4b47e11`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9b8b115b6329338ab5fea52358a641fbb017ecd917613643e4cbce6b3f081f`  
		Last Modified: Wed, 01 Sep 2021 00:25:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:8d81bd7b4391415f211507b119213f80d81d36599b115af271e315e5f4c349b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:5803aad472f3df866a4eeb6fec687bd68a01aadf17dc2e4880a9cc1184c74b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845900bd3c5d154c9ca7ed5b502968c1a3e1e5b1e77ebc4398b9156836710b2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:04:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 28 Sep 2021 02:05:34 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 28 Sep 2021 02:05:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Sep 2021 02:05:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 28 Sep 2021 02:05:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 28 Sep 2021 02:05:43 GMT
EXPOSE 8888
# Tue, 28 Sep 2021 02:05:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 28 Sep 2021 02:05:44 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 28 Sep 2021 02:05:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 02:05:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac1653626616a642c9b955388bec4fd6ccb341a84db6586a598c818bf9aec99`  
		Last Modified: Tue, 28 Sep 2021 02:06:27 GMT  
		Size: 6.8 MB (6760226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed1cde8d8940dab2b37d8c25ecdd256da47180c9f32698f21f3705cf03ee15f`  
		Last Modified: Tue, 28 Sep 2021 02:07:01 GMT  
		Size: 36.9 MB (36926062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8aec9fec9007f779f1ae1339d4dc70704a6e57918cb3ad81899bac570281c9`  
		Last Modified: Tue, 28 Sep 2021 02:06:56 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3803f255137c036e4b2e279d68831806c950a1bae670eeb13c3ab2acaa366986`  
		Last Modified: Tue, 28 Sep 2021 02:06:56 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f8f828ec61c7f80593ccaf8d07629a69dcd411300f5dc6686aabb91ce69ca5`  
		Last Modified: Tue, 28 Sep 2021 02:06:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c8d627a8b32106d64acdb406dca4b06a8cdb465edf348b9c453bd4760d0dbe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59632607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b0c56b08f26a9b47e6226e04c277fe74210547d84af9801aa893693337d4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:16:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:18:36 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 01 Oct 2021 05:18:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:18:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:18:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:18:57 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:18:58 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:18:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:18:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:18:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746784bfad62d65116943e0e010a50702ae1fb03d897851e36ad6b7b9fb15f4f`  
		Last Modified: Fri, 01 Oct 2021 05:20:27 GMT  
		Size: 5.8 MB (5780591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68ca75903ddc598693d1086158ac8bc0c601e3e95b4e18e335a45bc771e5927`  
		Last Modified: Fri, 01 Oct 2021 05:21:37 GMT  
		Size: 34.5 MB (34511170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a27dc6eeaf434a7b16a4be0a5fd4f63b3e9f1c5cd4b03f5fbb4d759e73acd`  
		Last Modified: Fri, 01 Oct 2021 05:21:20 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504bf596da81756db068927df3cb0123ee6e15645ce38b8e54abcb30974c73e`  
		Last Modified: Fri, 01 Oct 2021 05:21:20 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97f27e4a0b5b5e467d888bcb1a036dc6b2beb47087a1dacae4bc008ed8a6f2c`  
		Last Modified: Fri, 01 Oct 2021 05:21:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab6f87343df4ac8dff564bbf4561e54c41f76343461cab1af174cdb4ae9fc099
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60894104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2db46ffbab26315fb63c807d93c54ed1a66dbae430804cb81753faba4cb4c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 02:25:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:39 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08264f151f4d30a4fba68d5fe51630efced126fd472dcfb44cb30ee0b000a1b`  
		Last Modified: Tue, 12 Oct 2021 02:26:58 GMT  
		Size: 34.4 MB (34432275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a037be6d9070a98b468bae7a099e5478093d677b9f944f2ae1c8cda8dc38098`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e428abd6250e9e7fbbc22dd13bbed705111a055e1175e302203f4a361b6e83f5`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb99c2fa13e01a038fbb1101249ed08a0ebd2d4e4daa5d6e325f55aa68e1b0d`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:30f63fa8f9214eb152af97cd85908e510c913d81f80a49b9c232ea42c281b9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7c4dd500f22766f0a514d9a2d1d13c944e2aaeb5be7f2be304ae8ef21ec9bead
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22311020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419075de283e08462528ab9737dd9a32b8e4150dc96635bda486afb9571f2905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 01 Sep 2021 00:24:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:32 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:33 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9dd2619092db5ca6cb874052a71c03376efbdde1ef7f45ffd85cfa8282b9fd`  
		Last Modified: Wed, 01 Sep 2021 00:26:04 GMT  
		Size: 19.2 MB (19203889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799830d16117d477b1f2c4fa56db3520d04b1100e2330e4e4f5458ff89e0968`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 12.3 KB (12259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c610504f400b831a31045e828f0250e107de5ad4786642d241b0b70d2e5f744`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996e4d82939f361d8f0003173b864e68be9fe64e83e3f4cabba3aafe8ef39f01`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:8d81bd7b4391415f211507b119213f80d81d36599b115af271e315e5f4c349b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:5803aad472f3df866a4eeb6fec687bd68a01aadf17dc2e4880a9cc1184c74b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66238384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845900bd3c5d154c9ca7ed5b502968c1a3e1e5b1e77ebc4398b9156836710b2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:04:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 28 Sep 2021 02:05:34 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 28 Sep 2021 02:05:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Sep 2021 02:05:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 28 Sep 2021 02:05:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 28 Sep 2021 02:05:43 GMT
EXPOSE 8888
# Tue, 28 Sep 2021 02:05:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 28 Sep 2021 02:05:44 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 28 Sep 2021 02:05:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 02:05:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac1653626616a642c9b955388bec4fd6ccb341a84db6586a598c818bf9aec99`  
		Last Modified: Tue, 28 Sep 2021 02:06:27 GMT  
		Size: 6.8 MB (6760226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed1cde8d8940dab2b37d8c25ecdd256da47180c9f32698f21f3705cf03ee15f`  
		Last Modified: Tue, 28 Sep 2021 02:07:01 GMT  
		Size: 36.9 MB (36926062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8aec9fec9007f779f1ae1339d4dc70704a6e57918cb3ad81899bac570281c9`  
		Last Modified: Tue, 28 Sep 2021 02:06:56 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3803f255137c036e4b2e279d68831806c950a1bae670eeb13c3ab2acaa366986`  
		Last Modified: Tue, 28 Sep 2021 02:06:56 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f8f828ec61c7f80593ccaf8d07629a69dcd411300f5dc6686aabb91ce69ca5`  
		Last Modified: Tue, 28 Sep 2021 02:06:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c8d627a8b32106d64acdb406dca4b06a8cdb465edf348b9c453bd4760d0dbe7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59632607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b0c56b08f26a9b47e6226e04c277fe74210547d84af9801aa893693337d4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:16:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:18:36 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 01 Oct 2021 05:18:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:18:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:18:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:18:57 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:18:58 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:18:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:18:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:18:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746784bfad62d65116943e0e010a50702ae1fb03d897851e36ad6b7b9fb15f4f`  
		Last Modified: Fri, 01 Oct 2021 05:20:27 GMT  
		Size: 5.8 MB (5780591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68ca75903ddc598693d1086158ac8bc0c601e3e95b4e18e335a45bc771e5927`  
		Last Modified: Fri, 01 Oct 2021 05:21:37 GMT  
		Size: 34.5 MB (34511170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228a27dc6eeaf434a7b16a4be0a5fd4f63b3e9f1c5cd4b03f5fbb4d759e73acd`  
		Last Modified: Fri, 01 Oct 2021 05:21:20 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504bf596da81756db068927df3cb0123ee6e15645ce38b8e54abcb30974c73e`  
		Last Modified: Fri, 01 Oct 2021 05:21:20 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97f27e4a0b5b5e467d888bcb1a036dc6b2beb47087a1dacae4bc008ed8a6f2c`  
		Last Modified: Fri, 01 Oct 2021 05:21:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab6f87343df4ac8dff564bbf4561e54c41f76343461cab1af174cdb4ae9fc099
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60894104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2db46ffbab26315fb63c807d93c54ed1a66dbae430804cb81753faba4cb4c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Oct 2021 02:25:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:39 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08264f151f4d30a4fba68d5fe51630efced126fd472dcfb44cb30ee0b000a1b`  
		Last Modified: Tue, 12 Oct 2021 02:26:58 GMT  
		Size: 34.4 MB (34432275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a037be6d9070a98b468bae7a099e5478093d677b9f944f2ae1c8cda8dc38098`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e428abd6250e9e7fbbc22dd13bbed705111a055e1175e302203f4a361b6e83f5`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb99c2fa13e01a038fbb1101249ed08a0ebd2d4e4daa5d6e325f55aa68e1b0d`  
		Last Modified: Tue, 12 Oct 2021 02:26:53 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:30f63fa8f9214eb152af97cd85908e510c913d81f80a49b9c232ea42c281b9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7c4dd500f22766f0a514d9a2d1d13c944e2aaeb5be7f2be304ae8ef21ec9bead
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22311020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419075de283e08462528ab9737dd9a32b8e4150dc96635bda486afb9571f2905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 01 Sep 2021 00:24:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:31 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:32 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:33 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9dd2619092db5ca6cb874052a71c03376efbdde1ef7f45ffd85cfa8282b9fd`  
		Last Modified: Wed, 01 Sep 2021 00:26:04 GMT  
		Size: 19.2 MB (19203889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799830d16117d477b1f2c4fa56db3520d04b1100e2330e4e4f5458ff89e0968`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 12.3 KB (12259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c610504f400b831a31045e828f0250e107de5ad4786642d241b0b70d2e5f744`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996e4d82939f361d8f0003173b864e68be9fe64e83e3f4cabba3aafe8ef39f01`  
		Last Modified: Wed, 01 Sep 2021 00:26:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:7c9afa8b840c273dd861a6122cea5bd076935949d88fd222a4f23dad3eb44d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:d7e1b83ef03cc2ada6ddb4262a9ef6141d69252b4229f9312022de422eba9628
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592c5727cec3ebc49e90e1a1db3158afe8ff3c4f974e2d823f94ed2de681d3b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:04:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 28 Sep 2021 02:05:50 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 28 Sep 2021 02:05:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Sep 2021 02:05:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 28 Sep 2021 02:05:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 28 Sep 2021 02:05:58 GMT
EXPOSE 8888
# Tue, 28 Sep 2021 02:05:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 28 Sep 2021 02:05:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 28 Sep 2021 02:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 02:05:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac1653626616a642c9b955388bec4fd6ccb341a84db6586a598c818bf9aec99`  
		Last Modified: Tue, 28 Sep 2021 02:06:27 GMT  
		Size: 6.8 MB (6760226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211fad620672de80aa2eb37b52a4a350fca5b115b59a0f29c453dbc33106c842`  
		Last Modified: Tue, 28 Sep 2021 02:07:16 GMT  
		Size: 37.4 MB (37444950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b042071506815e237e7038debb7644e8651b62ae7f6eeee08cf3cc9f25dff`  
		Last Modified: Tue, 28 Sep 2021 02:07:12 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6813cf7b046ff4142fd4d0ba58ec4314368c6ff87a0f6a445a74c17954c68e`  
		Last Modified: Tue, 28 Sep 2021 02:07:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a88a250951fd04184933bd60acad8ee24297dc2caea606c9df00226ecc0cb2`  
		Last Modified: Tue, 28 Sep 2021 02:07:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1eaf9d54e80ec37220bf2e5c6772857401e611fa6e2974575ea238562e5eca8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60286017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3a0ed0ab3e2cf3af8f6c357383296fab4fc5a676f0dec7a7c3a9d6241605f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:16:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:19:09 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 01 Oct 2021 05:19:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:19:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:19:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:19:30 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:19:30 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:19:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:19:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:19:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746784bfad62d65116943e0e010a50702ae1fb03d897851e36ad6b7b9fb15f4f`  
		Last Modified: Fri, 01 Oct 2021 05:20:27 GMT  
		Size: 5.8 MB (5780591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f70d7dadcc587b01abb272b80cd64ba42d1e0d123c14ba94201cee1546f599f`  
		Last Modified: Fri, 01 Oct 2021 05:22:08 GMT  
		Size: 35.2 MB (35164577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e81f2620fb3a78dd449c871aa0dffb8d612270c0e4926e70bd9a4ac20d22872`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76af3bdd08d13774a02d1879f55bd572d8fef6cce9f936f0a5457bd76d04986`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf79df797875a5efea73a0584f057cd1ec273b5e125195997c57e405c247186`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f8b10eabd6a93f7fcbc8d8acce2b60e412754a07bb95664a8b3caa800ca21c38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc16a9b86e7c3cd6838f8aae38c005ab4d37fd1595c576151580683e74909a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:45 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 12 Oct 2021 02:25:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:53 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:53 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc03711acce0b5e2f3e2ad7249ce4962fdd520835a1c778de663b9f2bec5f309`  
		Last Modified: Tue, 12 Oct 2021 02:27:14 GMT  
		Size: 35.1 MB (35061492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ac3e7452691d4edc39f45e7e6706d3dcf06f188bb81aa96749fe12906f31bc`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef8988907a0a7be1f7d83a61d1aeaf02ef140108fff7f975c89339dd03e7848`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb9b5f2079e26ff03ed792915e6a981d31ea534399c82cf9eee4a529a07ae60`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:bdb38dbf0d72892a4685b69391c89a1716a2465b0d52f79bd859a846f982c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:44ddcc13955fcee6ada98e17e24ee8f695a9823b3c3e999e5d315c9a3bb0aa8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22689227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86636178ef7f0961c639954f1607c343f7ed49e2749304818d81e8d9aaec58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:42 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Wed, 01 Sep 2021 00:24:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:50 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0062288c23918a5c405390da5fe197e453d3162f22d5e04c4e80c771bfb7dbb`  
		Last Modified: Wed, 01 Sep 2021 00:26:19 GMT  
		Size: 19.6 MB (19582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56af5fa9abf70534bf74916985c59602805aaec20e843a8fb80451dc2b4aa6b`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 12.3 KB (12269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad79cf9294c71cb171d84b1b435766c73b488c2eaf98668e8fb24c098ec8e0`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584912177323f577d098fda53486bc0f440c26efb41dd2951ee13af7a0f369`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.0`

```console
$ docker pull chronograf@sha256:7c9afa8b840c273dd861a6122cea5bd076935949d88fd222a4f23dad3eb44d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.0` - linux; amd64

```console
$ docker pull chronograf@sha256:d7e1b83ef03cc2ada6ddb4262a9ef6141d69252b4229f9312022de422eba9628
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592c5727cec3ebc49e90e1a1db3158afe8ff3c4f974e2d823f94ed2de681d3b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:04:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 28 Sep 2021 02:05:50 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 28 Sep 2021 02:05:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Sep 2021 02:05:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 28 Sep 2021 02:05:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 28 Sep 2021 02:05:58 GMT
EXPOSE 8888
# Tue, 28 Sep 2021 02:05:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 28 Sep 2021 02:05:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 28 Sep 2021 02:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 02:05:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac1653626616a642c9b955388bec4fd6ccb341a84db6586a598c818bf9aec99`  
		Last Modified: Tue, 28 Sep 2021 02:06:27 GMT  
		Size: 6.8 MB (6760226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211fad620672de80aa2eb37b52a4a350fca5b115b59a0f29c453dbc33106c842`  
		Last Modified: Tue, 28 Sep 2021 02:07:16 GMT  
		Size: 37.4 MB (37444950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b042071506815e237e7038debb7644e8651b62ae7f6eeee08cf3cc9f25dff`  
		Last Modified: Tue, 28 Sep 2021 02:07:12 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6813cf7b046ff4142fd4d0ba58ec4314368c6ff87a0f6a445a74c17954c68e`  
		Last Modified: Tue, 28 Sep 2021 02:07:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a88a250951fd04184933bd60acad8ee24297dc2caea606c9df00226ecc0cb2`  
		Last Modified: Tue, 28 Sep 2021 02:07:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1eaf9d54e80ec37220bf2e5c6772857401e611fa6e2974575ea238562e5eca8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60286017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3a0ed0ab3e2cf3af8f6c357383296fab4fc5a676f0dec7a7c3a9d6241605f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:16:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:19:09 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 01 Oct 2021 05:19:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:19:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:19:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:19:30 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:19:30 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:19:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:19:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:19:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746784bfad62d65116943e0e010a50702ae1fb03d897851e36ad6b7b9fb15f4f`  
		Last Modified: Fri, 01 Oct 2021 05:20:27 GMT  
		Size: 5.8 MB (5780591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f70d7dadcc587b01abb272b80cd64ba42d1e0d123c14ba94201cee1546f599f`  
		Last Modified: Fri, 01 Oct 2021 05:22:08 GMT  
		Size: 35.2 MB (35164577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e81f2620fb3a78dd449c871aa0dffb8d612270c0e4926e70bd9a4ac20d22872`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76af3bdd08d13774a02d1879f55bd572d8fef6cce9f936f0a5457bd76d04986`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf79df797875a5efea73a0584f057cd1ec273b5e125195997c57e405c247186`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f8b10eabd6a93f7fcbc8d8acce2b60e412754a07bb95664a8b3caa800ca21c38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc16a9b86e7c3cd6838f8aae38c005ab4d37fd1595c576151580683e74909a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:45 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 12 Oct 2021 02:25:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:53 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:53 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc03711acce0b5e2f3e2ad7249ce4962fdd520835a1c778de663b9f2bec5f309`  
		Last Modified: Tue, 12 Oct 2021 02:27:14 GMT  
		Size: 35.1 MB (35061492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ac3e7452691d4edc39f45e7e6706d3dcf06f188bb81aa96749fe12906f31bc`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef8988907a0a7be1f7d83a61d1aeaf02ef140108fff7f975c89339dd03e7848`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb9b5f2079e26ff03ed792915e6a981d31ea534399c82cf9eee4a529a07ae60`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.0-alpine`

```console
$ docker pull chronograf@sha256:bdb38dbf0d72892a4685b69391c89a1716a2465b0d52f79bd859a846f982c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:44ddcc13955fcee6ada98e17e24ee8f695a9823b3c3e999e5d315c9a3bb0aa8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22689227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86636178ef7f0961c639954f1607c343f7ed49e2749304818d81e8d9aaec58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:42 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Wed, 01 Sep 2021 00:24:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:50 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0062288c23918a5c405390da5fe197e453d3162f22d5e04c4e80c771bfb7dbb`  
		Last Modified: Wed, 01 Sep 2021 00:26:19 GMT  
		Size: 19.6 MB (19582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56af5fa9abf70534bf74916985c59602805aaec20e843a8fb80451dc2b4aa6b`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 12.3 KB (12269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad79cf9294c71cb171d84b1b435766c73b488c2eaf98668e8fb24c098ec8e0`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584912177323f577d098fda53486bc0f440c26efb41dd2951ee13af7a0f369`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:bdb38dbf0d72892a4685b69391c89a1716a2465b0d52f79bd859a846f982c702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:44ddcc13955fcee6ada98e17e24ee8f695a9823b3c3e999e5d315c9a3bb0aa8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22689227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86636178ef7f0961c639954f1607c343f7ed49e2749304818d81e8d9aaec58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 00:24:42 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Wed, 01 Sep 2021 00:24:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 01 Sep 2021 00:24:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 01 Sep 2021 00:24:50 GMT
EXPOSE 8888
# Wed, 01 Sep 2021 00:24:50 GMT
VOLUME [/var/lib/chronograf]
# Wed, 01 Sep 2021 00:24:51 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 01 Sep 2021 00:24:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 00:24:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0062288c23918a5c405390da5fe197e453d3162f22d5e04c4e80c771bfb7dbb`  
		Last Modified: Wed, 01 Sep 2021 00:26:19 GMT  
		Size: 19.6 MB (19582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56af5fa9abf70534bf74916985c59602805aaec20e843a8fb80451dc2b4aa6b`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 12.3 KB (12269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bad79cf9294c71cb171d84b1b435766c73b488c2eaf98668e8fb24c098ec8e0`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80584912177323f577d098fda53486bc0f440c26efb41dd2951ee13af7a0f369`  
		Last Modified: Wed, 01 Sep 2021 00:26:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:7c9afa8b840c273dd861a6122cea5bd076935949d88fd222a4f23dad3eb44d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:d7e1b83ef03cc2ada6ddb4262a9ef6141d69252b4229f9312022de422eba9628
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592c5727cec3ebc49e90e1a1db3158afe8ff3c4f974e2d823f94ed2de681d3b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:30 GMT
ADD file:c7a3b8a1e87bedfb6605855ad703321050112d02c9925ece42f4111d7a42cdd0 in / 
# Tue, 28 Sep 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:04:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 28 Sep 2021 02:05:50 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 28 Sep 2021 02:05:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Sep 2021 02:05:57 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 28 Sep 2021 02:05:57 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 28 Sep 2021 02:05:58 GMT
EXPOSE 8888
# Tue, 28 Sep 2021 02:05:58 GMT
VOLUME [/var/lib/chronograf]
# Tue, 28 Sep 2021 02:05:58 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 28 Sep 2021 02:05:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Sep 2021 02:05:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:36d925ed8e305498a951c3b56d100d153ae3babf046b88e2d00899105fe81c31`  
		Last Modified: Tue, 28 Sep 2021 01:32:51 GMT  
		Size: 22.5 MB (22527699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac1653626616a642c9b955388bec4fd6ccb341a84db6586a598c818bf9aec99`  
		Last Modified: Tue, 28 Sep 2021 02:06:27 GMT  
		Size: 6.8 MB (6760226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211fad620672de80aa2eb37b52a4a350fca5b115b59a0f29c453dbc33106c842`  
		Last Modified: Tue, 28 Sep 2021 02:07:16 GMT  
		Size: 37.4 MB (37444950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8b042071506815e237e7038debb7644e8651b62ae7f6eeee08cf3cc9f25dff`  
		Last Modified: Tue, 28 Sep 2021 02:07:12 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6813cf7b046ff4142fd4d0ba58ec4314368c6ff87a0f6a445a74c17954c68e`  
		Last Modified: Tue, 28 Sep 2021 02:07:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a88a250951fd04184933bd60acad8ee24297dc2caea606c9df00226ecc0cb2`  
		Last Modified: Tue, 28 Sep 2021 02:07:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1eaf9d54e80ec37220bf2e5c6772857401e611fa6e2974575ea238562e5eca8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60286017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3a0ed0ab3e2cf3af8f6c357383296fab4fc5a676f0dec7a7c3a9d6241605f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:16:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:19:09 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 01 Oct 2021 05:19:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:19:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:19:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:19:30 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:19:30 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:19:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:19:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:19:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746784bfad62d65116943e0e010a50702ae1fb03d897851e36ad6b7b9fb15f4f`  
		Last Modified: Fri, 01 Oct 2021 05:20:27 GMT  
		Size: 5.8 MB (5780591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f70d7dadcc587b01abb272b80cd64ba42d1e0d123c14ba94201cee1546f599f`  
		Last Modified: Fri, 01 Oct 2021 05:22:08 GMT  
		Size: 35.2 MB (35164577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e81f2620fb3a78dd449c871aa0dffb8d612270c0e4926e70bd9a4ac20d22872`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76af3bdd08d13774a02d1879f55bd572d8fef6cce9f936f0a5457bd76d04986`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf79df797875a5efea73a0584f057cd1ec273b5e125195997c57e405c247186`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f8b10eabd6a93f7fcbc8d8acce2b60e412754a07bb95664a8b3caa800ca21c38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc16a9b86e7c3cd6838f8aae38c005ab4d37fd1595c576151580683e74909a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:45 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 12 Oct 2021 02:25:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:53 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:53 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc03711acce0b5e2f3e2ad7249ce4962fdd520835a1c778de663b9f2bec5f309`  
		Last Modified: Tue, 12 Oct 2021 02:27:14 GMT  
		Size: 35.1 MB (35061492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ac3e7452691d4edc39f45e7e6706d3dcf06f188bb81aa96749fe12906f31bc`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef8988907a0a7be1f7d83a61d1aeaf02ef140108fff7f975c89339dd03e7848`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb9b5f2079e26ff03ed792915e6a981d31ea534399c82cf9eee4a529a07ae60`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
