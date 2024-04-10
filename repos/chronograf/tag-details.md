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
$ docker pull chronograf@sha256:e429b94893f07a776ad6a99a2cb3bc9d3c35f760264de0754d454a372df2a48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:2e40d41b813ba900e66202581eacf7aedde0dd170dac5eb3c23717a1c7b0c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84088157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d7c71cc1be8579e816a6863034273d54dd892ca8ebef89a7c6c6c27aef32b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:13:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 06:13:53 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 10 Apr 2024 06:14:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:14:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 06:14:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 06:14:02 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 06:14:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 06:14:02 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 06:14:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:14:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10cf296e0e4c72f988a9c65f96602201aa59c2dc799b45e216055ace05c353c`  
		Last Modified: Wed, 10 Apr 2024 06:15:03 GMT  
		Size: 7.9 MB (7870385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7737e84fb59431d887d46c7e502391f0bb486024e9ae6a467f4984a960c218`  
		Last Modified: Wed, 10 Apr 2024 06:15:08 GMT  
		Size: 47.1 MB (47062023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a51405fbcdf2623ccb035d828b11dee3a02c6da0d140c094803983bac43189f`  
		Last Modified: Wed, 10 Apr 2024 06:15:02 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a95afc221d3a6d898fdbe1e368bba4d948fbe8d96659bd8c50ca531ba9eca0`  
		Last Modified: Wed, 10 Apr 2024 06:15:02 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9161c2be5d42be6f57dd01808a23d8b6ce4fc87cabfc121efacde92b598b2673`  
		Last Modified: Wed, 10 Apr 2024 06:15:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d263edc5bb074544e4bcbfcee26e85421e62a4cd6a3f6867785ecc1ca469ea9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75894357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db3e801b8d5f016c6d35b3c15e2229d24b17fd4f762aa6615a518c74a797073`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:11 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Wed, 10 Apr 2024 00:58:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:43:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 07:43:52 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 10 Apr 2024 07:44:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:44:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 07:44:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 07:44:11 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 07:44:11 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 07:44:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 07:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 07:44:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4f25b4ac6372ba346d6434625f83dba4e6ee2fb3c4e00140bfa4a41a2cf6ef`  
		Last Modified: Wed, 10 Apr 2024 07:45:19 GMT  
		Size: 6.5 MB (6495016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232a5311219bba33d66c91a4cff6e1f1a8d15cd0796ac56340bd239300a22fd9`  
		Last Modified: Wed, 10 Apr 2024 07:45:27 GMT  
		Size: 44.7 MB (44652023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ae1395d57960ff15937d7afac04153a74586dacb0b15396c9a0130b247671`  
		Last Modified: Wed, 10 Apr 2024 07:45:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b64a4d1a58e41999509949dddc867b89613eaad3478cf4bf2c5d49e7a382ce`  
		Last Modified: Wed, 10 Apr 2024 07:45:18 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505a9ebaa15449db4334510c3d75ac368f7fb45508f1e86d4ce26da067b76ce3`  
		Last Modified: Wed, 10 Apr 2024 07:45:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d6e9f583e1199c357877b35cbf747c643feeb0fabc70a6320bbb04904e601c5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81624175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2dcaafa57f86a500a0e86c62a5de0d6604e91baad421aa5616a213a35ad552`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:19:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 04:19:29 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 10 Apr 2024 04:19:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:19:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 04:19:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 04:19:38 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 04:19:38 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 04:19:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 04:19:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 04:19:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1d7d8a6358c8838e0104fe26f761cec05931d76d43a89886e83755c7c93013`  
		Last Modified: Wed, 10 Apr 2024 04:20:27 GMT  
		Size: 7.6 MB (7647268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb101624a62824ae74c02a3fc4eb1a3c15aa41d78b2dc7f70126ec26bd33d3d`  
		Last Modified: Wed, 10 Apr 2024 04:20:30 GMT  
		Size: 44.8 MB (44790363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f38fdbad0ac3c099da75e00b19bb8657d2c51c525bb15f8ce2eb06b073e284`  
		Last Modified: Wed, 10 Apr 2024 04:20:25 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3111c51e3444ff352a97f3b75a7f241357c137d2207495b86e0baeae8f25e2c1`  
		Last Modified: Wed, 10 Apr 2024 04:20:25 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d40a8ebbb32e9b50b0f4b1d95898be2da8eec6975abb4506d863ee57f35454`  
		Last Modified: Wed, 10 Apr 2024 04:20:26 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:7d96aada68f7a3b98895d0faeea984baba66af1b2808dba9f6d0521c8b5a944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a3afdd4ea86424100f3db85c4c76756f9b0b86d409211ffb730ee64340df2c08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31566092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d628147ca6e52b9a6e841c074d13321cbfb2cbb3f6427f8a3b5ea41f6aa9da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:47 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Sat, 16 Mar 2024 03:20:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:54 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:54 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:54 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:54 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:54 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377633fb5fdd007c0931220a6d839bb8682cccad8022dfb9d9a6a13f48bbcb31`  
		Last Modified: Sat, 16 Mar 2024 03:21:47 GMT  
		Size: 284.7 KB (284701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f9378d075e5479db8cee400626beec3637332abd781326a69cb1c2173ffd8e`  
		Last Modified: Sat, 16 Mar 2024 03:21:52 GMT  
		Size: 27.9 MB (27854172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68a198732915ac9a64b856384eef314de7974b3cca48446018aa151e50d6148`  
		Last Modified: Sat, 16 Mar 2024 03:21:46 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ce7d3e21fb69d974a79be54d2cd4667472c50ccf5a30c31c037687cfef4e6e`  
		Last Modified: Sat, 16 Mar 2024 03:21:46 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48216b42c8c48a5aebdd1f2d1009c957b6c0b3d86efa905e6f3d5143ae03fe5`  
		Last Modified: Sat, 16 Mar 2024 03:21:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.3`

```console
$ docker pull chronograf@sha256:e429b94893f07a776ad6a99a2cb3bc9d3c35f760264de0754d454a372df2a48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.3` - linux; amd64

```console
$ docker pull chronograf@sha256:2e40d41b813ba900e66202581eacf7aedde0dd170dac5eb3c23717a1c7b0c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84088157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d7c71cc1be8579e816a6863034273d54dd892ca8ebef89a7c6c6c27aef32b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:13:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 06:13:53 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 10 Apr 2024 06:14:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:14:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 06:14:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 06:14:02 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 06:14:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 06:14:02 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 06:14:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:14:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10cf296e0e4c72f988a9c65f96602201aa59c2dc799b45e216055ace05c353c`  
		Last Modified: Wed, 10 Apr 2024 06:15:03 GMT  
		Size: 7.9 MB (7870385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7737e84fb59431d887d46c7e502391f0bb486024e9ae6a467f4984a960c218`  
		Last Modified: Wed, 10 Apr 2024 06:15:08 GMT  
		Size: 47.1 MB (47062023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a51405fbcdf2623ccb035d828b11dee3a02c6da0d140c094803983bac43189f`  
		Last Modified: Wed, 10 Apr 2024 06:15:02 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a95afc221d3a6d898fdbe1e368bba4d948fbe8d96659bd8c50ca531ba9eca0`  
		Last Modified: Wed, 10 Apr 2024 06:15:02 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9161c2be5d42be6f57dd01808a23d8b6ce4fc87cabfc121efacde92b598b2673`  
		Last Modified: Wed, 10 Apr 2024 06:15:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.3` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d263edc5bb074544e4bcbfcee26e85421e62a4cd6a3f6867785ecc1ca469ea9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75894357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db3e801b8d5f016c6d35b3c15e2229d24b17fd4f762aa6615a518c74a797073`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:11 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Wed, 10 Apr 2024 00:58:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:43:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 07:43:52 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 10 Apr 2024 07:44:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:44:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 07:44:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 07:44:11 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 07:44:11 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 07:44:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 07:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 07:44:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4f25b4ac6372ba346d6434625f83dba4e6ee2fb3c4e00140bfa4a41a2cf6ef`  
		Last Modified: Wed, 10 Apr 2024 07:45:19 GMT  
		Size: 6.5 MB (6495016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232a5311219bba33d66c91a4cff6e1f1a8d15cd0796ac56340bd239300a22fd9`  
		Last Modified: Wed, 10 Apr 2024 07:45:27 GMT  
		Size: 44.7 MB (44652023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ae1395d57960ff15937d7afac04153a74586dacb0b15396c9a0130b247671`  
		Last Modified: Wed, 10 Apr 2024 07:45:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b64a4d1a58e41999509949dddc867b89613eaad3478cf4bf2c5d49e7a382ce`  
		Last Modified: Wed, 10 Apr 2024 07:45:18 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505a9ebaa15449db4334510c3d75ac368f7fb45508f1e86d4ce26da067b76ce3`  
		Last Modified: Wed, 10 Apr 2024 07:45:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.3` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d6e9f583e1199c357877b35cbf747c643feeb0fabc70a6320bbb04904e601c5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81624175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2dcaafa57f86a500a0e86c62a5de0d6604e91baad421aa5616a213a35ad552`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:19:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 04:19:29 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 10 Apr 2024 04:19:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:19:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 04:19:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 04:19:38 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 04:19:38 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 04:19:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 04:19:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 04:19:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1d7d8a6358c8838e0104fe26f761cec05931d76d43a89886e83755c7c93013`  
		Last Modified: Wed, 10 Apr 2024 04:20:27 GMT  
		Size: 7.6 MB (7647268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb101624a62824ae74c02a3fc4eb1a3c15aa41d78b2dc7f70126ec26bd33d3d`  
		Last Modified: Wed, 10 Apr 2024 04:20:30 GMT  
		Size: 44.8 MB (44790363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f38fdbad0ac3c099da75e00b19bb8657d2c51c525bb15f8ce2eb06b073e284`  
		Last Modified: Wed, 10 Apr 2024 04:20:25 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3111c51e3444ff352a97f3b75a7f241357c137d2207495b86e0baeae8f25e2c1`  
		Last Modified: Wed, 10 Apr 2024 04:20:25 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d40a8ebbb32e9b50b0f4b1d95898be2da8eec6975abb4506d863ee57f35454`  
		Last Modified: Wed, 10 Apr 2024 04:20:26 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.3-alpine`

```console
$ docker pull chronograf@sha256:7d96aada68f7a3b98895d0faeea984baba66af1b2808dba9f6d0521c8b5a944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.3-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a3afdd4ea86424100f3db85c4c76756f9b0b86d409211ffb730ee64340df2c08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31566092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d628147ca6e52b9a6e841c074d13321cbfb2cbb3f6427f8a3b5ea41f6aa9da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:47 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Sat, 16 Mar 2024 03:20:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:54 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:54 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:54 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:54 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:54 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377633fb5fdd007c0931220a6d839bb8682cccad8022dfb9d9a6a13f48bbcb31`  
		Last Modified: Sat, 16 Mar 2024 03:21:47 GMT  
		Size: 284.7 KB (284701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f9378d075e5479db8cee400626beec3637332abd781326a69cb1c2173ffd8e`  
		Last Modified: Sat, 16 Mar 2024 03:21:52 GMT  
		Size: 27.9 MB (27854172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68a198732915ac9a64b856384eef314de7974b3cca48446018aa151e50d6148`  
		Last Modified: Sat, 16 Mar 2024 03:21:46 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ce7d3e21fb69d974a79be54d2cd4667472c50ccf5a30c31c037687cfef4e6e`  
		Last Modified: Sat, 16 Mar 2024 03:21:46 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48216b42c8c48a5aebdd1f2d1009c957b6c0b3d86efa905e6f3d5143ae03fe5`  
		Last Modified: Sat, 16 Mar 2024 03:21:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:2d7e2a96c2c05b43bb4863b418cbd7c72ddbb18241dec8d6af60584cc6a3b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:e5bb0c57c1d04693f959a8e5030d1debd19fc3834c02554d88730f230ad61e50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70606909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875396625bb009d15f75611a40237e4b47acab7c875bacee24e12835d5312315`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:12:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 06:12:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 10 Apr 2024 06:12:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:12:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 06:12:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 06:12:57 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 06:12:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 06:12:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 06:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:12:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88face1910ce69ec34060f54c8c3fe84e7222bce6553d8bafba11be1c29bd05c`  
		Last Modified: Wed, 10 Apr 2024 06:14:22 GMT  
		Size: 4.4 MB (4416526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a4c920d9b16a67bb24b99ac8840ad618f4c70ffaea524ffa1e7d465deef671`  
		Last Modified: Wed, 10 Apr 2024 06:14:25 GMT  
		Size: 34.7 MB (34738253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184843215a224488b90c5214cd713f920aa0f268be34ec1669db121db2f02b9c`  
		Last Modified: Wed, 10 Apr 2024 06:14:21 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104f94cbb2799f396b605368c7ae61a4d6d831d3991b9ad7200dcbfcea4270a2`  
		Last Modified: Wed, 10 Apr 2024 06:14:21 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91deac2952c5c9dd42ea714c555c17ddb01504a8394242e1a68e0cb674bee1f7`  
		Last Modified: Wed, 10 Apr 2024 06:14:21 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e45cd7040df4533c9e01b8c45e5ce168e9f9c1278d37748eb61273cf096ddf61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63430580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21c6b121a898fe9494afc90347429eafd27f05467fcf5cd476b6398b8e9f460`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:46 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Wed, 10 Apr 2024 00:58:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:42:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 07:42:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 10 Apr 2024 07:42:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:42:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 07:42:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 07:42:27 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 07:42:27 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 07:42:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 07:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 07:42:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faada9fa522013b8a1a266524e377651dfbca83db96198f4f2b090ca6b5c80e`  
		Last Modified: Wed, 10 Apr 2024 07:44:35 GMT  
		Size: 3.7 MB (3719108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810579cabe498b5254ad1c3fe91f1179d43105c0bd7c2919b6dfb8561c4b8860`  
		Last Modified: Wed, 10 Apr 2024 07:44:40 GMT  
		Size: 33.1 MB (33098601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2914b0eb2fbdd42b07144be068ee52c26f8009fb6b830ff6ec448a60bdbdf0`  
		Last Modified: Wed, 10 Apr 2024 07:44:34 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9240e7e77e8f329364b82e1fdc3771dfe23c69fc03b155f61595ee132dab22`  
		Last Modified: Wed, 10 Apr 2024 07:44:34 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b512145f05ef5d835924054099ec9d92bf8d1d0c27b1ff4a540ec83f2e9e15`  
		Last Modified: Wed, 10 Apr 2024 07:44:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6befd39998e5d870129cc15f488fb7669d27d3296b40c8cde2d3145fc8e84d9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67757495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56afebb541026b9a0fa9335e1aed6751ee2e1ad42cae863fa8eb444353ff4edc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:18:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 04:18:44 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 10 Apr 2024 04:18:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:18:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 04:18:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 04:18:52 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 04:18:52 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 04:18:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 04:18:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 04:18:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d102b38495044d201497a094d1bf588efa76d1d2455dcbdcf3cbcd4e5c14b5e8`  
		Last Modified: Wed, 10 Apr 2024 04:19:51 GMT  
		Size: 4.4 MB (4418033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8478cf9b8501cc3c27958138050801f9722cd1ab47e685aa7b032c0450a4d7`  
		Last Modified: Wed, 10 Apr 2024 04:19:54 GMT  
		Size: 33.2 MB (33238759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d42982428d3db19c37af0bd36adcb4f965c5abee8372694f2f7f86d5a42c99e`  
		Last Modified: Wed, 10 Apr 2024 04:19:50 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede81af1d6e393961094e13a552bdba1571d1f3cfb47dcff2a383c1f541d6c50`  
		Last Modified: Wed, 10 Apr 2024 04:19:51 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae81ab0cc33207fe93243ff9c633388e33f8ba3ed6aec4b13b8c668937690e0c`  
		Last Modified: Wed, 10 Apr 2024 04:19:50 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:7cc77100ae752f9c44461fe06b8aeee4d2bc196a7600f33aecfbe22d60da8df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ff6e911fb57a1c911356978496ae4e19ce5a0071aa819daed26437c635ab9dbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23246247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591c051e96ac4e4633bc4f6731af433d301e815e3568351cf4e532609a3921a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:06 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 16 Mar 2024 03:20:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:12 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:12 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938fcaa198dc21c9b821d611166b80842631f50fe715a8f272172cafe3176814`  
		Last Modified: Sat, 16 Mar 2024 03:21:14 GMT  
		Size: 19.6 MB (19557218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266bc6e6efce66b509e7e8eca65e5ce23597892fb4f4560ce39cc6b2aad485d`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecf86d2f3fd6fc7c346b9659e0544173a1f9ab6b9aea84772c67cbb86bb4a3b`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e40de9b3fe95133a27a754000d8ba962b35b7bbf336e140ed9094c463b2073`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:2d7e2a96c2c05b43bb4863b418cbd7c72ddbb18241dec8d6af60584cc6a3b4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:e5bb0c57c1d04693f959a8e5030d1debd19fc3834c02554d88730f230ad61e50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70606909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875396625bb009d15f75611a40237e4b47acab7c875bacee24e12835d5312315`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:12:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 06:12:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 10 Apr 2024 06:12:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:12:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 06:12:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 06:12:57 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 06:12:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 06:12:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 06:12:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:12:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88face1910ce69ec34060f54c8c3fe84e7222bce6553d8bafba11be1c29bd05c`  
		Last Modified: Wed, 10 Apr 2024 06:14:22 GMT  
		Size: 4.4 MB (4416526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a4c920d9b16a67bb24b99ac8840ad618f4c70ffaea524ffa1e7d465deef671`  
		Last Modified: Wed, 10 Apr 2024 06:14:25 GMT  
		Size: 34.7 MB (34738253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184843215a224488b90c5214cd713f920aa0f268be34ec1669db121db2f02b9c`  
		Last Modified: Wed, 10 Apr 2024 06:14:21 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104f94cbb2799f396b605368c7ae61a4d6d831d3991b9ad7200dcbfcea4270a2`  
		Last Modified: Wed, 10 Apr 2024 06:14:21 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91deac2952c5c9dd42ea714c555c17ddb01504a8394242e1a68e0cb674bee1f7`  
		Last Modified: Wed, 10 Apr 2024 06:14:21 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e45cd7040df4533c9e01b8c45e5ce168e9f9c1278d37748eb61273cf096ddf61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63430580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21c6b121a898fe9494afc90347429eafd27f05467fcf5cd476b6398b8e9f460`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:46 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Wed, 10 Apr 2024 00:58:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:42:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 07:42:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 10 Apr 2024 07:42:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:42:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 07:42:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 07:42:27 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 07:42:27 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 07:42:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 07:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 07:42:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faada9fa522013b8a1a266524e377651dfbca83db96198f4f2b090ca6b5c80e`  
		Last Modified: Wed, 10 Apr 2024 07:44:35 GMT  
		Size: 3.7 MB (3719108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810579cabe498b5254ad1c3fe91f1179d43105c0bd7c2919b6dfb8561c4b8860`  
		Last Modified: Wed, 10 Apr 2024 07:44:40 GMT  
		Size: 33.1 MB (33098601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2914b0eb2fbdd42b07144be068ee52c26f8009fb6b830ff6ec448a60bdbdf0`  
		Last Modified: Wed, 10 Apr 2024 07:44:34 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9240e7e77e8f329364b82e1fdc3771dfe23c69fc03b155f61595ee132dab22`  
		Last Modified: Wed, 10 Apr 2024 07:44:34 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b512145f05ef5d835924054099ec9d92bf8d1d0c27b1ff4a540ec83f2e9e15`  
		Last Modified: Wed, 10 Apr 2024 07:44:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6befd39998e5d870129cc15f488fb7669d27d3296b40c8cde2d3145fc8e84d9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67757495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56afebb541026b9a0fa9335e1aed6751ee2e1ad42cae863fa8eb444353ff4edc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:18:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 04:18:44 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 10 Apr 2024 04:18:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:18:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 04:18:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 04:18:52 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 04:18:52 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 04:18:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 04:18:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 04:18:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d102b38495044d201497a094d1bf588efa76d1d2455dcbdcf3cbcd4e5c14b5e8`  
		Last Modified: Wed, 10 Apr 2024 04:19:51 GMT  
		Size: 4.4 MB (4418033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8478cf9b8501cc3c27958138050801f9722cd1ab47e685aa7b032c0450a4d7`  
		Last Modified: Wed, 10 Apr 2024 04:19:54 GMT  
		Size: 33.2 MB (33238759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d42982428d3db19c37af0bd36adcb4f965c5abee8372694f2f7f86d5a42c99e`  
		Last Modified: Wed, 10 Apr 2024 04:19:50 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede81af1d6e393961094e13a552bdba1571d1f3cfb47dcff2a383c1f541d6c50`  
		Last Modified: Wed, 10 Apr 2024 04:19:51 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae81ab0cc33207fe93243ff9c633388e33f8ba3ed6aec4b13b8c668937690e0c`  
		Last Modified: Wed, 10 Apr 2024 04:19:50 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:7cc77100ae752f9c44461fe06b8aeee4d2bc196a7600f33aecfbe22d60da8df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ff6e911fb57a1c911356978496ae4e19ce5a0071aa819daed26437c635ab9dbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23246247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591c051e96ac4e4633bc4f6731af433d301e815e3568351cf4e532609a3921a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:06 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Sat, 16 Mar 2024 03:20:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:11 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:12 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:12 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938fcaa198dc21c9b821d611166b80842631f50fe715a8f272172cafe3176814`  
		Last Modified: Sat, 16 Mar 2024 03:21:14 GMT  
		Size: 19.6 MB (19557218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266bc6e6efce66b509e7e8eca65e5ce23597892fb4f4560ce39cc6b2aad485d`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecf86d2f3fd6fc7c346b9659e0544173a1f9ab6b9aea84772c67cbb86bb4a3b`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e40de9b3fe95133a27a754000d8ba962b35b7bbf336e140ed9094c463b2073`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:e2a14a22a238e6c7895b528d7bbc843f073ceaa1d401bd37771d5ef9206ee3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:77006f95484835b9a771b4a8a914c11377e2cbc1593c6a94bf664530d5536cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71258731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b53d392cd130b0fb035391dc58ea2b63bd9b04605b09865b820eb8d2133023`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:13:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 06:13:12 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 10 Apr 2024 06:13:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:13:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 06:13:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 06:13:20 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 06:13:20 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 06:13:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 06:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:13:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb63b5d213626bf6fe47af0cf35c9acde544f52f8060daca7e97dc16eb1f8e8`  
		Last Modified: Wed, 10 Apr 2024 06:14:36 GMT  
		Size: 5.2 MB (5226493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bced2cf78b545716590c2bdb9ff7226fb08bfffdd15ddd6a0a47f5ea6d1188`  
		Last Modified: Wed, 10 Apr 2024 06:14:39 GMT  
		Size: 34.6 MB (34580105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317b3b3c112d487d295d4bfd464163d8a39b1fafad195b25d552de3209e469e`  
		Last Modified: Wed, 10 Apr 2024 06:14:35 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579d7e4eee3eedad3a3dde30a0ee080d2cfe945954aeac4fc73a81f32e1bb992`  
		Last Modified: Wed, 10 Apr 2024 06:14:35 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229d7e32f8f7a10bf885f2bf46a6aa9ddce2543c306382860c9ea8fb894cf0d6`  
		Last Modified: Wed, 10 Apr 2024 06:14:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d3cb6cd35ded06675b0b7e07df1249ac879ecea6bf34991125946f48be04754f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63856324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8edf29b629a933bebd674bac014931b5b4f4d33700844eacdcdd2f812c27600`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:46 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Wed, 10 Apr 2024 00:58:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:42:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 07:42:55 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 10 Apr 2024 07:43:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:43:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 07:43:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 07:43:08 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 07:43:08 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 07:43:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 07:43:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 07:43:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa8730c2a259b1c7efadb92f0dbb035ad0d934270c78b748877c80dc62ac9ee`  
		Last Modified: Wed, 10 Apr 2024 07:44:50 GMT  
		Size: 4.5 MB (4492172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a539dcba89e9f1f3bb89a912063e52c4c7cdb677ca8bdc4b65d3649133552`  
		Last Modified: Wed, 10 Apr 2024 07:44:55 GMT  
		Size: 32.8 MB (32751281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74a5761e0395ba414073ded04490a028578dbd2b9d1c18b98cb43f6af622e2`  
		Last Modified: Wed, 10 Apr 2024 07:44:48 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddad8b667ff6bb2c713b0fe4c4dbff7383e9fa9c900d3f44cef0b8a5458af3e`  
		Last Modified: Wed, 10 Apr 2024 07:44:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284db0e9054c829c98b8d2238083b37f07808b241431cb85e67b251c51623cce`  
		Last Modified: Wed, 10 Apr 2024 07:44:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:328f13e45f1bddf57d29dec5f9effa41825958b5f42e123dd426529e2a162d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67955452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9741690d9a65f3d36a6c506b7d4b5d43819b29bc443e96873b062225a3e9a806`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:19:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 04:19:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 10 Apr 2024 04:19:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:19:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 04:19:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 04:19:09 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 04:19:09 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 04:19:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 04:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 04:19:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb2206bcb33a196b583ebd35312146d93fcd45f7d038ef866c5e590d71bd51`  
		Last Modified: Wed, 10 Apr 2024 04:20:04 GMT  
		Size: 5.2 MB (5209533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f69e46c3482c2e32207f482a4953b62bfc38629d84943af3705d342f540595`  
		Last Modified: Wed, 10 Apr 2024 04:20:06 GMT  
		Size: 32.6 MB (32645227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bccfabd53ab2bac9836d50b8a4836fda391ba9dc23ccc48f14543e345c3203`  
		Last Modified: Wed, 10 Apr 2024 04:20:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e05d6df616400ebab7726c78fa64ca0089d6f78adf2dc0bfc282b365f68ba13`  
		Last Modified: Wed, 10 Apr 2024 04:20:03 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13005d6e4daf59c18c966f80a0e4ed3f23e7a8c33d525dc4678b80cd79917055`  
		Last Modified: Wed, 10 Apr 2024 04:20:03 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:f86b9c1882c523515c80d656b0ebdbf97d0591f86d4ad35b6c2d41af9d4d6e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4e405e1032ae084ea4091b135168c25b345399d30879e6aafbc3861de36d803e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22893187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76ad514ca513592ec7ac47b5fb9dc6c033299f933ff5b456706545a69b4b1d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:19 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 16 Mar 2024 03:20:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:25 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:25 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4cc01a94fafcaa370de6eb1d82920490e8b7bad16c2eaa40918e3a9fad57e1`  
		Last Modified: Sat, 16 Mar 2024 03:21:26 GMT  
		Size: 19.2 MB (19204158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2e39810281cb32653a738bf6e8e1949692a93c19dcc6ea1af683671af9f58c`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5290c71eb9dd78e6d62ced897c4ec0ba8880d660722b1e56a6b8769ca100841`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac68863d78379d68261e2d0188f4da0241ac15bf7d368e2a034e5639eadc08`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:e2a14a22a238e6c7895b528d7bbc843f073ceaa1d401bd37771d5ef9206ee3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:77006f95484835b9a771b4a8a914c11377e2cbc1593c6a94bf664530d5536cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71258731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b53d392cd130b0fb035391dc58ea2b63bd9b04605b09865b820eb8d2133023`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:13:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 06:13:12 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 10 Apr 2024 06:13:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:13:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 06:13:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 06:13:20 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 06:13:20 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 06:13:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 06:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:13:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb63b5d213626bf6fe47af0cf35c9acde544f52f8060daca7e97dc16eb1f8e8`  
		Last Modified: Wed, 10 Apr 2024 06:14:36 GMT  
		Size: 5.2 MB (5226493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bced2cf78b545716590c2bdb9ff7226fb08bfffdd15ddd6a0a47f5ea6d1188`  
		Last Modified: Wed, 10 Apr 2024 06:14:39 GMT  
		Size: 34.6 MB (34580105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317b3b3c112d487d295d4bfd464163d8a39b1fafad195b25d552de3209e469e`  
		Last Modified: Wed, 10 Apr 2024 06:14:35 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579d7e4eee3eedad3a3dde30a0ee080d2cfe945954aeac4fc73a81f32e1bb992`  
		Last Modified: Wed, 10 Apr 2024 06:14:35 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229d7e32f8f7a10bf885f2bf46a6aa9ddce2543c306382860c9ea8fb894cf0d6`  
		Last Modified: Wed, 10 Apr 2024 06:14:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d3cb6cd35ded06675b0b7e07df1249ac879ecea6bf34991125946f48be04754f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63856324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8edf29b629a933bebd674bac014931b5b4f4d33700844eacdcdd2f812c27600`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:46 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Wed, 10 Apr 2024 00:58:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:42:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 07:42:55 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 10 Apr 2024 07:43:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:43:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 07:43:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 07:43:08 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 07:43:08 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 07:43:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 07:43:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 07:43:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa8730c2a259b1c7efadb92f0dbb035ad0d934270c78b748877c80dc62ac9ee`  
		Last Modified: Wed, 10 Apr 2024 07:44:50 GMT  
		Size: 4.5 MB (4492172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a539dcba89e9f1f3bb89a912063e52c4c7cdb677ca8bdc4b65d3649133552`  
		Last Modified: Wed, 10 Apr 2024 07:44:55 GMT  
		Size: 32.8 MB (32751281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74a5761e0395ba414073ded04490a028578dbd2b9d1c18b98cb43f6af622e2`  
		Last Modified: Wed, 10 Apr 2024 07:44:48 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddad8b667ff6bb2c713b0fe4c4dbff7383e9fa9c900d3f44cef0b8a5458af3e`  
		Last Modified: Wed, 10 Apr 2024 07:44:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284db0e9054c829c98b8d2238083b37f07808b241431cb85e67b251c51623cce`  
		Last Modified: Wed, 10 Apr 2024 07:44:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:328f13e45f1bddf57d29dec5f9effa41825958b5f42e123dd426529e2a162d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67955452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9741690d9a65f3d36a6c506b7d4b5d43819b29bc443e96873b062225a3e9a806`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:19:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 04:19:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 10 Apr 2024 04:19:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:19:09 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 04:19:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 04:19:09 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 04:19:09 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 04:19:09 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 04:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 04:19:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb2206bcb33a196b583ebd35312146d93fcd45f7d038ef866c5e590d71bd51`  
		Last Modified: Wed, 10 Apr 2024 04:20:04 GMT  
		Size: 5.2 MB (5209533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f69e46c3482c2e32207f482a4953b62bfc38629d84943af3705d342f540595`  
		Last Modified: Wed, 10 Apr 2024 04:20:06 GMT  
		Size: 32.6 MB (32645227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bccfabd53ab2bac9836d50b8a4836fda391ba9dc23ccc48f14543e345c3203`  
		Last Modified: Wed, 10 Apr 2024 04:20:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e05d6df616400ebab7726c78fa64ca0089d6f78adf2dc0bfc282b365f68ba13`  
		Last Modified: Wed, 10 Apr 2024 04:20:03 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13005d6e4daf59c18c966f80a0e4ed3f23e7a8c33d525dc4678b80cd79917055`  
		Last Modified: Wed, 10 Apr 2024 04:20:03 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:f86b9c1882c523515c80d656b0ebdbf97d0591f86d4ad35b6c2d41af9d4d6e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4e405e1032ae084ea4091b135168c25b345399d30879e6aafbc3861de36d803e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22893187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76ad514ca513592ec7ac47b5fb9dc6c033299f933ff5b456706545a69b4b1d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:19 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Sat, 16 Mar 2024 03:20:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:25 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:25 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:25 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4cc01a94fafcaa370de6eb1d82920490e8b7bad16c2eaa40918e3a9fad57e1`  
		Last Modified: Sat, 16 Mar 2024 03:21:26 GMT  
		Size: 19.2 MB (19204158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2e39810281cb32653a738bf6e8e1949692a93c19dcc6ea1af683671af9f58c`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5290c71eb9dd78e6d62ced897c4ec0ba8880d660722b1e56a6b8769ca100841`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eac68863d78379d68261e2d0188f4da0241ac15bf7d368e2a034e5639eadc08`  
		Last Modified: Sat, 16 Mar 2024 03:21:23 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:d67e2bb7181bc4bc809c39e99e512b6bc6e10942beb24fb67a677d4bac505d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:36dff18a19d1e5ddf7c03dcb9f62bf729da49457bfe36d928680f00c7c6a1ede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71905999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2053f021d6c894774957408b19b025c4637a5d3162e91121d2d6c50a178460`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:13:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 06:13:28 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 10 Apr 2024 06:13:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:13:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 06:13:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 06:13:39 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 06:13:39 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 06:13:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 06:13:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:13:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb63b5d213626bf6fe47af0cf35c9acde544f52f8060daca7e97dc16eb1f8e8`  
		Last Modified: Wed, 10 Apr 2024 06:14:36 GMT  
		Size: 5.2 MB (5226493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd70fbd04436e2ad9ba2a24ed6a83258488c3516d2debd28405538db08b5808c`  
		Last Modified: Wed, 10 Apr 2024 06:14:53 GMT  
		Size: 35.2 MB (35227377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57fda35129c4afc60887c92ce78bce828c788c8affa21f975d0af8e34d5e9fb`  
		Last Modified: Wed, 10 Apr 2024 06:14:48 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142cfe0828cff0010c6977456998c717345f01cb279d213ddd8791f50bc42d5b`  
		Last Modified: Wed, 10 Apr 2024 06:14:48 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b9f1edc1bdfbe80a04fc2ddc27c9de2dd1ae58d892b9a1c0a816ae557b74d5`  
		Last Modified: Wed, 10 Apr 2024 06:14:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b3f9e75a71531cdc7616011ece615ee95961fc92a8c2b579ff9d82b81933fc84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64632530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b000710d166031784e2d6a2d7c39ec6a7a2cfc950fc153705e110cadcbd41b48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:46 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Wed, 10 Apr 2024 00:58:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:42:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 07:43:14 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 10 Apr 2024 07:43:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:43:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 07:43:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 07:43:28 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 07:43:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 07:43:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 07:43:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 07:43:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa8730c2a259b1c7efadb92f0dbb035ad0d934270c78b748877c80dc62ac9ee`  
		Last Modified: Wed, 10 Apr 2024 07:44:50 GMT  
		Size: 4.5 MB (4492172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1536d4799efe2b8584f4de68849a18bc3dd3508025fcac46c8ae93b7e6f5ebc2`  
		Last Modified: Wed, 10 Apr 2024 07:45:09 GMT  
		Size: 33.5 MB (33527489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b106a16f96555e5c6f5d83cbc8b61f852932f6e4fc94db7483db5479b7b98d5`  
		Last Modified: Wed, 10 Apr 2024 07:45:03 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328b50fcf4b925bf5c8e1f3de3e42d5cec81f8787f2bea487e7080285f17e326`  
		Last Modified: Wed, 10 Apr 2024 07:45:03 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79150cbcb6566e181e8896e2015fb77edc2073596f46fbf1491d93a9cf7945c1`  
		Last Modified: Wed, 10 Apr 2024 07:45:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:cb85373be7887fb45a84a1b8da5d7c5572e222d08d61c0239b435481215bcf7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68707725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a136f67b5e214b9bf720e4b20bed27e356598621b93e0268950cf51744708e96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:19:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 04:19:12 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 10 Apr 2024 04:19:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:19:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 04:19:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 04:19:19 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 04:19:19 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 04:19:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 04:19:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 04:19:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb2206bcb33a196b583ebd35312146d93fcd45f7d038ef866c5e590d71bd51`  
		Last Modified: Wed, 10 Apr 2024 04:20:04 GMT  
		Size: 5.2 MB (5209533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b240dd6f81756a67300748b440ac70d32b798d709f7ce8f707aea189892fd71`  
		Last Modified: Wed, 10 Apr 2024 04:20:17 GMT  
		Size: 33.4 MB (33397500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6823ea972fb44c8c8cbced007534575dfe3edc3b3b114dab7e7bf6cf996707`  
		Last Modified: Wed, 10 Apr 2024 04:20:14 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e1b3e66ea559167f24e338b96b2b7decbdd4f20770394ded6c224af48041f1`  
		Last Modified: Wed, 10 Apr 2024 04:20:15 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3dffbe0ae27e3306ba4f446fd8d2bfb41c0d784d42881f673bd861a9d8af37`  
		Last Modified: Wed, 10 Apr 2024 04:20:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:58038f3e5f95b38efbe31e2dd8c7b7c0da7a926da9b6ee6845699869095111a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c25d48417f45446f783c5adf64c42c1d76444df716f79ea61f71db2172028923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23361283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cd392d9f55a4830d355e0f9b6d013cadc65691db4951a14030c9261717c704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 16 Mar 2024 03:20:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:38 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:38 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ad7820274585078b0e98dff9ca0a6a138b48fa805200be362ae835e55d935e`  
		Last Modified: Sat, 16 Mar 2024 03:21:38 GMT  
		Size: 19.7 MB (19672268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10615eac7f71b29e6e8a49969cc83939de885312ca46c1b7c853a6986226fc1d`  
		Last Modified: Sat, 16 Mar 2024 03:21:35 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4992ddaf3fbc8a86cae023d8a55729ea8c144f3fd64ce6429f512019224862f`  
		Last Modified: Sat, 16 Mar 2024 03:21:35 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e62fadc79b84d0c222bb06eb7e644dd0ab83db94c3bcc9ebe9067fca5a45b4`  
		Last Modified: Sat, 16 Mar 2024 03:21:34 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:d67e2bb7181bc4bc809c39e99e512b6bc6e10942beb24fb67a677d4bac505d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:36dff18a19d1e5ddf7c03dcb9f62bf729da49457bfe36d928680f00c7c6a1ede
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71905999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2053f021d6c894774957408b19b025c4637a5d3162e91121d2d6c50a178460`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:13:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 06:13:28 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 10 Apr 2024 06:13:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:13:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 06:13:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 06:13:39 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 06:13:39 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 06:13:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 06:13:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:13:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb63b5d213626bf6fe47af0cf35c9acde544f52f8060daca7e97dc16eb1f8e8`  
		Last Modified: Wed, 10 Apr 2024 06:14:36 GMT  
		Size: 5.2 MB (5226493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd70fbd04436e2ad9ba2a24ed6a83258488c3516d2debd28405538db08b5808c`  
		Last Modified: Wed, 10 Apr 2024 06:14:53 GMT  
		Size: 35.2 MB (35227377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57fda35129c4afc60887c92ce78bce828c788c8affa21f975d0af8e34d5e9fb`  
		Last Modified: Wed, 10 Apr 2024 06:14:48 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142cfe0828cff0010c6977456998c717345f01cb279d213ddd8791f50bc42d5b`  
		Last Modified: Wed, 10 Apr 2024 06:14:48 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b9f1edc1bdfbe80a04fc2ddc27c9de2dd1ae58d892b9a1c0a816ae557b74d5`  
		Last Modified: Wed, 10 Apr 2024 06:14:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b3f9e75a71531cdc7616011ece615ee95961fc92a8c2b579ff9d82b81933fc84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64632530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b000710d166031784e2d6a2d7c39ec6a7a2cfc950fc153705e110cadcbd41b48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:46 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Wed, 10 Apr 2024 00:58:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:42:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 07:43:14 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 10 Apr 2024 07:43:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:43:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 07:43:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 07:43:28 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 07:43:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 07:43:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 07:43:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 07:43:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa8730c2a259b1c7efadb92f0dbb035ad0d934270c78b748877c80dc62ac9ee`  
		Last Modified: Wed, 10 Apr 2024 07:44:50 GMT  
		Size: 4.5 MB (4492172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1536d4799efe2b8584f4de68849a18bc3dd3508025fcac46c8ae93b7e6f5ebc2`  
		Last Modified: Wed, 10 Apr 2024 07:45:09 GMT  
		Size: 33.5 MB (33527489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b106a16f96555e5c6f5d83cbc8b61f852932f6e4fc94db7483db5479b7b98d5`  
		Last Modified: Wed, 10 Apr 2024 07:45:03 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328b50fcf4b925bf5c8e1f3de3e42d5cec81f8787f2bea487e7080285f17e326`  
		Last Modified: Wed, 10 Apr 2024 07:45:03 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79150cbcb6566e181e8896e2015fb77edc2073596f46fbf1491d93a9cf7945c1`  
		Last Modified: Wed, 10 Apr 2024 07:45:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:cb85373be7887fb45a84a1b8da5d7c5572e222d08d61c0239b435481215bcf7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68707725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a136f67b5e214b9bf720e4b20bed27e356598621b93e0268950cf51744708e96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:19:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 04:19:12 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 10 Apr 2024 04:19:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:19:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 04:19:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 04:19:19 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 04:19:19 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 04:19:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 04:19:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 04:19:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb2206bcb33a196b583ebd35312146d93fcd45f7d038ef866c5e590d71bd51`  
		Last Modified: Wed, 10 Apr 2024 04:20:04 GMT  
		Size: 5.2 MB (5209533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b240dd6f81756a67300748b440ac70d32b798d709f7ce8f707aea189892fd71`  
		Last Modified: Wed, 10 Apr 2024 04:20:17 GMT  
		Size: 33.4 MB (33397500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6823ea972fb44c8c8cbced007534575dfe3edc3b3b114dab7e7bf6cf996707`  
		Last Modified: Wed, 10 Apr 2024 04:20:14 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e1b3e66ea559167f24e338b96b2b7decbdd4f20770394ded6c224af48041f1`  
		Last Modified: Wed, 10 Apr 2024 04:20:15 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3dffbe0ae27e3306ba4f446fd8d2bfb41c0d784d42881f673bd861a9d8af37`  
		Last Modified: Wed, 10 Apr 2024 04:20:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:58038f3e5f95b38efbe31e2dd8c7b7c0da7a926da9b6ee6845699869095111a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c25d48417f45446f783c5adf64c42c1d76444df716f79ea61f71db2172028923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23361283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cd392d9f55a4830d355e0f9b6d013cadc65691db4951a14030c9261717c704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:06 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Sat, 16 Mar 2024 03:20:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:38 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:38 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:38 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485cfb0fb6cd4129a6e7d303f3ebec56b5c133689199b5426db52a97cdafd15a`  
		Last Modified: Sat, 16 Mar 2024 03:21:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98004ffc28465fb13a09790c0b8d8af0ed002fa6fa8a93c0bfc098bb1862afb1`  
		Last Modified: Sat, 16 Mar 2024 03:21:11 GMT  
		Size: 284.9 KB (284942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ad7820274585078b0e98dff9ca0a6a138b48fa805200be362ae835e55d935e`  
		Last Modified: Sat, 16 Mar 2024 03:21:38 GMT  
		Size: 19.7 MB (19672268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10615eac7f71b29e6e8a49969cc83939de885312ca46c1b7c853a6986226fc1d`  
		Last Modified: Sat, 16 Mar 2024 03:21:35 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4992ddaf3fbc8a86cae023d8a55729ea8c144f3fd64ce6429f512019224862f`  
		Last Modified: Sat, 16 Mar 2024 03:21:35 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e62fadc79b84d0c222bb06eb7e644dd0ab83db94c3bcc9ebe9067fca5a45b4`  
		Last Modified: Sat, 16 Mar 2024 03:21:34 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:7d96aada68f7a3b98895d0faeea984baba66af1b2808dba9f6d0521c8b5a944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a3afdd4ea86424100f3db85c4c76756f9b0b86d409211ffb730ee64340df2c08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31566092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d628147ca6e52b9a6e841c074d13321cbfb2cbb3f6427f8a3b5ea41f6aa9da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 03:20:47 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Sat, 16 Mar 2024 03:20:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 03:20:54 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 16 Mar 2024 03:20:54 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 16 Mar 2024 03:20:54 GMT
EXPOSE 8888
# Sat, 16 Mar 2024 03:20:54 GMT
VOLUME [/var/lib/chronograf]
# Sat, 16 Mar 2024 03:20:54 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Sat, 16 Mar 2024 03:20:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 03:20:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377633fb5fdd007c0931220a6d839bb8682cccad8022dfb9d9a6a13f48bbcb31`  
		Last Modified: Sat, 16 Mar 2024 03:21:47 GMT  
		Size: 284.7 KB (284701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f9378d075e5479db8cee400626beec3637332abd781326a69cb1c2173ffd8e`  
		Last Modified: Sat, 16 Mar 2024 03:21:52 GMT  
		Size: 27.9 MB (27854172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68a198732915ac9a64b856384eef314de7974b3cca48446018aa151e50d6148`  
		Last Modified: Sat, 16 Mar 2024 03:21:46 GMT  
		Size: 12.3 KB (12262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ce7d3e21fb69d974a79be54d2cd4667472c50ccf5a30c31c037687cfef4e6e`  
		Last Modified: Sat, 16 Mar 2024 03:21:46 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48216b42c8c48a5aebdd1f2d1009c957b6c0b3d86efa905e6f3d5143ae03fe5`  
		Last Modified: Sat, 16 Mar 2024 03:21:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:e429b94893f07a776ad6a99a2cb3bc9d3c35f760264de0754d454a372df2a48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:2e40d41b813ba900e66202581eacf7aedde0dd170dac5eb3c23717a1c7b0c9da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84088157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d7c71cc1be8579e816a6863034273d54dd892ca8ebef89a7c6c6c27aef32b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:13:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 06:13:53 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 10 Apr 2024 06:14:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:14:02 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 06:14:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 06:14:02 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 06:14:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 06:14:02 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 06:14:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:14:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10cf296e0e4c72f988a9c65f96602201aa59c2dc799b45e216055ace05c353c`  
		Last Modified: Wed, 10 Apr 2024 06:15:03 GMT  
		Size: 7.9 MB (7870385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7737e84fb59431d887d46c7e502391f0bb486024e9ae6a467f4984a960c218`  
		Last Modified: Wed, 10 Apr 2024 06:15:08 GMT  
		Size: 47.1 MB (47062023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a51405fbcdf2623ccb035d828b11dee3a02c6da0d140c094803983bac43189f`  
		Last Modified: Wed, 10 Apr 2024 06:15:02 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a95afc221d3a6d898fdbe1e368bba4d948fbe8d96659bd8c50ca531ba9eca0`  
		Last Modified: Wed, 10 Apr 2024 06:15:02 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9161c2be5d42be6f57dd01808a23d8b6ce4fc87cabfc121efacde92b598b2673`  
		Last Modified: Wed, 10 Apr 2024 06:15:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d263edc5bb074544e4bcbfcee26e85421e62a4cd6a3f6867785ecc1ca469ea9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75894357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db3e801b8d5f016c6d35b3c15e2229d24b17fd4f762aa6615a518c74a797073`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:11 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Wed, 10 Apr 2024 00:58:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:43:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 07:43:52 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 10 Apr 2024 07:44:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:44:10 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 07:44:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 07:44:11 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 07:44:11 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 07:44:12 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 07:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 07:44:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4f25b4ac6372ba346d6434625f83dba4e6ee2fb3c4e00140bfa4a41a2cf6ef`  
		Last Modified: Wed, 10 Apr 2024 07:45:19 GMT  
		Size: 6.5 MB (6495016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232a5311219bba33d66c91a4cff6e1f1a8d15cd0796ac56340bd239300a22fd9`  
		Last Modified: Wed, 10 Apr 2024 07:45:27 GMT  
		Size: 44.7 MB (44652023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ae1395d57960ff15937d7afac04153a74586dacb0b15396c9a0130b247671`  
		Last Modified: Wed, 10 Apr 2024 07:45:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b64a4d1a58e41999509949dddc867b89613eaad3478cf4bf2c5d49e7a382ce`  
		Last Modified: Wed, 10 Apr 2024 07:45:18 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505a9ebaa15449db4334510c3d75ac368f7fb45508f1e86d4ce26da067b76ce3`  
		Last Modified: Wed, 10 Apr 2024 07:45:18 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:d6e9f583e1199c357877b35cbf747c643feeb0fabc70a6320bbb04904e601c5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81624175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2dcaafa57f86a500a0e86c62a5de0d6604e91baad421aa5616a213a35ad552`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:19:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 04:19:29 GMT
ENV CHRONOGRAF_VERSION=1.10.3
# Wed, 10 Apr 2024 04:19:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:19:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 10 Apr 2024 04:19:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 10 Apr 2024 04:19:38 GMT
EXPOSE 8888
# Wed, 10 Apr 2024 04:19:38 GMT
VOLUME [/var/lib/chronograf]
# Wed, 10 Apr 2024 04:19:38 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 10 Apr 2024 04:19:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 04:19:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1d7d8a6358c8838e0104fe26f761cec05931d76d43a89886e83755c7c93013`  
		Last Modified: Wed, 10 Apr 2024 04:20:27 GMT  
		Size: 7.6 MB (7647268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb101624a62824ae74c02a3fc4eb1a3c15aa41d78b2dc7f70126ec26bd33d3d`  
		Last Modified: Wed, 10 Apr 2024 04:20:30 GMT  
		Size: 44.8 MB (44790363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f38fdbad0ac3c099da75e00b19bb8657d2c51c525bb15f8ce2eb06b073e284`  
		Last Modified: Wed, 10 Apr 2024 04:20:25 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3111c51e3444ff352a97f3b75a7f241357c137d2207495b86e0baeae8f25e2c1`  
		Last Modified: Wed, 10 Apr 2024 04:20:25 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d40a8ebbb32e9b50b0f4b1d95898be2da8eec6975abb4506d863ee57f35454`  
		Last Modified: Wed, 10 Apr 2024 04:20:26 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
