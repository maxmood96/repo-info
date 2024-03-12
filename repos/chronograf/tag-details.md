<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.3`](#chronograf1103)
-	[`chronograf:1.10.3-alpine`](#chronograf1103-alpine)
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
$ docker pull chronograf@sha256:083f7147ebde3832a4be854b9d3292ffbef150a6bcbfc305c1c46111a7508f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:e52487674516e7bd523529f1c8ee7c5a9ea402e8c64944b541466cd6b2ed1d6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84080944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee218588e2adf727d71fdcbccb7d4350016b9e59df825c18a17bf711f9c4bee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 28 Feb 2024 22:51:09 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 28 Feb 2024 22:51:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 28 Feb 2024 22:51:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 28 Feb 2024 22:51:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 28 Feb 2024 22:51:19 GMT
EXPOSE 8888
# Wed, 28 Feb 2024 22:51:19 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Feb 2024 22:51:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 28 Feb 2024 22:51:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Feb 2024 22:51:20 GMT
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
	-	`sha256:4a8e55f12424541a2e8e23f3e0cf88a5d1d3f9e99772269d434a6fff9d0f50b3`  
		Last Modified: Wed, 28 Feb 2024 22:51:57 GMT  
		Size: 47.1 MB (47062107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb101b090416d1c2ab2f5b75a323db75a662d9c53c771593c819d3582cdb2bd`  
		Last Modified: Wed, 28 Feb 2024 22:51:51 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b88a3c5c768253177a4dbb5f86629d99cb702011e4cdca7d8e181dba7fb3630`  
		Last Modified: Wed, 28 Feb 2024 22:51:51 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b1baaf522e3d47fc30204a7aa802ef64d4b170102e01fd2151ecc4d8e962e`  
		Last Modified: Wed, 28 Feb 2024 22:51:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ac86911909685cf357a22361691ff445ca9e85a29158221f7f0fdfa3a22df6c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75888012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565838b7551edbef7e5c55ad95031b2ac7605e28f49ec86f20ca20b69c594024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 28 Feb 2024 21:51:50 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 28 Feb 2024 21:52:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 28 Feb 2024 21:52:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 28 Feb 2024 21:52:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 28 Feb 2024 21:52:03 GMT
