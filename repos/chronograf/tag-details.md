<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.2`](#chronograf1102)
-	[`chronograf:1.10.2-alpine`](#chronograf1102-alpine)
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
$ docker pull chronograf@sha256:b9c52b548066f3b4ed876dcb3e5f0a652548dd41cc7e7f2f42c3700dd29eab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:04462ac26b7dbe7a416cce7de3b7cb3f980b2902a3b0ea0945b2b48574b8c61d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84071849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba864730ae6dd40df4e4518818953064d84a262247c361f41dd3c4696b995db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:37:30 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 01:37:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:37:37 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:37:37 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:37:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4699424b1273b826b5cdc341e3b641e4677c94540188c99dbfe6107f04b338`  
		Last Modified: Tue, 13 Feb 2024 01:38:40 GMT  
		Size: 7.9 MB (7870359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdf86bc6e62c35c39e6459d906c2630014debc2e98d324647a464bbebf11e69`  
		Last Modified: Tue, 13 Feb 2024 01:38:45 GMT  
		Size: 47.1 MB (47053015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212a2b45925a777bacea28fb46859ff3c9d814027aa8c86354e32ff87ea2909`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2998c8c8e76f333407adb69b20a7daf0d2eda63ff22da8b98eb2e40f0ace65d`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a23ee363789d93f633ec5fd788469b8fd511b4832198e334f0cf1a4ea393a1b`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:164f96a54a6789a5d6d7a24c9f4b99b9ab6923c70cd5bf272fa5249ba2f804cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75885126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5ae27c0d2625e913fa8e6302b205402c5df1e6dd6b4c5ed3f8bda8030293cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 02:51:56 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 02:52:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:52:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 02:52:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 02:52:11 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 02:52:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 02:52:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 02:52:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fa9249853ada1b6b31f64fba359a34bef386b24491b6f80cd43c735b0ebd35`  
		Last Modified: Tue, 13 Feb 2024 02:53:12 GMT  
		Size: 6.5 MB (6494977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a9c5f20d623828e8c0cd47e752d2442b46028e7c104a9b3d49735da99d20e6`  
		Last Modified: Tue, 13 Feb 2024 02:53:19 GMT  
		Size: 44.6 MB (44649109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0fe2869b4515f458397b229257482fb87e4d54de15183499e91fbef9c9cec8`  
		Last Modified: Tue, 13 Feb 2024 02:53:10 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e397a95fb4e32746ad1943d95189aee536299d523974be91c03658c3c9cb7b12`  
		Last Modified: Tue, 13 Feb 2024 02:53:10 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93685ee3caaebd7a2349d57a759e12e6dfe4674e7f1d6d19cefb2dae559cbfc5`  
		Last Modified: Tue, 13 Feb 2024 02:53:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5d8d80646010cfe6875f70f0305283c4ecf410af01669a7739bbb99f6ab4d71c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81601411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ea9755b59d1150652ef5cf7cf8d8fcb4e8d418288516d3ba6d9b18a3a00b5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:52:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:52:22 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 01:52:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:52:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:52:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:52:28 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:52:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:52:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:52:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:52:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8356d255d957337b3271ca2ccb409831d13fb862aa8674a62d51e2a0cf121c5`  
		Last Modified: Tue, 13 Feb 2024 01:53:15 GMT  
		Size: 7.6 MB (7647144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae248ef7539fbb6f443297ba9bd3c53a1fc193086a6befe57cf3165c6eee1f5`  
		Last Modified: Tue, 13 Feb 2024 01:53:19 GMT  
		Size: 44.8 MB (44773513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b1b3905f9f2f89ae89d40f805eaaffd9b634c0bdbd3e9dfdb75ae53737a4bb`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0252bd3162130e739e5cabd7d9e9bea09a6b3ef32210f0103dbd7be761759e0d`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7a271221e0ffe0f48af65b288d14a19ab326cfcf5088ab1fda68f49415702c`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:7504f4ab2f4887539ce3d2c909f1ca6408d80195628832eea63877f69a2523b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7c778533d522ed28a95e32c4ee03548ffb53da4a86622d809be58448be6b917f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31559565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde71584b4fc8d5b5e38c218fada6f2ad411de8c7696cdf339ca84620205f4d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:11:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:41:06 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Sat, 27 Jan 2024 03:41:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:41:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 27 Jan 2024 03:41:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 27 Jan 2024 03:41:12 GMT
EXPOSE 8888
# Sat, 27 Jan 2024 03:41:12 GMT
VOLUME [/var/lib/chronograf]
# Sat, 27 Jan 2024 03:41:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:41:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:41:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24534ed772762b2bbf09082d1b3308d3f8c7dccd367ecbd54b5c74c15eeafde`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 284.7 KB (284696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c624949424b9846e8fde3d2631c54bb17d01a5ae3d1deb66cae28461a9216573`  
		Last Modified: Sat, 27 Jan 2024 03:42:13 GMT  
		Size: 27.8 MB (27847643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c293158dc305d0ec9786dea2382423ceedd941090dfb8a1bfeaf2561027c7450`  
		Last Modified: Sat, 27 Jan 2024 03:42:08 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31183b1bef5ed3811386cde8b8e41ed9471882c7b5e863a54aa3b5971834bf85`  
		Last Modified: Sat, 27 Jan 2024 03:42:08 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7580a090490b5fa9251ae3de9349440c555d2055c48af8983fffc2abb1d4bf`  
		Last Modified: Sat, 27 Jan 2024 03:42:08 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.2`

```console
$ docker pull chronograf@sha256:b9c52b548066f3b4ed876dcb3e5f0a652548dd41cc7e7f2f42c3700dd29eab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.2` - linux; amd64

```console
$ docker pull chronograf@sha256:04462ac26b7dbe7a416cce7de3b7cb3f980b2902a3b0ea0945b2b48574b8c61d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84071849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba864730ae6dd40df4e4518818953064d84a262247c361f41dd3c4696b995db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:37:30 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 01:37:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:37:37 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:37:37 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:37:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4699424b1273b826b5cdc341e3b641e4677c94540188c99dbfe6107f04b338`  
		Last Modified: Tue, 13 Feb 2024 01:38:40 GMT  
		Size: 7.9 MB (7870359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdf86bc6e62c35c39e6459d906c2630014debc2e98d324647a464bbebf11e69`  
		Last Modified: Tue, 13 Feb 2024 01:38:45 GMT  
		Size: 47.1 MB (47053015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212a2b45925a777bacea28fb46859ff3c9d814027aa8c86354e32ff87ea2909`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2998c8c8e76f333407adb69b20a7daf0d2eda63ff22da8b98eb2e40f0ace65d`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a23ee363789d93f633ec5fd788469b8fd511b4832198e334f0cf1a4ea393a1b`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:164f96a54a6789a5d6d7a24c9f4b99b9ab6923c70cd5bf272fa5249ba2f804cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75885126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5ae27c0d2625e913fa8e6302b205402c5df1e6dd6b4c5ed3f8bda8030293cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 02:51:56 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 02:52:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:52:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 02:52:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 02:52:11 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 02:52:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 02:52:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 02:52:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fa9249853ada1b6b31f64fba359a34bef386b24491b6f80cd43c735b0ebd35`  
		Last Modified: Tue, 13 Feb 2024 02:53:12 GMT  
		Size: 6.5 MB (6494977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a9c5f20d623828e8c0cd47e752d2442b46028e7c104a9b3d49735da99d20e6`  
		Last Modified: Tue, 13 Feb 2024 02:53:19 GMT  
		Size: 44.6 MB (44649109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0fe2869b4515f458397b229257482fb87e4d54de15183499e91fbef9c9cec8`  
		Last Modified: Tue, 13 Feb 2024 02:53:10 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e397a95fb4e32746ad1943d95189aee536299d523974be91c03658c3c9cb7b12`  
		Last Modified: Tue, 13 Feb 2024 02:53:10 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93685ee3caaebd7a2349d57a759e12e6dfe4674e7f1d6d19cefb2dae559cbfc5`  
		Last Modified: Tue, 13 Feb 2024 02:53:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5d8d80646010cfe6875f70f0305283c4ecf410af01669a7739bbb99f6ab4d71c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81601411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ea9755b59d1150652ef5cf7cf8d8fcb4e8d418288516d3ba6d9b18a3a00b5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:52:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:52:22 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 01:52:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:52:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:52:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:52:28 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:52:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:52:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:52:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:52:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8356d255d957337b3271ca2ccb409831d13fb862aa8674a62d51e2a0cf121c5`  
		Last Modified: Tue, 13 Feb 2024 01:53:15 GMT  
		Size: 7.6 MB (7647144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae248ef7539fbb6f443297ba9bd3c53a1fc193086a6befe57cf3165c6eee1f5`  
		Last Modified: Tue, 13 Feb 2024 01:53:19 GMT  
		Size: 44.8 MB (44773513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b1b3905f9f2f89ae89d40f805eaaffd9b634c0bdbd3e9dfdb75ae53737a4bb`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0252bd3162130e739e5cabd7d9e9bea09a6b3ef32210f0103dbd7be761759e0d`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7a271221e0ffe0f48af65b288d14a19ab326cfcf5088ab1fda68f49415702c`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.2-alpine`

```console
$ docker pull chronograf@sha256:7504f4ab2f4887539ce3d2c909f1ca6408d80195628832eea63877f69a2523b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7c778533d522ed28a95e32c4ee03548ffb53da4a86622d809be58448be6b917f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31559565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde71584b4fc8d5b5e38c218fada6f2ad411de8c7696cdf339ca84620205f4d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:11:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:41:06 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Sat, 27 Jan 2024 03:41:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:41:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 27 Jan 2024 03:41:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 27 Jan 2024 03:41:12 GMT
EXPOSE 8888
# Sat, 27 Jan 2024 03:41:12 GMT
VOLUME [/var/lib/chronograf]
# Sat, 27 Jan 2024 03:41:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:41:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:41:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24534ed772762b2bbf09082d1b3308d3f8c7dccd367ecbd54b5c74c15eeafde`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 284.7 KB (284696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c624949424b9846e8fde3d2631c54bb17d01a5ae3d1deb66cae28461a9216573`  
		Last Modified: Sat, 27 Jan 2024 03:42:13 GMT  
		Size: 27.8 MB (27847643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c293158dc305d0ec9786dea2382423ceedd941090dfb8a1bfeaf2561027c7450`  
		Last Modified: Sat, 27 Jan 2024 03:42:08 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31183b1bef5ed3811386cde8b8e41ed9471882c7b5e863a54aa3b5971834bf85`  
		Last Modified: Sat, 27 Jan 2024 03:42:08 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7580a090490b5fa9251ae3de9349440c555d2055c48af8983fffc2abb1d4bf`  
		Last Modified: Sat, 27 Jan 2024 03:42:08 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:fa8c940cde4e46f18224fd186a9db15e21f2dc3b921e595f4ca7ff9ed8ca5045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:39526efe16c3fcb25c0741157a779b78dd1e6175bb1d4088bc39076907523a2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70601706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1467f66e48aefe950487656191a7627da12751287129d2c31002b804d9d138f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:36:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:36:33 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Feb 2024 01:36:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:36:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:36:41 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:36:41 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:36:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:36:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:36:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:36:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65125b5447fdda5aec7b275007074f6c5a66f4912dcc04a39bacb6935349fa93`  
		Last Modified: Tue, 13 Feb 2024 01:37:57 GMT  
		Size: 4.4 MB (4416535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf0cfbd70159d3096719056760fb6472c9af8e0b393b3872c86b98816e3d500`  
		Last Modified: Tue, 13 Feb 2024 01:38:01 GMT  
		Size: 34.7 MB (34738356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eafcd6a5ee702125ec390ecfad592be2d67c7bf7b583f3c431cb0c83bb24f3`  
		Last Modified: Tue, 13 Feb 2024 01:37:56 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2919874de093e410058c166c851f90b76ec6e494ac4d23b15d26ddb1a74aa0b9`  
		Last Modified: Tue, 13 Feb 2024 01:37:56 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d307e820f836aaf2a35beac9fdc29d44673b71ffc96e2e08061209de03334ba7`  
		Last Modified: Tue, 13 Feb 2024 01:37:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e63cf548dde5ab108d416cf8c2bb0943634666fbd0168848cd215f1bf1a62862
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63424600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa40f7cb000168a0de7a3b47f34214c662574a6618c9e1f7feed05b893d0ce5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:39 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
# Tue, 13 Feb 2024 01:20:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:50:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 02:50:07 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Feb 2024 02:50:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:50:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 02:50:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 02:50:25 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 02:50:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 02:50:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 02:50:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:50:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775286c6c22a94f34e5a6dfd0a21a9d715fe1acb165465535ac1cbe1ddbbbdf`  
		Last Modified: Tue, 13 Feb 2024 02:52:30 GMT  
		Size: 3.7 MB (3719070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca47a211c563b9718e4db3c34c5f8409a6aa12fbcd10478c24324fff1a21bec`  
		Last Modified: Tue, 13 Feb 2024 02:52:35 GMT  
		Size: 33.1 MB (33098476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c512088d564674aa1c3a57e49cab824c7e54e90c89433c7649f5ddc869b773c`  
		Last Modified: Tue, 13 Feb 2024 02:52:29 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af8bf2bbc48218ba3aafe9771baa067561fdd0459cf1f03f2c4211a9f6fdc7e`  
		Last Modified: Tue, 13 Feb 2024 02:52:29 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8202e28b3fe0c175b6a0c4946e16a13e068e5b18b5576ad6b6f9cbfda04d33`  
		Last Modified: Tue, 13 Feb 2024 02:52:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e042c48d2a2862c66e08d7c1ca7b4c0698769059a56d4cff5ec892742bd15330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67752248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef613abc69f8df2a747cb20c36ece799989c0fe2efee3db71373bfd54a73b15e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:51:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:51:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Feb 2024 01:51:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:51:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:51:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:51:47 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:51:47 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:51:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:51:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ab9c9af9c41bcf1d08056bed60455d63ae9b54ff539d85c435d220c22d56ff`  
		Last Modified: Tue, 13 Feb 2024 01:52:40 GMT  
		Size: 4.4 MB (4418028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325e790ad2925dbf8fdf966f8bb432883afa0c52a3a4575b270dae5a8b122b63`  
		Last Modified: Tue, 13 Feb 2024 01:52:42 GMT  
		Size: 33.2 MB (33238753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf0d32b8f796de6dc2024bbe741ab23b550469f52e0a1196cc842d93a425f1e`  
		Last Modified: Tue, 13 Feb 2024 01:52:39 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3d3dd2a8764b539aeae0304d40aad7f29d7cfd0b2d91fa6037bff203c4808b`  
		Last Modified: Tue, 13 Feb 2024 01:52:39 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df04474168f76014010a3f11d786018a36593128451b601fa0beffe357aa703`  
		Last Modified: Tue, 13 Feb 2024 01:52:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:c64bcb7e5e2b3b7fa24d9fccb683026c1c36199bea2ca418bdb6645d867a4f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:33758f71250128d11acd954622e8a71508f91b95cbec7627ecb1340217d7f878
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23246234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0d6423ef66d78f1a7fb1fa046655619f2e3a3de707ac48ae05070f2e20b97f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:40:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:40:29 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 27 Jan 2024 03:40:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:40:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 27 Jan 2024 03:40:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 27 Jan 2024 03:40:34 GMT
EXPOSE 8888
# Sat, 27 Jan 2024 03:40:34 GMT
VOLUME [/var/lib/chronograf]
# Sat, 27 Jan 2024 03:40:35 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:40:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:40:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a894b23b9ee924163e7f06389bd22fa5039c489dc5e4b1a2d2867971d69c0b`  
		Last Modified: Sat, 27 Jan 2024 03:41:29 GMT  
		Size: 284.9 KB (284934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16952c7f7187deea3c412a07fbb07a9f2aa917913aef6139d3a3518160ebc32`  
		Last Modified: Sat, 27 Jan 2024 03:41:32 GMT  
		Size: 19.6 MB (19557214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa83367bcdd0bf4575e355bdaa80bc2c8d764a76c5904cb82655613690258bb`  
		Last Modified: Sat, 27 Jan 2024 03:41:29 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d3ff0289b08182682ab811730549fef5be511560cee6ef28ccc6436a6cde55`  
		Last Modified: Sat, 27 Jan 2024 03:41:28 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a64a7235117d6c095dcc0288ee4be0ff14e0794e8b0396a0010d6780ced6a76`  
		Last Modified: Sat, 27 Jan 2024 03:41:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:fa8c940cde4e46f18224fd186a9db15e21f2dc3b921e595f4ca7ff9ed8ca5045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:39526efe16c3fcb25c0741157a779b78dd1e6175bb1d4088bc39076907523a2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70601706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1467f66e48aefe950487656191a7627da12751287129d2c31002b804d9d138f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:36:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:36:33 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Feb 2024 01:36:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:36:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:36:41 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:36:41 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:36:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:36:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:36:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:36:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65125b5447fdda5aec7b275007074f6c5a66f4912dcc04a39bacb6935349fa93`  
		Last Modified: Tue, 13 Feb 2024 01:37:57 GMT  
		Size: 4.4 MB (4416535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf0cfbd70159d3096719056760fb6472c9af8e0b393b3872c86b98816e3d500`  
		Last Modified: Tue, 13 Feb 2024 01:38:01 GMT  
		Size: 34.7 MB (34738356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eafcd6a5ee702125ec390ecfad592be2d67c7bf7b583f3c431cb0c83bb24f3`  
		Last Modified: Tue, 13 Feb 2024 01:37:56 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2919874de093e410058c166c851f90b76ec6e494ac4d23b15d26ddb1a74aa0b9`  
		Last Modified: Tue, 13 Feb 2024 01:37:56 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d307e820f836aaf2a35beac9fdc29d44673b71ffc96e2e08061209de03334ba7`  
		Last Modified: Tue, 13 Feb 2024 01:37:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e63cf548dde5ab108d416cf8c2bb0943634666fbd0168848cd215f1bf1a62862
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63424600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa40f7cb000168a0de7a3b47f34214c662574a6618c9e1f7feed05b893d0ce5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:39 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
# Tue, 13 Feb 2024 01:20:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:50:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 02:50:07 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Feb 2024 02:50:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:50:24 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 02:50:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 02:50:25 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 02:50:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 02:50:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 02:50:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:50:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775286c6c22a94f34e5a6dfd0a21a9d715fe1acb165465535ac1cbe1ddbbbdf`  
		Last Modified: Tue, 13 Feb 2024 02:52:30 GMT  
		Size: 3.7 MB (3719070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca47a211c563b9718e4db3c34c5f8409a6aa12fbcd10478c24324fff1a21bec`  
		Last Modified: Tue, 13 Feb 2024 02:52:35 GMT  
		Size: 33.1 MB (33098476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c512088d564674aa1c3a57e49cab824c7e54e90c89433c7649f5ddc869b773c`  
		Last Modified: Tue, 13 Feb 2024 02:52:29 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af8bf2bbc48218ba3aafe9771baa067561fdd0459cf1f03f2c4211a9f6fdc7e`  
		Last Modified: Tue, 13 Feb 2024 02:52:29 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8202e28b3fe0c175b6a0c4946e16a13e068e5b18b5576ad6b6f9cbfda04d33`  
		Last Modified: Tue, 13 Feb 2024 02:52:29 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e042c48d2a2862c66e08d7c1ca7b4c0698769059a56d4cff5ec892742bd15330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67752248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef613abc69f8df2a747cb20c36ece799989c0fe2efee3db71373bfd54a73b15e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:51:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:51:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 13 Feb 2024 01:51:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:51:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:51:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:51:47 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:51:47 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:51:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:51:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ab9c9af9c41bcf1d08056bed60455d63ae9b54ff539d85c435d220c22d56ff`  
		Last Modified: Tue, 13 Feb 2024 01:52:40 GMT  
		Size: 4.4 MB (4418028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325e790ad2925dbf8fdf966f8bb432883afa0c52a3a4575b270dae5a8b122b63`  
		Last Modified: Tue, 13 Feb 2024 01:52:42 GMT  
		Size: 33.2 MB (33238753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf0d32b8f796de6dc2024bbe741ab23b550469f52e0a1196cc842d93a425f1e`  
		Last Modified: Tue, 13 Feb 2024 01:52:39 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3d3dd2a8764b539aeae0304d40aad7f29d7cfd0b2d91fa6037bff203c4808b`  
		Last Modified: Tue, 13 Feb 2024 01:52:39 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df04474168f76014010a3f11d786018a36593128451b601fa0beffe357aa703`  
		Last Modified: Tue, 13 Feb 2024 01:52:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:c64bcb7e5e2b3b7fa24d9fccb683026c1c36199bea2ca418bdb6645d867a4f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:33758f71250128d11acd954622e8a71508f91b95cbec7627ecb1340217d7f878
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23246234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0d6423ef66d78f1a7fb1fa046655619f2e3a3de707ac48ae05070f2e20b97f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:40:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:40:29 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 27 Jan 2024 03:40:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:40:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 27 Jan 2024 03:40:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 27 Jan 2024 03:40:34 GMT
EXPOSE 8888
# Sat, 27 Jan 2024 03:40:34 GMT
VOLUME [/var/lib/chronograf]
# Sat, 27 Jan 2024 03:40:35 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:40:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:40:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a894b23b9ee924163e7f06389bd22fa5039c489dc5e4b1a2d2867971d69c0b`  
		Last Modified: Sat, 27 Jan 2024 03:41:29 GMT  
		Size: 284.9 KB (284934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16952c7f7187deea3c412a07fbb07a9f2aa917913aef6139d3a3518160ebc32`  
		Last Modified: Sat, 27 Jan 2024 03:41:32 GMT  
		Size: 19.6 MB (19557214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa83367bcdd0bf4575e355bdaa80bc2c8d764a76c5904cb82655613690258bb`  
		Last Modified: Sat, 27 Jan 2024 03:41:29 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d3ff0289b08182682ab811730549fef5be511560cee6ef28ccc6436a6cde55`  
		Last Modified: Sat, 27 Jan 2024 03:41:28 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a64a7235117d6c095dcc0288ee4be0ff14e0794e8b0396a0010d6780ced6a76`  
		Last Modified: Sat, 27 Jan 2024 03:41:28 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:e9824622427124d4051c6a38692c4a9f06c1e0ef1e767a1e15e9eb65e78b9e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:189c410ef0bb18bf3a9449bf3e5249f4fa745d31c1355e350c979a05d3a0ab0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71253281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030a23451e1ff832a3d8ecacd307baaacff4fc00b3ca562734597bce74095d63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:36:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:36:53 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Feb 2024 01:37:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:37:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:37:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:37:01 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:37:01 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:37:01 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:37:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:37:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829c083c75eadd589b8a8f8cb16916104c86b6e3e076638ad223d9a2750ee5e0`  
		Last Modified: Tue, 13 Feb 2024 01:38:13 GMT  
		Size: 5.2 MB (5226443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fc1f36edcd0cb05696b42922389a0e68912489da60dc6fa27d14d8da8e9244`  
		Last Modified: Tue, 13 Feb 2024 01:38:17 GMT  
		Size: 34.6 MB (34580022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9356772e4fe7b3655dd50ac36f134bf3ec5121fd419b918734881dc968abe9`  
		Last Modified: Tue, 13 Feb 2024 01:38:12 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99168f3b0cbf07f1c116e528015e3bcb50ff99c43dcaf350f76cab247a2f88d0`  
		Last Modified: Tue, 13 Feb 2024 01:38:13 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396836d5520b73a68bdf1159e5543396ef9860a82a41563c2d24a974b6d52528`  
		Last Modified: Tue, 13 Feb 2024 01:38:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:25d8b09702515ef6acead5c48cecf056cb2198a9fe3f85615ce68bae18394a26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63850389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f657e4cc8c047219eb74c6aa18c78529b21ad4e585ab81f8b12de8285191e3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:39 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
# Tue, 13 Feb 2024 01:20:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:50:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 02:50:49 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Feb 2024 02:51:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:51:04 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 02:51:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 02:51:05 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 02:51:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 02:51:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 02:51:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:51:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb23410a5056fcfb050496c0f367867389448c109176e03309e7bf04864e81f`  
		Last Modified: Tue, 13 Feb 2024 02:52:44 GMT  
		Size: 4.5 MB (4492081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e703b3a3f0dd32c4e14dbcb272aaf2e7e333fb075e9f21c193345919dd27f6b3`  
		Last Modified: Tue, 13 Feb 2024 02:52:48 GMT  
		Size: 32.8 MB (32751249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd4e985201fcfa4e81003134462159af58976fefe46e4adad02e32c267f881a`  
		Last Modified: Tue, 13 Feb 2024 02:52:43 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba51f2345b221c034f2e89b17f9d75be39f7520c8cabb2bb1442743690b162f`  
		Last Modified: Tue, 13 Feb 2024 02:52:43 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ca7bd83998757244273c53f0c4a62144a5ca52085136a07ed09957decde569`  
		Last Modified: Tue, 13 Feb 2024 02:52:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8b6efaf2a0b75ef6a509c91c12a35dabb934d4512d8419057416f8f8f2f31c32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67950265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2847f110ec0e3807b8c6dce909ad3f8609f8e12cbf19bca95b69c4ee746b86c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:51:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:51:57 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Feb 2024 01:52:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:52:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:52:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:52:03 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:52:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:52:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:52:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:52:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf6a957e22a2a9e121959314e020c66ccdb2b7d3efe6cef87e93651b691c512`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 5.2 MB (5209567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fd5bbb7466349998e2cbb4540b3b104c104f1fa25a51e5e6459aec676fda63`  
		Last Modified: Tue, 13 Feb 2024 01:52:55 GMT  
		Size: 32.6 MB (32645228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b6cf5521416c46bd2f2ab21a59e11332ac18a98a0395a97b2e791007dfcb67`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba65d21f7f7ddc8e4a72384602c692463b083befd81e4ea3be2a6b1acc46666`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c9c68228aa5dabc190f0ffe97edbd6a036034d0f9dbbf69be5d0e50acbbb6d`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:9b5352a49781044ac0c7a2b604070f8faf23a0c19cf02c098e16d623cea7038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:476eae2a459f2030b6f4138845d5cfaa9b1af70692220ce0742a4264b8978cc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22893185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc7bde13275acbdb5a6fb1fffc636c9391b5d06fde6325018730c2b739fe2f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:40:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:40:40 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 27 Jan 2024 03:40:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:40:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 27 Jan 2024 03:40:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 27 Jan 2024 03:40:49 GMT
EXPOSE 8888
# Sat, 27 Jan 2024 03:40:49 GMT
VOLUME [/var/lib/chronograf]
# Sat, 27 Jan 2024 03:40:50 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:40:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:40:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a894b23b9ee924163e7f06389bd22fa5039c489dc5e4b1a2d2867971d69c0b`  
		Last Modified: Sat, 27 Jan 2024 03:41:29 GMT  
		Size: 284.9 KB (284934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad66235d9f4da152cfd7441e1746d163c33e8cf6e59110ea18c474dba3a54e32`  
		Last Modified: Sat, 27 Jan 2024 03:41:44 GMT  
		Size: 19.2 MB (19204185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664f567d3fb106241f2304028168250d0364a33a6e2035fbe89b6085e06f001e`  
		Last Modified: Sat, 27 Jan 2024 03:41:41 GMT  
		Size: 12.3 KB (12258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0369ec23601ebf6d3a3de51e9cb140e4ab7f98816aaa1377f19b9c11755f86bb`  
		Last Modified: Sat, 27 Jan 2024 03:41:41 GMT  
		Size: 11.9 KB (11890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c3651064a54f438188f1bd4857d3cfd66b2601283107b4ea1f5811ff82f7e6`  
		Last Modified: Sat, 27 Jan 2024 03:41:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:e9824622427124d4051c6a38692c4a9f06c1e0ef1e767a1e15e9eb65e78b9e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:189c410ef0bb18bf3a9449bf3e5249f4fa745d31c1355e350c979a05d3a0ab0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71253281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030a23451e1ff832a3d8ecacd307baaacff4fc00b3ca562734597bce74095d63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:36:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:36:53 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Feb 2024 01:37:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:37:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:37:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:37:01 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:37:01 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:37:01 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:37:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:37:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829c083c75eadd589b8a8f8cb16916104c86b6e3e076638ad223d9a2750ee5e0`  
		Last Modified: Tue, 13 Feb 2024 01:38:13 GMT  
		Size: 5.2 MB (5226443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fc1f36edcd0cb05696b42922389a0e68912489da60dc6fa27d14d8da8e9244`  
		Last Modified: Tue, 13 Feb 2024 01:38:17 GMT  
		Size: 34.6 MB (34580022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9356772e4fe7b3655dd50ac36f134bf3ec5121fd419b918734881dc968abe9`  
		Last Modified: Tue, 13 Feb 2024 01:38:12 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99168f3b0cbf07f1c116e528015e3bcb50ff99c43dcaf350f76cab247a2f88d0`  
		Last Modified: Tue, 13 Feb 2024 01:38:13 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396836d5520b73a68bdf1159e5543396ef9860a82a41563c2d24a974b6d52528`  
		Last Modified: Tue, 13 Feb 2024 01:38:12 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:25d8b09702515ef6acead5c48cecf056cb2198a9fe3f85615ce68bae18394a26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63850389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f657e4cc8c047219eb74c6aa18c78529b21ad4e585ab81f8b12de8285191e3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:39 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
# Tue, 13 Feb 2024 01:20:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:50:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 02:50:49 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Feb 2024 02:51:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:51:04 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 02:51:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 02:51:05 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 02:51:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 02:51:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 02:51:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:51:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb23410a5056fcfb050496c0f367867389448c109176e03309e7bf04864e81f`  
		Last Modified: Tue, 13 Feb 2024 02:52:44 GMT  
		Size: 4.5 MB (4492081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e703b3a3f0dd32c4e14dbcb272aaf2e7e333fb075e9f21c193345919dd27f6b3`  
		Last Modified: Tue, 13 Feb 2024 02:52:48 GMT  
		Size: 32.8 MB (32751249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd4e985201fcfa4e81003134462159af58976fefe46e4adad02e32c267f881a`  
		Last Modified: Tue, 13 Feb 2024 02:52:43 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba51f2345b221c034f2e89b17f9d75be39f7520c8cabb2bb1442743690b162f`  
		Last Modified: Tue, 13 Feb 2024 02:52:43 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ca7bd83998757244273c53f0c4a62144a5ca52085136a07ed09957decde569`  
		Last Modified: Tue, 13 Feb 2024 02:52:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8b6efaf2a0b75ef6a509c91c12a35dabb934d4512d8419057416f8f8f2f31c32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67950265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2847f110ec0e3807b8c6dce909ad3f8609f8e12cbf19bca95b69c4ee746b86c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:51:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:51:57 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 13 Feb 2024 01:52:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:52:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:52:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:52:03 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:52:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:52:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:52:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:52:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf6a957e22a2a9e121959314e020c66ccdb2b7d3efe6cef87e93651b691c512`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 5.2 MB (5209567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fd5bbb7466349998e2cbb4540b3b104c104f1fa25a51e5e6459aec676fda63`  
		Last Modified: Tue, 13 Feb 2024 01:52:55 GMT  
		Size: 32.6 MB (32645228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b6cf5521416c46bd2f2ab21a59e11332ac18a98a0395a97b2e791007dfcb67`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba65d21f7f7ddc8e4a72384602c692463b083befd81e4ea3be2a6b1acc46666`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c9c68228aa5dabc190f0ffe97edbd6a036034d0f9dbbf69be5d0e50acbbb6d`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:9b5352a49781044ac0c7a2b604070f8faf23a0c19cf02c098e16d623cea7038d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:476eae2a459f2030b6f4138845d5cfaa9b1af70692220ce0742a4264b8978cc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22893185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc7bde13275acbdb5a6fb1fffc636c9391b5d06fde6325018730c2b739fe2f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:40:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:40:40 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 27 Jan 2024 03:40:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:40:49 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 27 Jan 2024 03:40:49 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 27 Jan 2024 03:40:49 GMT
EXPOSE 8888
# Sat, 27 Jan 2024 03:40:49 GMT
VOLUME [/var/lib/chronograf]
# Sat, 27 Jan 2024 03:40:50 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:40:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:40:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a894b23b9ee924163e7f06389bd22fa5039c489dc5e4b1a2d2867971d69c0b`  
		Last Modified: Sat, 27 Jan 2024 03:41:29 GMT  
		Size: 284.9 KB (284934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad66235d9f4da152cfd7441e1746d163c33e8cf6e59110ea18c474dba3a54e32`  
		Last Modified: Sat, 27 Jan 2024 03:41:44 GMT  
		Size: 19.2 MB (19204185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664f567d3fb106241f2304028168250d0364a33a6e2035fbe89b6085e06f001e`  
		Last Modified: Sat, 27 Jan 2024 03:41:41 GMT  
		Size: 12.3 KB (12258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0369ec23601ebf6d3a3de51e9cb140e4ab7f98816aaa1377f19b9c11755f86bb`  
		Last Modified: Sat, 27 Jan 2024 03:41:41 GMT  
		Size: 11.9 KB (11890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c3651064a54f438188f1bd4857d3cfd66b2601283107b4ea1f5811ff82f7e6`  
		Last Modified: Sat, 27 Jan 2024 03:41:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:6d0ad66bf4af83cd75bd432858df696986d5d2f6e8edc2a1195b975c79e49607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:55c5656d179a5668cab8c253f7e23409cf821aa06bfbd69b8b1eb472527defd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71900605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814b72987a56bb71eed31a1e50a118ca20f5a0e01d190f060fb8848666dacee8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:36:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:37:09 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Feb 2024 01:37:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:37:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:37:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:37:15 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:37:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:37:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:37:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:37:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829c083c75eadd589b8a8f8cb16916104c86b6e3e076638ad223d9a2750ee5e0`  
		Last Modified: Tue, 13 Feb 2024 01:38:13 GMT  
		Size: 5.2 MB (5226443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bc51c64815f927f26ca986defeb6d256569a94c253a1ab42ef9ccf7b30fa41`  
		Last Modified: Tue, 13 Feb 2024 01:38:30 GMT  
		Size: 35.2 MB (35227350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1749187b30e6d96e2d26dab919ecdb931c4a03c857062726b7c88b6b1bcaef81`  
		Last Modified: Tue, 13 Feb 2024 01:38:26 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4aef0e5ec6c76655fedfc0589c830735fc9511f4e115fc42d5c5173d8fb9b3`  
		Last Modified: Tue, 13 Feb 2024 01:38:26 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30920e15d63b562afaa448f4e5f6c2d484f2083160390fe15aa8fa38e262d13`  
		Last Modified: Tue, 13 Feb 2024 01:38:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d06445556baf391e3cf01ed00c4fbca94c2c7b741e73d39d8a9b25c404e18a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64626592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101c617c36e9847a07fd70cda5f670cc9b775b0dbbf81dcfe0bc49813ab8b12b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:39 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
# Tue, 13 Feb 2024 01:20:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:50:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 02:51:13 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Feb 2024 02:51:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:51:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 02:51:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 02:51:25 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 02:51:26 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 02:51:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 02:51:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:51:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb23410a5056fcfb050496c0f367867389448c109176e03309e7bf04864e81f`  
		Last Modified: Tue, 13 Feb 2024 02:52:44 GMT  
		Size: 4.5 MB (4492081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a662ef22fde244eb0cf627a3d0525298cfcd7bfa3e4ef06ed31e2d3a412f7798`  
		Last Modified: Tue, 13 Feb 2024 02:53:02 GMT  
		Size: 33.5 MB (33527454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042f6eeb4943dffe35692eb3882087579bca6106aefb98f03cec15981cfcea2`  
		Last Modified: Tue, 13 Feb 2024 02:52:56 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b70aa65193e2cb4dbb9147b153170203a6c8edad8b42f3a02ae7e67ba08079`  
		Last Modified: Tue, 13 Feb 2024 02:52:56 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1493008008f22b4a3971a4dd0b7418d799563c6dd2662b1a689edb8ceee7af`  
		Last Modified: Tue, 13 Feb 2024 02:52:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:72c10e7455c8d8c38c8dffb82a88f4d69ca967929ea582abdc0546d639cd9511
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68702509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4549529266df145ee04e0de318fc8ace233c49903dc2f32143d4d5f33f3487`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:51:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:52:07 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Feb 2024 01:52:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:52:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:52:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:52:13 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:52:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:52:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:52:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:52:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf6a957e22a2a9e121959314e020c66ccdb2b7d3efe6cef87e93651b691c512`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 5.2 MB (5209567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549bc8d63fe6887e7928e7d81e3e42ca8b6aeed882f6f1e59b54fd290c814c3d`  
		Last Modified: Tue, 13 Feb 2024 01:53:06 GMT  
		Size: 33.4 MB (33397475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a093f735a216bd69e0d1118cd3930cd06753476673b3113ace1a4e429ba4e298`  
		Last Modified: Tue, 13 Feb 2024 01:53:03 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42532c7431b4ca8c188c2800c2bc490ae82e99e7ea5bf838abc021c64c67f3b2`  
		Last Modified: Tue, 13 Feb 2024 01:53:03 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99afa0e10a58b90ea5f5be4074c19b1f6fa3d5de344ef6b183935f626cfca382`  
		Last Modified: Tue, 13 Feb 2024 01:53:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:780f985e16a46666cdda98b07ad7a4df4eb48d130c78efd7df90402a8c5ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:59b8e8924c3fad6f89bda5274bb999cfe8625b112c4db5658e89e6b9b60feeca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23361240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f5acfbed6478a5f505a17aea81378af1682062b08bc6cdd03d7edc491122a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:40:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:40:55 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 27 Jan 2024 03:41:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:41:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 27 Jan 2024 03:41:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 27 Jan 2024 03:41:00 GMT
EXPOSE 8888
# Sat, 27 Jan 2024 03:41:00 GMT
VOLUME [/var/lib/chronograf]
# Sat, 27 Jan 2024 03:41:00 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:41:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:41:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a894b23b9ee924163e7f06389bd22fa5039c489dc5e4b1a2d2867971d69c0b`  
		Last Modified: Sat, 27 Jan 2024 03:41:29 GMT  
		Size: 284.9 KB (284934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a33c886730a81544a9abd17a5ae9ae705afc4b57ce37427f345b23866fbe2a`  
		Last Modified: Sat, 27 Jan 2024 03:41:59 GMT  
		Size: 19.7 MB (19672227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404cadf46487f8dfd5e66928aed2338d8c28fb0ae64a7bf34a43f0085dedab2a`  
		Last Modified: Sat, 27 Jan 2024 03:41:55 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a884d87bf3dc589e757a8556bdcb713e33028df12ee69c8c69a405c4d769397`  
		Last Modified: Sat, 27 Jan 2024 03:41:55 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129204f45d7e31476aca1e943d4902fb7fd1f5113c372aecbcf5eedc10643895`  
		Last Modified: Sat, 27 Jan 2024 03:41:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:6d0ad66bf4af83cd75bd432858df696986d5d2f6e8edc2a1195b975c79e49607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:55c5656d179a5668cab8c253f7e23409cf821aa06bfbd69b8b1eb472527defd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71900605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814b72987a56bb71eed31a1e50a118ca20f5a0e01d190f060fb8848666dacee8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:36:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:37:09 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Feb 2024 01:37:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:37:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:37:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:37:15 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:37:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:37:16 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:37:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:37:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829c083c75eadd589b8a8f8cb16916104c86b6e3e076638ad223d9a2750ee5e0`  
		Last Modified: Tue, 13 Feb 2024 01:38:13 GMT  
		Size: 5.2 MB (5226443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bc51c64815f927f26ca986defeb6d256569a94c253a1ab42ef9ccf7b30fa41`  
		Last Modified: Tue, 13 Feb 2024 01:38:30 GMT  
		Size: 35.2 MB (35227350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1749187b30e6d96e2d26dab919ecdb931c4a03c857062726b7c88b6b1bcaef81`  
		Last Modified: Tue, 13 Feb 2024 01:38:26 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4aef0e5ec6c76655fedfc0589c830735fc9511f4e115fc42d5c5173d8fb9b3`  
		Last Modified: Tue, 13 Feb 2024 01:38:26 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30920e15d63b562afaa448f4e5f6c2d484f2083160390fe15aa8fa38e262d13`  
		Last Modified: Tue, 13 Feb 2024 01:38:26 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d06445556baf391e3cf01ed00c4fbca94c2c7b741e73d39d8a9b25c404e18a43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64626592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101c617c36e9847a07fd70cda5f670cc9b775b0dbbf81dcfe0bc49813ab8b12b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:39 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
# Tue, 13 Feb 2024 01:20:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:50:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 02:51:13 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Feb 2024 02:51:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:51:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 02:51:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 02:51:25 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 02:51:26 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 02:51:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 02:51:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:51:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb23410a5056fcfb050496c0f367867389448c109176e03309e7bf04864e81f`  
		Last Modified: Tue, 13 Feb 2024 02:52:44 GMT  
		Size: 4.5 MB (4492081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a662ef22fde244eb0cf627a3d0525298cfcd7bfa3e4ef06ed31e2d3a412f7798`  
		Last Modified: Tue, 13 Feb 2024 02:53:02 GMT  
		Size: 33.5 MB (33527454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042f6eeb4943dffe35692eb3882087579bca6106aefb98f03cec15981cfcea2`  
		Last Modified: Tue, 13 Feb 2024 02:52:56 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b70aa65193e2cb4dbb9147b153170203a6c8edad8b42f3a02ae7e67ba08079`  
		Last Modified: Tue, 13 Feb 2024 02:52:56 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1493008008f22b4a3971a4dd0b7418d799563c6dd2662b1a689edb8ceee7af`  
		Last Modified: Tue, 13 Feb 2024 02:52:56 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:72c10e7455c8d8c38c8dffb82a88f4d69ca967929ea582abdc0546d639cd9511
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68702509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4549529266df145ee04e0de318fc8ace233c49903dc2f32143d4d5f33f3487`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:51:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:52:07 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 13 Feb 2024 01:52:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:52:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:52:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:52:13 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:52:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:52:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:52:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:52:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf6a957e22a2a9e121959314e020c66ccdb2b7d3efe6cef87e93651b691c512`  
		Last Modified: Tue, 13 Feb 2024 01:52:52 GMT  
		Size: 5.2 MB (5209567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549bc8d63fe6887e7928e7d81e3e42ca8b6aeed882f6f1e59b54fd290c814c3d`  
		Last Modified: Tue, 13 Feb 2024 01:53:06 GMT  
		Size: 33.4 MB (33397475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a093f735a216bd69e0d1118cd3930cd06753476673b3113ace1a4e429ba4e298`  
		Last Modified: Tue, 13 Feb 2024 01:53:03 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42532c7431b4ca8c188c2800c2bc490ae82e99e7ea5bf838abc021c64c67f3b2`  
		Last Modified: Tue, 13 Feb 2024 01:53:03 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99afa0e10a58b90ea5f5be4074c19b1f6fa3d5de344ef6b183935f626cfca382`  
		Last Modified: Tue, 13 Feb 2024 01:53:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:780f985e16a46666cdda98b07ad7a4df4eb48d130c78efd7df90402a8c5ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:59b8e8924c3fad6f89bda5274bb999cfe8625b112c4db5658e89e6b9b60feeca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23361240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f5acfbed6478a5f505a17aea81378af1682062b08bc6cdd03d7edc491122a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:40:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:40:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:40:55 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 27 Jan 2024 03:41:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:41:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 27 Jan 2024 03:41:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 27 Jan 2024 03:41:00 GMT
EXPOSE 8888
# Sat, 27 Jan 2024 03:41:00 GMT
VOLUME [/var/lib/chronograf]
# Sat, 27 Jan 2024 03:41:00 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:41:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:41:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c332be88cb2898fd00957a6e5a3581893f9a14b30ec2470466897e8b246e9ad`  
		Last Modified: Sat, 27 Jan 2024 03:41:30 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a894b23b9ee924163e7f06389bd22fa5039c489dc5e4b1a2d2867971d69c0b`  
		Last Modified: Sat, 27 Jan 2024 03:41:29 GMT  
		Size: 284.9 KB (284934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a33c886730a81544a9abd17a5ae9ae705afc4b57ce37427f345b23866fbe2a`  
		Last Modified: Sat, 27 Jan 2024 03:41:59 GMT  
		Size: 19.7 MB (19672227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404cadf46487f8dfd5e66928aed2338d8c28fb0ae64a7bf34a43f0085dedab2a`  
		Last Modified: Sat, 27 Jan 2024 03:41:55 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a884d87bf3dc589e757a8556bdcb713e33028df12ee69c8c69a405c4d769397`  
		Last Modified: Sat, 27 Jan 2024 03:41:55 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129204f45d7e31476aca1e943d4902fb7fd1f5113c372aecbcf5eedc10643895`  
		Last Modified: Sat, 27 Jan 2024 03:41:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:7504f4ab2f4887539ce3d2c909f1ca6408d80195628832eea63877f69a2523b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7c778533d522ed28a95e32c4ee03548ffb53da4a86622d809be58448be6b917f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31559565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde71584b4fc8d5b5e38c218fada6f2ad411de8c7696cdf339ca84620205f4d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:11:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:41:06 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Sat, 27 Jan 2024 03:41:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:41:12 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 27 Jan 2024 03:41:12 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 27 Jan 2024 03:41:12 GMT
EXPOSE 8888
# Sat, 27 Jan 2024 03:41:12 GMT
VOLUME [/var/lib/chronograf]
# Sat, 27 Jan 2024 03:41:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:41:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:41:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24534ed772762b2bbf09082d1b3308d3f8c7dccd367ecbd54b5c74c15eeafde`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 284.7 KB (284696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c624949424b9846e8fde3d2631c54bb17d01a5ae3d1deb66cae28461a9216573`  
		Last Modified: Sat, 27 Jan 2024 03:42:13 GMT  
		Size: 27.8 MB (27847643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c293158dc305d0ec9786dea2382423ceedd941090dfb8a1bfeaf2561027c7450`  
		Last Modified: Sat, 27 Jan 2024 03:42:08 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31183b1bef5ed3811386cde8b8e41ed9471882c7b5e863a54aa3b5971834bf85`  
		Last Modified: Sat, 27 Jan 2024 03:42:08 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7580a090490b5fa9251ae3de9349440c555d2055c48af8983fffc2abb1d4bf`  
		Last Modified: Sat, 27 Jan 2024 03:42:08 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:b9c52b548066f3b4ed876dcb3e5f0a652548dd41cc7e7f2f42c3700dd29eab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:04462ac26b7dbe7a416cce7de3b7cb3f980b2902a3b0ea0945b2b48574b8c61d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84071849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba864730ae6dd40df4e4518818953064d84a262247c361f41dd3c4696b995db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:37:30 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 01:37:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:37:37 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:37:37 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:37:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4699424b1273b826b5cdc341e3b641e4677c94540188c99dbfe6107f04b338`  
		Last Modified: Tue, 13 Feb 2024 01:38:40 GMT  
		Size: 7.9 MB (7870359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdf86bc6e62c35c39e6459d906c2630014debc2e98d324647a464bbebf11e69`  
		Last Modified: Tue, 13 Feb 2024 01:38:45 GMT  
		Size: 47.1 MB (47053015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212a2b45925a777bacea28fb46859ff3c9d814027aa8c86354e32ff87ea2909`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2998c8c8e76f333407adb69b20a7daf0d2eda63ff22da8b98eb2e40f0ace65d`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a23ee363789d93f633ec5fd788469b8fd511b4832198e334f0cf1a4ea393a1b`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:164f96a54a6789a5d6d7a24c9f4b99b9ab6923c70cd5bf272fa5249ba2f804cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75885126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5ae27c0d2625e913fa8e6302b205402c5df1e6dd6b4c5ed3f8bda8030293cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 02:51:56 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 02:52:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:52:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 02:52:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 02:52:11 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 02:52:12 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 02:52:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 02:52:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fa9249853ada1b6b31f64fba359a34bef386b24491b6f80cd43c735b0ebd35`  
		Last Modified: Tue, 13 Feb 2024 02:53:12 GMT  
		Size: 6.5 MB (6494977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a9c5f20d623828e8c0cd47e752d2442b46028e7c104a9b3d49735da99d20e6`  
		Last Modified: Tue, 13 Feb 2024 02:53:19 GMT  
		Size: 44.6 MB (44649109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0fe2869b4515f458397b229257482fb87e4d54de15183499e91fbef9c9cec8`  
		Last Modified: Tue, 13 Feb 2024 02:53:10 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e397a95fb4e32746ad1943d95189aee536299d523974be91c03658c3c9cb7b12`  
		Last Modified: Tue, 13 Feb 2024 02:53:10 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93685ee3caaebd7a2349d57a759e12e6dfe4674e7f1d6d19cefb2dae559cbfc5`  
		Last Modified: Tue, 13 Feb 2024 02:53:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5d8d80646010cfe6875f70f0305283c4ecf410af01669a7739bbb99f6ab4d71c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81601411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ea9755b59d1150652ef5cf7cf8d8fcb4e8d418288516d3ba6d9b18a3a00b5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:52:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:52:22 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 01:52:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:52:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:52:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:52:28 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:52:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:52:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:52:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:52:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8356d255d957337b3271ca2ccb409831d13fb862aa8674a62d51e2a0cf121c5`  
		Last Modified: Tue, 13 Feb 2024 01:53:15 GMT  
		Size: 7.6 MB (7647144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae248ef7539fbb6f443297ba9bd3c53a1fc193086a6befe57cf3165c6eee1f5`  
		Last Modified: Tue, 13 Feb 2024 01:53:19 GMT  
		Size: 44.8 MB (44773513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b1b3905f9f2f89ae89d40f805eaaffd9b634c0bdbd3e9dfdb75ae53737a4bb`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0252bd3162130e739e5cabd7d9e9bea09a6b3ef32210f0103dbd7be761759e0d`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7a271221e0ffe0f48af65b288d14a19ab326cfcf5088ab1fda68f49415702c`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