EXPOSE 8888
# Wed, 28 Feb 2024 21:52:03 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Feb 2024 21:52:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 28 Feb 2024 21:52:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Feb 2024 21:52:03 GMT
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
	-	`sha256:7c5d2f5aec634562162fc0968eea9b75c0a255305210a5fc96a911857203bbaa`  
		Last Modified: Wed, 28 Feb 2024 21:52:26 GMT  
		Size: 44.7 MB (44651992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8aba5ac3153918ca823fef9a8f5049660c9d5e6f422bd61a4a9ab29fc801c5`  
		Last Modified: Wed, 28 Feb 2024 21:52:19 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529df11f5459db42a3eba6bfa7c3eeb869f7461d786b4a87b1f279918f264a7b`  
		Last Modified: Wed, 28 Feb 2024 21:52:19 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d51ec578ed6a768c45bc4bd74e603f29897558e43bdad85e66a47399c137`  
		Last Modified: Wed, 28 Feb 2024 21:52:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:715aba20aa6226c793fafc508ae6d45450674c0e4d782bb81ea787466a71d9c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81618278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacaf41c366822e8f6997928164674e3ace666c585382c8c3f1764e0d325cf54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:40:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 01:40:40 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Tue, 12 Mar 2024 01:40:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:40:48 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Mar 2024 01:40:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Mar 2024 01:40:48 GMT
EXPOSE 8888
# Tue, 12 Mar 2024 01:40:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Mar 2024 01:40:48 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Mar 2024 01:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 01:40:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874b126ecb6fa274dfdb60449996fa41caa0ed81035a911293ad47a6246b5fb`  
		Last Modified: Tue, 12 Mar 2024 01:41:35 GMT  
		Size: 7.6 MB (7647190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b593b92507b5ba9af3a3c414fc982ffb2e57fb3ffcec44266871a6e56ef08ec`  
		Last Modified: Tue, 12 Mar 2024 01:41:39 GMT  
		Size: 44.8 MB (44790261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3e3ac909f79b313e69a21da13f757cfc393da16d008f3b8f31b43c2867b789`  
		Last Modified: Tue, 12 Mar 2024 01:41:34 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe513d8c326c90470dc9d9c72b29af2fc9453df2e3996c2d2125cc4b2465d302`  
		Last Modified: Tue, 12 Mar 2024 01:41:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237bc863051e7fc3f56a03e6fab4f4253f88398f087fa195dfb2e45143fb9ec0`  
		Last Modified: Tue, 12 Mar 2024 01:41:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:de4749482f214597a5817c3258312c935282985dea909a82a7499b3131d2ec28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7d57e94195bd5f194f97064b962d88005aff44c4360c5e056d182638964fa215
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31566096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdeaf4c467b46cbf96b4201f5c0b474fd7a9a2a8955ffca865978da4c5d2937e`
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
# Wed, 28 Feb 2024 22:51:24 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 28 Feb 2024 22:51:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 28 Feb 2024 22:51:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 28 Feb 2024 22:51:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 28 Feb 2024 22:51:30 GMT
EXPOSE 8888
# Wed, 28 Feb 2024 22:51:30 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Feb 2024 22:51:30 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 28 Feb 2024 22:51:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Feb 2024 22:51:30 GMT
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
	-	`sha256:b33a76c8868e3829c411283b1f3b2258587e18439a3854a5a9f8e1bc20cb4325`  
		Last Modified: Wed, 28 Feb 2024 22:52:12 GMT  
		Size: 27.9 MB (27854170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4abc3026ebc412c406ee7fd914436238ce42d00389c16df2166546d98b0b97c`  
		Last Modified: Wed, 28 Feb 2024 22:52:08 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d2c53c3010f6ab7237639313cbec1cb88ce63ebe1c2691425fcaf28e397abd`  
		Last Modified: Wed, 28 Feb 2024 22:52:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57568e663ba60a29816eba284d76e2b1ae7d26f9789bbc4ab0834703fd80a445`  
		Last Modified: Wed, 28 Feb 2024 22:52:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.3`

```console
$ docker pull chronograf@sha256:083f7147ebde3832a4be854b9d3292ffbef150a6bcbfc305c1c46111a7508f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.3` - linux; amd64

```console
$ docker pull chronograf@sha256:e52487674516e7bd523529f1c8ee7c5a9ea402e8c64944b541466cd6b2ed1d6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84080944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee218588e2adf727d71fdcbccb7d4350016b9e59df825c18a17bf711f9c4bee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 28 Feb 2024 22:51:09 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 28 Feb 2024 22:51:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 28 Feb 2024 22:51:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 28 Feb 2024 22:51:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 28 Feb 2024 22:51:19 GMT
EXPOSE 8888
# Wed, 28 Feb 2024 22:51:19 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Feb 2024 22:51:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 28 Feb 2024 22:51:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Feb 2024 22:51:20 GMT
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
	-	`sha256:4a8e55f12424541a2e8e23f3e0cf88a5d1d3f9e99772269d434a6fff9d0f50b3`  
		Last Modified: Wed, 28 Feb 2024 22:51:57 GMT  
		Size: 47.1 MB (47062107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb101b090416d1c2ab2f5b75a323db75a662d9c53c771593c819d3582cdb2bd`  
		Last Modified: Wed, 28 Feb 2024 22:51:51 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b88a3c5c768253177a4dbb5f86629d99cb702011e4cdca7d8e181dba7fb3630`  
		Last Modified: Wed, 28 Feb 2024 22:51:51 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b1baaf522e3d47fc30204a7aa802ef64d4b170102e01fd2151ecc4d8e962e`  
		Last Modified: Wed, 28 Feb 2024 22:51:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.3` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ac86911909685cf357a22361691ff445ca9e85a29158221f7f0fdfa3a22df6c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75888012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565838b7551edbef7e5c55ad95031b2ac7605e28f49ec86f20ca20b69c594024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 28 Feb 2024 21:51:50 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 28 Feb 2024 21:52:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 28 Feb 2024 21:52:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 28 Feb 2024 21:52:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 28 Feb 2024 21:52:03 GMT
EXPOSE 8888
# Wed, 28 Feb 2024 21:52:03 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Feb 2024 21:52:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 28 Feb 2024 21:52:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Feb 2024 21:52:03 GMT
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
	-	`sha256:7c5d2f5aec634562162fc0968eea9b75c0a255305210a5fc96a911857203bbaa`  
		Last Modified: Wed, 28 Feb 2024 21:52:26 GMT  
		Size: 44.7 MB (44651992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8aba5ac3153918ca823fef9a8f5049660c9d5e6f422bd61a4a9ab29fc801c5`  
		Last Modified: Wed, 28 Feb 2024 21:52:19 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529df11f5459db42a3eba6bfa7c3eeb869f7461d786b4a87b1f279918f264a7b`  
		Last Modified: Wed, 28 Feb 2024 21:52:19 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d51ec578ed6a768c45bc4bd74e603f29897558e43bdad85e66a47399c137`  
		Last Modified: Wed, 28 Feb 2024 21:52:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.3` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:715aba20aa6226c793fafc508ae6d45450674c0e4d782bb81ea787466a71d9c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81618278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacaf41c366822e8f6997928164674e3ace666c585382c8c3f1764e0d325cf54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:40:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 01:40:40 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Tue, 12 Mar 2024 01:40:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:40:48 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Mar 2024 01:40:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Mar 2024 01:40:48 GMT
EXPOSE 8888
# Tue, 12 Mar 2024 01:40:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Mar 2024 01:40:48 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Mar 2024 01:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 01:40:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874b126ecb6fa274dfdb60449996fa41caa0ed81035a911293ad47a6246b5fb`  
		Last Modified: Tue, 12 Mar 2024 01:41:35 GMT  
		Size: 7.6 MB (7647190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b593b92507b5ba9af3a3c414fc982ffb2e57fb3ffcec44266871a6e56ef08ec`  
		Last Modified: Tue, 12 Mar 2024 01:41:39 GMT  
		Size: 44.8 MB (44790261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3e3ac909f79b313e69a21da13f757cfc393da16d008f3b8f31b43c2867b789`  
		Last Modified: Tue, 12 Mar 2024 01:41:34 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe513d8c326c90470dc9d9c72b29af2fc9453df2e3996c2d2125cc4b2465d302`  
		Last Modified: Tue, 12 Mar 2024 01:41:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237bc863051e7fc3f56a03e6fab4f4253f88398f087fa195dfb2e45143fb9ec0`  
		Last Modified: Tue, 12 Mar 2024 01:41:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.3-alpine`

```console
$ docker pull chronograf@sha256:de4749482f214597a5817c3258312c935282985dea909a82a7499b3131d2ec28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.3-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7d57e94195bd5f194f97064b962d88005aff44c4360c5e056d182638964fa215
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31566096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdeaf4c467b46cbf96b4201f5c0b474fd7a9a2a8955ffca865978da4c5d2937e`
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
# Wed, 28 Feb 2024 22:51:24 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 28 Feb 2024 22:51:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 28 Feb 2024 22:51:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 28 Feb 2024 22:51:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 28 Feb 2024 22:51:30 GMT
EXPOSE 8888
# Wed, 28 Feb 2024 22:51:30 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Feb 2024 22:51:30 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 28 Feb 2024 22:51:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Feb 2024 22:51:30 GMT
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
	-	`sha256:b33a76c8868e3829c411283b1f3b2258587e18439a3854a5a9f8e1bc20cb4325`  
		Last Modified: Wed, 28 Feb 2024 22:52:12 GMT  
		Size: 27.9 MB (27854170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4abc3026ebc412c406ee7fd914436238ce42d00389c16df2166546d98b0b97c`  
		Last Modified: Wed, 28 Feb 2024 22:52:08 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d2c53c3010f6ab7237639313cbec1cb88ce63ebe1c2691425fcaf28e397abd`  
		Last Modified: Wed, 28 Feb 2024 22:52:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57568e663ba60a29816eba284d76e2b1ae7d26f9789bbc4ab0834703fd80a445`  
		Last Modified: Wed, 28 Feb 2024 22:52:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:3f8ebba586c5d560d2ee22a8f5a132fe6c797b121a8c6e43ad4d031e6cd14b65
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
$ docker pull chronograf@sha256:a6729ad7af2aaf23e11e24b0e2047a778d42ac74c099d03f5f45058adcb348d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67752259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d146791618c6d40d83a1cedc1fd80b917874d6f8a742ef0ff7e40175242c855b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 01:39:56 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Mar 2024 01:40:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:40:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Mar 2024 01:40:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Mar 2024 01:40:03 GMT
EXPOSE 8888
# Tue, 12 Mar 2024 01:40:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Mar 2024 01:40:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Mar 2024 01:40:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 01:40:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba5595889da88cecd11b0ad971df924fa863673a16024ffbcdb3f68004a1661`  
		Last Modified: Tue, 12 Mar 2024 01:41:02 GMT  
		Size: 4.4 MB (4418049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85167bd8545d4c22bc57d225cf0f3d9dc1f2d5df65f9901af23264d419beb`  
		Last Modified: Tue, 12 Mar 2024 01:41:04 GMT  
		Size: 33.2 MB (33238697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081b967540b546a165182f8634651230279d33ad25ebbed2efd79fa2b6c39b3f`  
		Last Modified: Tue, 12 Mar 2024 01:41:01 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5420a777fc5285d26b81e653c85dea231bf22318923ac3fdf46ed20fd5b48`  
		Last Modified: Tue, 12 Mar 2024 01:41:01 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c8c123a616776e50c4a2bab2ee7abf7fb9985760083f27643f6634f3d2c421`  
		Last Modified: Tue, 12 Mar 2024 01:41:01 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:3f8ebba586c5d560d2ee22a8f5a132fe6c797b121a8c6e43ad4d031e6cd14b65
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
$ docker pull chronograf@sha256:a6729ad7af2aaf23e11e24b0e2047a778d42ac74c099d03f5f45058adcb348d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67752259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d146791618c6d40d83a1cedc1fd80b917874d6f8a742ef0ff7e40175242c855b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 01:39:56 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 12 Mar 2024 01:40:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:40:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Mar 2024 01:40:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Mar 2024 01:40:03 GMT
EXPOSE 8888
# Tue, 12 Mar 2024 01:40:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Mar 2024 01:40:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Mar 2024 01:40:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 01:40:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba5595889da88cecd11b0ad971df924fa863673a16024ffbcdb3f68004a1661`  
		Last Modified: Tue, 12 Mar 2024 01:41:02 GMT  
		Size: 4.4 MB (4418049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b85167bd8545d4c22bc57d225cf0f3d9dc1f2d5df65f9901af23264d419beb`  
		Last Modified: Tue, 12 Mar 2024 01:41:04 GMT  
		Size: 33.2 MB (33238697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081b967540b546a165182f8634651230279d33ad25ebbed2efd79fa2b6c39b3f`  
		Last Modified: Tue, 12 Mar 2024 01:41:01 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b5420a777fc5285d26b81e653c85dea231bf22318923ac3fdf46ed20fd5b48`  
		Last Modified: Tue, 12 Mar 2024 01:41:01 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c8c123a616776e50c4a2bab2ee7abf7fb9985760083f27643f6634f3d2c421`  
		Last Modified: Tue, 12 Mar 2024 01:41:01 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:de2e858cbd34e7f26c92919932a9bf0db9c68e7b45a01126a54ac6e0125b4637
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
$ docker pull chronograf@sha256:922f2a877af04315e27cd8c800750a7869991df59bf640ee95cabfa2c3d58af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67950175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18027bd544f8be24bb36357207fadd8280ed744b5729b7ff9888e1c104dc09ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:40:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 01:40:13 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Mar 2024 01:40:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:40:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Mar 2024 01:40:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Mar 2024 01:40:19 GMT
EXPOSE 8888
# Tue, 12 Mar 2024 01:40:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Mar 2024 01:40:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Mar 2024 01:40:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 01:40:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc29f81ae0d155b86351dba48cfe0dfd6b011e81aa8d1a054417a82f15a812b`  
		Last Modified: Tue, 12 Mar 2024 01:41:13 GMT  
		Size: 5.2 MB (5209512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5938b167d37c8f2f749f0ae11a4351baac4d54b4593b555784df99b022c4bd85`  
		Last Modified: Tue, 12 Mar 2024 01:41:16 GMT  
		Size: 32.6 MB (32645149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689c741d4a1c8c330ea339ec81731fece0f99084fa1a49f75087d10e72d8b2c2`  
		Last Modified: Tue, 12 Mar 2024 01:41:13 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa6b1361e7cae1bcf627bc8e9f252791ad52d978941c811774ea24a17ab2c87`  
		Last Modified: Tue, 12 Mar 2024 01:41:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7f7e39c8f75b410861234d02e155a360d50139085987a01de2aaab62d9c24a`  
		Last Modified: Tue, 12 Mar 2024 01:41:12 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:de2e858cbd34e7f26c92919932a9bf0db9c68e7b45a01126a54ac6e0125b4637
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
$ docker pull chronograf@sha256:922f2a877af04315e27cd8c800750a7869991df59bf640ee95cabfa2c3d58af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67950175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18027bd544f8be24bb36357207fadd8280ed744b5729b7ff9888e1c104dc09ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:40:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 01:40:13 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 12 Mar 2024 01:40:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:40:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Mar 2024 01:40:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Mar 2024 01:40:19 GMT
EXPOSE 8888
# Tue, 12 Mar 2024 01:40:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Mar 2024 01:40:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Mar 2024 01:40:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 01:40:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc29f81ae0d155b86351dba48cfe0dfd6b011e81aa8d1a054417a82f15a812b`  
		Last Modified: Tue, 12 Mar 2024 01:41:13 GMT  
		Size: 5.2 MB (5209512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5938b167d37c8f2f749f0ae11a4351baac4d54b4593b555784df99b022c4bd85`  
		Last Modified: Tue, 12 Mar 2024 01:41:16 GMT  
		Size: 32.6 MB (32645149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689c741d4a1c8c330ea339ec81731fece0f99084fa1a49f75087d10e72d8b2c2`  
		Last Modified: Tue, 12 Mar 2024 01:41:13 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa6b1361e7cae1bcf627bc8e9f252791ad52d978941c811774ea24a17ab2c87`  
		Last Modified: Tue, 12 Mar 2024 01:41:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7f7e39c8f75b410861234d02e155a360d50139085987a01de2aaab62d9c24a`  
		Last Modified: Tue, 12 Mar 2024 01:41:12 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:178898723949ef42f4ab97419b3051f31e6024d4afe0110b2875eabf31c17b3d
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
$ docker pull chronograf@sha256:a4219c3d62942a01fbecc8775a452a14bf2760ff7700df5e0d23729601214622
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68702513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ac9080de12ec7bb3440e60eac9ebfb2301b84c8a6cdc87ddeb02082e9b0143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:40:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 01:40:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 12 Mar 2024 01:40:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:40:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Mar 2024 01:40:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Mar 2024 01:40:29 GMT
EXPOSE 8888
# Tue, 12 Mar 2024 01:40:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Mar 2024 01:40:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Mar 2024 01:40:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 01:40:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc29f81ae0d155b86351dba48cfe0dfd6b011e81aa8d1a054417a82f15a812b`  
		Last Modified: Tue, 12 Mar 2024 01:41:13 GMT  
		Size: 5.2 MB (5209512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc44db49161bb3333b10d287c34c422b2cc25450562ec63aaa9909717284501b`  
		Last Modified: Tue, 12 Mar 2024 01:41:26 GMT  
		Size: 33.4 MB (33397489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336e478695e6d70f8f71b8210c8cf5846cb930931334de445885ce785d1ca158`  
		Last Modified: Tue, 12 Mar 2024 01:41:23 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdea8e1e67a3b0506503bbfaa3232fa8a4ac5281d2a46986b31783703cc20a46`  
		Last Modified: Tue, 12 Mar 2024 01:41:23 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a3c53dc7abc4c249b0b71a3dd4f05560e25ed83d412e0d78d556e92827eee8`  
		Last Modified: Tue, 12 Mar 2024 01:41:23 GMT  
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
$ docker pull chronograf@sha256:178898723949ef42f4ab97419b3051f31e6024d4afe0110b2875eabf31c17b3d
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
$ docker pull chronograf@sha256:a4219c3d62942a01fbecc8775a452a14bf2760ff7700df5e0d23729601214622
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68702513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ac9080de12ec7bb3440e60eac9ebfb2301b84c8a6cdc87ddeb02082e9b0143`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:40:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 01:40:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 12 Mar 2024 01:40:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:40:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Mar 2024 01:40:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Mar 2024 01:40:29 GMT
EXPOSE 8888
# Tue, 12 Mar 2024 01:40:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Mar 2024 01:40:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Mar 2024 01:40:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 01:40:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc29f81ae0d155b86351dba48cfe0dfd6b011e81aa8d1a054417a82f15a812b`  
		Last Modified: Tue, 12 Mar 2024 01:41:13 GMT  
		Size: 5.2 MB (5209512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc44db49161bb3333b10d287c34c422b2cc25450562ec63aaa9909717284501b`  
		Last Modified: Tue, 12 Mar 2024 01:41:26 GMT  
		Size: 33.4 MB (33397489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336e478695e6d70f8f71b8210c8cf5846cb930931334de445885ce785d1ca158`  
		Last Modified: Tue, 12 Mar 2024 01:41:23 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdea8e1e67a3b0506503bbfaa3232fa8a4ac5281d2a46986b31783703cc20a46`  
		Last Modified: Tue, 12 Mar 2024 01:41:23 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a3c53dc7abc4c249b0b71a3dd4f05560e25ed83d412e0d78d556e92827eee8`  
		Last Modified: Tue, 12 Mar 2024 01:41:23 GMT  
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
$ docker pull chronograf@sha256:de4749482f214597a5817c3258312c935282985dea909a82a7499b3131d2ec28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7d57e94195bd5f194f97064b962d88005aff44c4360c5e056d182638964fa215
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31566096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdeaf4c467b46cbf96b4201f5c0b474fd7a9a2a8955ffca865978da4c5d2937e`
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
# Wed, 28 Feb 2024 22:51:24 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 28 Feb 2024 22:51:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 28 Feb 2024 22:51:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 28 Feb 2024 22:51:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 28 Feb 2024 22:51:30 GMT
EXPOSE 8888
# Wed, 28 Feb 2024 22:51:30 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Feb 2024 22:51:30 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Wed, 28 Feb 2024 22:51:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Feb 2024 22:51:30 GMT
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
	-	`sha256:b33a76c8868e3829c411283b1f3b2258587e18439a3854a5a9f8e1bc20cb4325`  
		Last Modified: Wed, 28 Feb 2024 22:52:12 GMT  
		Size: 27.9 MB (27854170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4abc3026ebc412c406ee7fd914436238ce42d00389c16df2166546d98b0b97c`  
		Last Modified: Wed, 28 Feb 2024 22:52:08 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d2c53c3010f6ab7237639313cbec1cb88ce63ebe1c2691425fcaf28e397abd`  
		Last Modified: Wed, 28 Feb 2024 22:52:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57568e663ba60a29816eba284d76e2b1ae7d26f9789bbc4ab0834703fd80a445`  
		Last Modified: Wed, 28 Feb 2024 22:52:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:083f7147ebde3832a4be854b9d3292ffbef150a6bcbfc305c1c46111a7508f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:e52487674516e7bd523529f1c8ee7c5a9ea402e8c64944b541466cd6b2ed1d6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84080944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee218588e2adf727d71fdcbccb7d4350016b9e59df825c18a17bf711f9c4bee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 28 Feb 2024 22:51:09 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 28 Feb 2024 22:51:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 28 Feb 2024 22:51:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 28 Feb 2024 22:51:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 28 Feb 2024 22:51:19 GMT
EXPOSE 8888
# Wed, 28 Feb 2024 22:51:19 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Feb 2024 22:51:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 28 Feb 2024 22:51:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Feb 2024 22:51:20 GMT
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
	-	`sha256:4a8e55f12424541a2e8e23f3e0cf88a5d1d3f9e99772269d434a6fff9d0f50b3`  
		Last Modified: Wed, 28 Feb 2024 22:51:57 GMT  
		Size: 47.1 MB (47062107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb101b090416d1c2ab2f5b75a323db75a662d9c53c771593c819d3582cdb2bd`  
		Last Modified: Wed, 28 Feb 2024 22:51:51 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b88a3c5c768253177a4dbb5f86629d99cb702011e4cdca7d8e181dba7fb3630`  
		Last Modified: Wed, 28 Feb 2024 22:51:51 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5b1baaf522e3d47fc30204a7aa802ef64d4b170102e01fd2151ecc4d8e962e`  
		Last Modified: Wed, 28 Feb 2024 22:51:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ac86911909685cf357a22361691ff445ca9e85a29158221f7f0fdfa3a22df6c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75888012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565838b7551edbef7e5c55ad95031b2ac7605e28f49ec86f20ca20b69c594024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 28 Feb 2024 21:51:50 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 28 Feb 2024 21:52:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 28 Feb 2024 21:52:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 28 Feb 2024 21:52:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 28 Feb 2024 21:52:03 GMT
EXPOSE 8888
# Wed, 28 Feb 2024 21:52:03 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Feb 2024 21:52:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 28 Feb 2024 21:52:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Feb 2024 21:52:03 GMT
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
	-	`sha256:7c5d2f5aec634562162fc0968eea9b75c0a255305210a5fc96a911857203bbaa`  
		Last Modified: Wed, 28 Feb 2024 21:52:26 GMT  
		Size: 44.7 MB (44651992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8aba5ac3153918ca823fef9a8f5049660c9d5e6f422bd61a4a9ab29fc801c5`  
		Last Modified: Wed, 28 Feb 2024 21:52:19 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529df11f5459db42a3eba6bfa7c3eeb869f7461d786b4a87b1f279918f264a7b`  
		Last Modified: Wed, 28 Feb 2024 21:52:19 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d46d51ec578ed6a768c45bc4bd74e603f29897558e43bdad85e66a47399c137`  
		Last Modified: Wed, 28 Feb 2024 21:52:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:715aba20aa6226c793fafc508ae6d45450674c0e4d782bb81ea787466a71d9c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81618278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacaf41c366822e8f6997928164674e3ace666c585382c8c3f1764e0d325cf54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:40:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 01:40:40 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Tue, 12 Mar 2024 01:40:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:40:48 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Mar 2024 01:40:48 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Mar 2024 01:40:48 GMT
EXPOSE 8888
# Tue, 12 Mar 2024 01:40:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Mar 2024 01:40:48 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Mar 2024 01:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 01:40:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8874b126ecb6fa274dfdb60449996fa41caa0ed81035a911293ad47a6246b5fb`  
		Last Modified: Tue, 12 Mar 2024 01:41:35 GMT  
		Size: 7.6 MB (7647190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b593b92507b5ba9af3a3c414fc982ffb2e57fb3ffcec44266871a6e56ef08ec`  
		Last Modified: Tue, 12 Mar 2024 01:41:39 GMT  
		Size: 44.8 MB (44790261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3e3ac909f79b313e69a21da13f757cfc393da16d008f3b8f31b43c2867b789`  
		Last Modified: Tue, 12 Mar 2024 01:41:34 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe513d8c326c90470dc9d9c72b29af2fc9453df2e3996c2d2125cc4b2465d302`  
		Last Modified: Tue, 12 Mar 2024 01:41:34 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237bc863051e7fc3f56a03e6fab4f4253f88398f087fa195dfb2e45143fb9ec0`  
		Last Modified: Tue, 12 Mar 2024 01:41:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
