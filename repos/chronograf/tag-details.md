<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.5`](#chronograf1105)
-	[`chronograf:1.10.5-alpine`](#chronograf1105-alpine)
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
$ docker pull chronograf@sha256:bc97d8bd9b619b8188a7cec64bb4787ca46efa0be66ea89e650e24ad702fc1c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:cbb2398ca1e9c1e79905f76a6f508c0b84e124ed19d8bd1ef329113df6bd0554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84245436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef430dd9bd942ea971170a9ad41a7b86bf2b0bd54963f64e172414e8bbf7b6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224e7e2d3fcfa467dc4f217326c057f4f2dd7300e13ef8f9e857ce39d3b4a1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 7.9 MB (7875383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156341f7966c50570025c0aa511f08d25d6323a659a42aed5dbf0d667f59476a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 47.2 MB (47217593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc833227a91630f06fdbd4aa78c70728725f847e7108c30819c0dd7b1bcc2f1`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942d7292f5707350b55e75b6962c10f687a2f79cd6897f52184d0d756f3640af`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b128af6ad42b6a2e4237a81330a24126fa56928cb1282247f5a0b2e934cce`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d283d9166d23e08f8f2ecab79a9506abca9aca59180582cf53a41af1716e8570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff9e10e6a0907fdc037209f268bd74095409b257480933f04b1cad3729d68f`

```dockerfile
```

-	Layers:
	-	`sha256:3e81168bed413e125218f95a0a4120c7164a7f95a704ffc312fa47035416659c`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 2.7 MB (2706777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da14de2590a125267c353c750cc1c061c345a17e9a5da32b3651a9e5dc1c2ec`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:13a78f4c253093cf30fca5c89c1bb696e1fc682c1b7810e70e5a4c3ed0cc5151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75516412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d71adce3a94e5289bac0d13f5cc4efb87d068f50d800592bc297e2793cbe9ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a2e66a49258f3d38a009ec8390c0ca30e9b21e10c1f97f033935a3cc5547d`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 6.5 MB (6497599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab246a3e9d45eb0ec1e5d6429010eebe6b5030c07dbb87501a3ceca74ea685b9`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 44.3 MB (44276153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6311c1ec06eb271b214b2fb3b0ec782a808c8ccbf31c6753f73123807ef5811`  
		Last Modified: Thu, 17 Oct 2024 06:28:45 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6079489fc1564886a6fb52e0420b2c1478c533f5d728c5f252a9020d11ff0a`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f8925067ffa8213682865f92f9c8e961b3a242bf92478a328aa37bafa4db9b`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:4d5d473389d12da9d271eb185b6a74cb3f4555b5f0067cca46a140fa3143c38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837b3ca99f4b4f58ae00c768cdda7420b29c4d4adbb04fe379004c82e8e8019a`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9dce96a65ba948929d290d404f8baa6920851fe61442b3dddea26a887d674`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 2.7 MB (2693256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6257c8555aefbf425ff0fc7ba80af9cfaff204b57d960f0c1ed989a1ea96928`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 16.0 KB (16047 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8fb487b848793c15136e02fc531d8a600c1dbe1ec7f1e418a2e5aea62ed7a608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81802481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dea180108a03c10165a2e50c3cbc5225dadc03aa48168a2036fb7bc765d5005`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb962cc4d13593ec1e24aa00be579a90629298b3683b14cae17fb4a8c2fe8380`  
		Last Modified: Thu, 17 Oct 2024 07:53:09 GMT  
		Size: 7.7 MB (7651303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200d97f9a1d8c647ce3047b313528d76f945a2926ad045b195e466d07555aaba`  
		Last Modified: Thu, 17 Oct 2024 07:53:10 GMT  
		Size: 45.0 MB (44970383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1878e31ec9c4489a3f688ef4d78f6e5ecf3a69d2cd8b6a9bbfdc90cee6ab6`  
		Last Modified: Thu, 17 Oct 2024 07:53:08 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f088a8bc8a57f96ba34779583e83565f82f1f269de5c2919c90cff4b146ea27`  
		Last Modified: Thu, 17 Oct 2024 07:53:08 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c773560ba85255bf61546e83fa0ce860ab100ea9a8f11a0a2b5b8447d834b0`  
		Last Modified: Thu, 17 Oct 2024 07:53:09 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:20c5461af83dfb820f38f35c139fb0b294b249b23c65840fd8e87e1bb7c4b1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89f10a644756e7e03f46303a18af6db2d8ff06de4416e4616c60a0d1adcd844`

```dockerfile
```

-	Layers:
	-	`sha256:88003a62b99096f1793d902b4a71d21463c3d6ad917e6cfbc59f5aa71c4a7059`  
		Last Modified: Thu, 17 Oct 2024 07:53:09 GMT  
		Size: 2.7 MB (2691232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3caa001d0cbf97f812f486c523302cbf267b994639b6dcab87ba924b738a63`  
		Last Modified: Thu, 17 Oct 2024 07:53:08 GMT  
		Size: 16.1 KB (16073 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:e917c05d49569ffc91363b69db1139b3aec3ea352d7e4ab116ac73b5276c1e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9177fbf8d1abc0941d457afc9b0e50767dab53c0fa38968d0935948927429e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31808028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbf6891fc635a202a911272984b230346ed88f7ed61e7c5b4e6699d84faef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85d2cc53952cb93e416bed6638ae8631ac933e78edf15edc8f453889c78a4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 292.6 KB (292626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8ac47ff12105d7e2e63bdfecfe44bad8e9ed2abbb6bf69e824e6185e38c30`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 27.9 MB (27866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e56c6035356fa99cb81386116d4e7f9647b9d607a8d8bf3c7bad00f71e5ae4`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404105c04126e648e925115b31e8503e9be79bff0ac07d22b960fce01cc68627`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2d0f282dc22ee43b73a0bfff8802169fb0b6a1285ee756c538a46c2ffc4303`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf8a567d3540090f865ac052c59bda542cc0aebd2c1ad4413eadd03d956c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 KB (257758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6ab8b16a87c767b2f89aa09b99f84a49a0f574642aff41a53d43e44085627d`

```dockerfile
```

-	Layers:
	-	`sha256:608de47fe583d55de96c34e4f648a275957c4723931f32f5bf45243c183b05fb`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 239.9 KB (239903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf620aebcdf5b9e70ca057c32bcd31da203ea2fc4f7048080488c8522073c0c`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:bc97d8bd9b619b8188a7cec64bb4787ca46efa0be66ea89e650e24ad702fc1c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.5` - linux; amd64

```console
$ docker pull chronograf@sha256:cbb2398ca1e9c1e79905f76a6f508c0b84e124ed19d8bd1ef329113df6bd0554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84245436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef430dd9bd942ea971170a9ad41a7b86bf2b0bd54963f64e172414e8bbf7b6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224e7e2d3fcfa467dc4f217326c057f4f2dd7300e13ef8f9e857ce39d3b4a1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 7.9 MB (7875383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156341f7966c50570025c0aa511f08d25d6323a659a42aed5dbf0d667f59476a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 47.2 MB (47217593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc833227a91630f06fdbd4aa78c70728725f847e7108c30819c0dd7b1bcc2f1`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942d7292f5707350b55e75b6962c10f687a2f79cd6897f52184d0d756f3640af`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b128af6ad42b6a2e4237a81330a24126fa56928cb1282247f5a0b2e934cce`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:d283d9166d23e08f8f2ecab79a9506abca9aca59180582cf53a41af1716e8570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff9e10e6a0907fdc037209f268bd74095409b257480933f04b1cad3729d68f`

```dockerfile
```

-	Layers:
	-	`sha256:3e81168bed413e125218f95a0a4120c7164a7f95a704ffc312fa47035416659c`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 2.7 MB (2706777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da14de2590a125267c353c750cc1c061c345a17e9a5da32b3651a9e5dc1c2ec`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:13a78f4c253093cf30fca5c89c1bb696e1fc682c1b7810e70e5a4c3ed0cc5151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75516412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d71adce3a94e5289bac0d13f5cc4efb87d068f50d800592bc297e2793cbe9ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a2e66a49258f3d38a009ec8390c0ca30e9b21e10c1f97f033935a3cc5547d`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 6.5 MB (6497599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab246a3e9d45eb0ec1e5d6429010eebe6b5030c07dbb87501a3ceca74ea685b9`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 44.3 MB (44276153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6311c1ec06eb271b214b2fb3b0ec782a808c8ccbf31c6753f73123807ef5811`  
		Last Modified: Thu, 17 Oct 2024 06:28:45 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6079489fc1564886a6fb52e0420b2c1478c533f5d728c5f252a9020d11ff0a`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f8925067ffa8213682865f92f9c8e961b3a242bf92478a328aa37bafa4db9b`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:4d5d473389d12da9d271eb185b6a74cb3f4555b5f0067cca46a140fa3143c38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837b3ca99f4b4f58ae00c768cdda7420b29c4d4adbb04fe379004c82e8e8019a`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9dce96a65ba948929d290d404f8baa6920851fe61442b3dddea26a887d674`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 2.7 MB (2693256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6257c8555aefbf425ff0fc7ba80af9cfaff204b57d960f0c1ed989a1ea96928`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 16.0 KB (16047 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8fb487b848793c15136e02fc531d8a600c1dbe1ec7f1e418a2e5aea62ed7a608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81802481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dea180108a03c10165a2e50c3cbc5225dadc03aa48168a2036fb7bc765d5005`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb962cc4d13593ec1e24aa00be579a90629298b3683b14cae17fb4a8c2fe8380`  
		Last Modified: Thu, 17 Oct 2024 07:53:09 GMT  
		Size: 7.7 MB (7651303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200d97f9a1d8c647ce3047b313528d76f945a2926ad045b195e466d07555aaba`  
		Last Modified: Thu, 17 Oct 2024 07:53:10 GMT  
		Size: 45.0 MB (44970383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1878e31ec9c4489a3f688ef4d78f6e5ecf3a69d2cd8b6a9bbfdc90cee6ab6`  
		Last Modified: Thu, 17 Oct 2024 07:53:08 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f088a8bc8a57f96ba34779583e83565f82f1f269de5c2919c90cff4b146ea27`  
		Last Modified: Thu, 17 Oct 2024 07:53:08 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c773560ba85255bf61546e83fa0ce860ab100ea9a8f11a0a2b5b8447d834b0`  
		Last Modified: Thu, 17 Oct 2024 07:53:09 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:20c5461af83dfb820f38f35c139fb0b294b249b23c65840fd8e87e1bb7c4b1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89f10a644756e7e03f46303a18af6db2d8ff06de4416e4616c60a0d1adcd844`

```dockerfile
```

-	Layers:
	-	`sha256:88003a62b99096f1793d902b4a71d21463c3d6ad917e6cfbc59f5aa71c4a7059`  
		Last Modified: Thu, 17 Oct 2024 07:53:09 GMT  
		Size: 2.7 MB (2691232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3caa001d0cbf97f812f486c523302cbf267b994639b6dcab87ba924b738a63`  
		Last Modified: Thu, 17 Oct 2024 07:53:08 GMT  
		Size: 16.1 KB (16073 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:e917c05d49569ffc91363b69db1139b3aec3ea352d7e4ab116ac73b5276c1e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9177fbf8d1abc0941d457afc9b0e50767dab53c0fa38968d0935948927429e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31808028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbf6891fc635a202a911272984b230346ed88f7ed61e7c5b4e6699d84faef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85d2cc53952cb93e416bed6638ae8631ac933e78edf15edc8f453889c78a4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 292.6 KB (292626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8ac47ff12105d7e2e63bdfecfe44bad8e9ed2abbb6bf69e824e6185e38c30`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 27.9 MB (27866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e56c6035356fa99cb81386116d4e7f9647b9d607a8d8bf3c7bad00f71e5ae4`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404105c04126e648e925115b31e8503e9be79bff0ac07d22b960fce01cc68627`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2d0f282dc22ee43b73a0bfff8802169fb0b6a1285ee756c538a46c2ffc4303`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf8a567d3540090f865ac052c59bda542cc0aebd2c1ad4413eadd03d956c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 KB (257758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6ab8b16a87c767b2f89aa09b99f84a49a0f574642aff41a53d43e44085627d`

```dockerfile
```

-	Layers:
	-	`sha256:608de47fe583d55de96c34e4f648a275957c4723931f32f5bf45243c183b05fb`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 239.9 KB (239903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf620aebcdf5b9e70ca057c32bcd31da203ea2fc4f7048080488c8522073c0c`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:7bcb9c589f055a2862cbb3f23b58505699952bb1b60f6a54362f4a7ff0536840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:2e049b9a32b3c7088f9c802f7923d91d4242c8ef07f8d1c5694c657730b344a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70218746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05d82d0aa19e8425c3e53f13b83e8901ef2d875a7ddc5bf7348a6e80d68e438`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd178515fec27036d2917939188bb7e5fe2f7221764e88a3cd02e69f2eb56b4`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 4.2 MB (4209304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebac161544dc4658cc814aad81b0ff86bd1d898e91f0338551c49b3016088402`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 34.5 MB (34533493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60528a108f9e014fac4c88d7296bc87640fa6dc870be9556a38b77052eb37d17`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d765878602b49619efdfaf06bad80588374d00c52cd8bcb12e58e429353ff33c`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c578b6b26676ec6f489b38e7793a1c9f45f29f1b6b2d08f0cbfb56cfdf15eb1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:239a24ec96d5152a662ed774fd93d6370d8d1af285516c25c7903fbb742ca3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474012545f814205c43db413af10950e0de4ae35bad155ee8f62215822d9d3`

```dockerfile
```

-	Layers:
	-	`sha256:26661d4e888049dfe670c2fc04261cdfcd4555b0f715a38a5ef4d762e1ed17c8`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 2.9 MB (2909710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e019200dd299ab18cc283e7937105f43642f6b99cde77a24a7ec9350cddd98d`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0b492c6d05689f325947c3e44d2c3f63b6299ae4085e51a10d457ec51fc90425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63223175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537402ab45140b490f9658dedc8b5417385430538b6bbbcd993f9af56c1f78ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1bd891fa2294cc29f58e5acf4752a287e008732eefe0b15933e925f1a94d20`  
		Last Modified: Thu, 17 Oct 2024 06:26:32 GMT  
		Size: 3.5 MB (3511688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de36fa410591221fa6227a8908486c83e59678dacc395bce7b0e0ef7cc9601`  
		Last Modified: Thu, 17 Oct 2024 06:26:33 GMT  
		Size: 33.1 MB (33097538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b9a058809c5beb7edacfb21826e76fc3797f3a0ea9d07f06b04715c09643d1`  
		Last Modified: Thu, 17 Oct 2024 06:26:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c58758a3b470de1527bdc9423eccd5b762bed20bcfd790f0f3f60d4f049a53`  
		Last Modified: Thu, 17 Oct 2024 06:26:33 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1c640d490118b29674bb22e41da515b326a940c47962ff2be819d73255ef98`  
		Last Modified: Thu, 17 Oct 2024 06:26:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:90111ff4592753bdf9f1af8b0bf8b641c3e23f79179054bcc7f5f1361adac87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2911639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb26422ef6167f0bc0fdcc8edb4c5cb019e0c137bf366caac1c3e55c93070e1`

```dockerfile
```

-	Layers:
	-	`sha256:f00a1114ca629f53c25ff1d8f4aa4add1cfd098b2f8ab2789f9b34c4dac15a5b`  
		Last Modified: Thu, 17 Oct 2024 06:26:32 GMT  
		Size: 2.9 MB (2895951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888848e26e926100a729ba53afeab4d47f482eb8418c3bb741d04d61e398c8e4`  
		Last Modified: Thu, 17 Oct 2024 06:26:32 GMT  
		Size: 15.7 KB (15688 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:4caec29ad84d8f65607dd0384f6dcbb72c45b510e323565829e8428b70d845af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67548533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b9f1adeef0b772f85427658f080359ce47ac3c684dbb837646f9c705dd4b39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f1633116557b1eef61b5774f6a6bb4420023b95ac40c6c6e12cf5c0383c8b`  
		Last Modified: Thu, 17 Oct 2024 07:51:07 GMT  
		Size: 4.2 MB (4210574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae58e1e7c61f3772f506c61a75a4bebb9f9cdc440cfdbc0406b083bbf945dfe`  
		Last Modified: Thu, 17 Oct 2024 07:51:07 GMT  
		Size: 33.2 MB (33237821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f322b953091e4ea9cb0276ce86bed756172ba0a9512c9a8931d5a8525a51cdb`  
		Last Modified: Thu, 17 Oct 2024 07:51:06 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3413e6c18ce970eaca7cfa6947661fe2d7097b1551976b6975b83eac74cb8d49`  
		Last Modified: Thu, 17 Oct 2024 07:51:07 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1edcdabeaf5265fdda4ed0b76c967065d36b2a4a51593f8e348a98f28b38d02`  
		Last Modified: Thu, 17 Oct 2024 07:51:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:2ce4d2e62054d244bbb05dfcce6a063701e9a8c7f6c6812bcccb171192d1464e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bf0ac76d7f141a354757ed3b9bfcb99f6c95bd860e1f4ba614349bea56cffe`

```dockerfile
```

-	Layers:
	-	`sha256:f41a3b4197dcc07ba59a796e3516a74b9870c94fac4058dc8edafa6158ec6463`  
		Last Modified: Thu, 17 Oct 2024 07:51:07 GMT  
		Size: 2.9 MB (2893929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb49d72cec5e0fd01ed5e9fa8d818e17466cecbf4894be3b5c6c7eb245362ddb`  
		Last Modified: Thu, 17 Oct 2024 07:51:06 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:287ff0fe62f1d938c9f5a4276ffdac4b96b80a9fe3f1c5cd2a5fe136a8b60b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e590b22cd07479b45e4b1e21199857d7b8dad3afdadf9fbf74affe9e22fbaeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23496129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ee9cbce84cddf5af1b3cec11a1bec04e7c131c56c4e0ab88301e36b1c61f66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb0c63a516b7d1c4b6f1b8b33078458f7cbd1898070843f549e6d43cd5324d`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 290.9 KB (290886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9ab55224078be68f4a7871e8058733688c9eb20b9ac31ef4ecad44b26714f0`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 19.6 MB (19556696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782f73fe87195977b450fc5374cb4eb5706d48954c1f955f9a381f81c91a51b8`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 12.2 KB (12233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c1d264bde5e62a8767474eb0bbec13ddf17d34ee732fe1b1fcfed60e89672`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310fd68fe32a67bc64c8924a620d071699d04bea0e7015d71946c0ab8d28c43`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:43cb3142ea3dde7754a8511a1bf59b24c421ce486acc40e35e5d2ca247019c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 KB (188251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f960e3661dbab4d85d385021946762c4fe6b9774a09368fcf9fb0ef400426ed`

```dockerfile
```

-	Layers:
	-	`sha256:247771501dba854ae3371fbeb61ba23468ea08d067b3a7b9ce93ea0def7bd516`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 171.3 KB (171339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae95d3380a26f742724416d959bc64a1d708327eda838c26bff991cbbcd839e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:7bcb9c589f055a2862cbb3f23b58505699952bb1b60f6a54362f4a7ff0536840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:2e049b9a32b3c7088f9c802f7923d91d4242c8ef07f8d1c5694c657730b344a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70218746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05d82d0aa19e8425c3e53f13b83e8901ef2d875a7ddc5bf7348a6e80d68e438`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd178515fec27036d2917939188bb7e5fe2f7221764e88a3cd02e69f2eb56b4`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 4.2 MB (4209304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebac161544dc4658cc814aad81b0ff86bd1d898e91f0338551c49b3016088402`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 34.5 MB (34533493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60528a108f9e014fac4c88d7296bc87640fa6dc870be9556a38b77052eb37d17`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d765878602b49619efdfaf06bad80588374d00c52cd8bcb12e58e429353ff33c`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c578b6b26676ec6f489b38e7793a1c9f45f29f1b6b2d08f0cbfb56cfdf15eb1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:239a24ec96d5152a662ed774fd93d6370d8d1af285516c25c7903fbb742ca3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2925487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc474012545f814205c43db413af10950e0de4ae35bad155ee8f62215822d9d3`

```dockerfile
```

-	Layers:
	-	`sha256:26661d4e888049dfe670c2fc04261cdfcd4555b0f715a38a5ef4d762e1ed17c8`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 2.9 MB (2909710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e019200dd299ab18cc283e7937105f43642f6b99cde77a24a7ec9350cddd98d`  
		Last Modified: Tue, 12 Nov 2024 02:38:21 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0b492c6d05689f325947c3e44d2c3f63b6299ae4085e51a10d457ec51fc90425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63223175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537402ab45140b490f9658dedc8b5417385430538b6bbbcd993f9af56c1f78ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1bd891fa2294cc29f58e5acf4752a287e008732eefe0b15933e925f1a94d20`  
		Last Modified: Thu, 17 Oct 2024 06:26:32 GMT  
		Size: 3.5 MB (3511688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9de36fa410591221fa6227a8908486c83e59678dacc395bce7b0e0ef7cc9601`  
		Last Modified: Thu, 17 Oct 2024 06:26:33 GMT  
		Size: 33.1 MB (33097538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b9a058809c5beb7edacfb21826e76fc3797f3a0ea9d07f06b04715c09643d1`  
		Last Modified: Thu, 17 Oct 2024 06:26:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c58758a3b470de1527bdc9423eccd5b762bed20bcfd790f0f3f60d4f049a53`  
		Last Modified: Thu, 17 Oct 2024 06:26:33 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1c640d490118b29674bb22e41da515b326a940c47962ff2be819d73255ef98`  
		Last Modified: Thu, 17 Oct 2024 06:26:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:90111ff4592753bdf9f1af8b0bf8b641c3e23f79179054bcc7f5f1361adac87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2911639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb26422ef6167f0bc0fdcc8edb4c5cb019e0c137bf366caac1c3e55c93070e1`

```dockerfile
```

-	Layers:
	-	`sha256:f00a1114ca629f53c25ff1d8f4aa4add1cfd098b2f8ab2789f9b34c4dac15a5b`  
		Last Modified: Thu, 17 Oct 2024 06:26:32 GMT  
		Size: 2.9 MB (2895951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888848e26e926100a729ba53afeab4d47f482eb8418c3bb741d04d61e398c8e4`  
		Last Modified: Thu, 17 Oct 2024 06:26:32 GMT  
		Size: 15.7 KB (15688 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:4caec29ad84d8f65607dd0384f6dcbb72c45b510e323565829e8428b70d845af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67548533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b9f1adeef0b772f85427658f080359ce47ac3c684dbb837646f9c705dd4b39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f1633116557b1eef61b5774f6a6bb4420023b95ac40c6c6e12cf5c0383c8b`  
		Last Modified: Thu, 17 Oct 2024 07:51:07 GMT  
		Size: 4.2 MB (4210574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae58e1e7c61f3772f506c61a75a4bebb9f9cdc440cfdbc0406b083bbf945dfe`  
		Last Modified: Thu, 17 Oct 2024 07:51:07 GMT  
		Size: 33.2 MB (33237821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f322b953091e4ea9cb0276ce86bed756172ba0a9512c9a8931d5a8525a51cdb`  
		Last Modified: Thu, 17 Oct 2024 07:51:06 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3413e6c18ce970eaca7cfa6947661fe2d7097b1551976b6975b83eac74cb8d49`  
		Last Modified: Thu, 17 Oct 2024 07:51:07 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1edcdabeaf5265fdda4ed0b76c967065d36b2a4a51593f8e348a98f28b38d02`  
		Last Modified: Thu, 17 Oct 2024 07:51:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:2ce4d2e62054d244bbb05dfcce6a063701e9a8c7f6c6812bcccb171192d1464e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bf0ac76d7f141a354757ed3b9bfcb99f6c95bd860e1f4ba614349bea56cffe`

```dockerfile
```

-	Layers:
	-	`sha256:f41a3b4197dcc07ba59a796e3516a74b9870c94fac4058dc8edafa6158ec6463`  
		Last Modified: Thu, 17 Oct 2024 07:51:07 GMT  
		Size: 2.9 MB (2893929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb49d72cec5e0fd01ed5e9fa8d818e17466cecbf4894be3b5c6c7eb245362ddb`  
		Last Modified: Thu, 17 Oct 2024 07:51:06 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:287ff0fe62f1d938c9f5a4276ffdac4b96b80a9fe3f1c5cd2a5fe136a8b60b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e590b22cd07479b45e4b1e21199857d7b8dad3afdadf9fbf74affe9e22fbaeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23496129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ee9cbce84cddf5af1b3cec11a1bec04e7c131c56c4e0ab88301e36b1c61f66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb0c63a516b7d1c4b6f1b8b33078458f7cbd1898070843f549e6d43cd5324d`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 290.9 KB (290886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9ab55224078be68f4a7871e8058733688c9eb20b9ac31ef4ecad44b26714f0`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 19.6 MB (19556696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782f73fe87195977b450fc5374cb4eb5706d48954c1f955f9a381f81c91a51b8`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 12.2 KB (12233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c1d264bde5e62a8767474eb0bbec13ddf17d34ee732fe1b1fcfed60e89672`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310fd68fe32a67bc64c8924a620d071699d04bea0e7015d71946c0ab8d28c43`  
		Last Modified: Tue, 12 Nov 2024 02:38:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:43cb3142ea3dde7754a8511a1bf59b24c421ce486acc40e35e5d2ca247019c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 KB (188251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f960e3661dbab4d85d385021946762c4fe6b9774a09368fcf9fb0ef400426ed`

```dockerfile
```

-	Layers:
	-	`sha256:247771501dba854ae3371fbeb61ba23468ea08d067b3a7b9ce93ea0def7bd516`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 171.3 KB (171339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae95d3380a26f742724416d959bc64a1d708327eda838c26bff991cbbcd839e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:17bd61e41088c5e06c318b9241e74fee0838a02b08ee1712251f99db896388d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:c6e9646764e6944c7c8fc138539632b3bd8cc064914a36174e6c576ae6465403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70860520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389c547c19e9286bc658a37a71155ccd5486f7d8fbc5d51268af58036fbbf446`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7074b6f8a051b34df09afd81984702756eac1a6d80ba80df612d4e91b9dbe3`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 5.0 MB (5020317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8ce1b138a4e7eb1283d723db328262df8d9d3856abe75faa754077f200881`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 34.4 MB (34364253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73f9633ce34099e462eab26842cf9f3573f170e0f4d0ffdaf317e269f5c8d73`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120606c6913bce6b726210d1c4b0140fda3e7b5fc8a4414471d50fe1dbb6da81`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383e51ee302fafcf5b6a9f4152f42d85cc2539d4b381d9d88c85799a610537af`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:43f24eee2e8d6fb1ad09c47e1a7fe8c9e702bc0f131c2cefbd795e740d2f8f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c42cfda542739a5405cfc3abc2e1d0aab363bfc81fe03c246d12d32c34ca3e`

```dockerfile
```

-	Layers:
	-	`sha256:818a923debf8be6a6daa6a0ce0a06e8c5920c4d05e010ae252bbb4363deade66`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 3.0 MB (2965808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6739731f2a91e929f4d41f825d19d398803be2aa001feef1d0b9c709e05b699`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5250943732e87285bdbc2d0bb6d6be84405396c6540dc1b4744e55cddc49dec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63639016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dffcd8d691c33d7a51f2114870f6b9c89a6c116f2c2f80f8775cdc055f6e98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0c2bdb87b9efc4ecca70915ec74c43dc3af4aca3ed73584c2eeb0c3543701d`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 4.5 MB (4490255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5da11fe81201a6faae1c472f334265a15409d0b7d1e618d13aaacfb169a28a8`  
		Last Modified: Thu, 17 Oct 2024 06:27:19 GMT  
		Size: 32.5 MB (32534813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba73a12d5f0271f9a763276eb1c68d0b96c41b9972c282076cf779a4a17cc4`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447cf80ce0c3f1a8b335d9919e56ed7bceb2e448d68aaf68b6cf8d889e051f72`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a851f64386fb21307229edbefb8db1ab09423335733e93c5c463bce8e7b35b`  
		Last Modified: Thu, 17 Oct 2024 06:27:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:89fc084d758f59141109e6fb71dfcc7e8d8b90c46bda80bf60510c450f2f71eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89b03f7e40189a9b6426d1abbcd01f2c297e02f8da0081614708a20f8879543`

```dockerfile
```

-	Layers:
	-	`sha256:ed985b33017babec1d73f1242e161c0ee753192bfa5846d490aa6489f9834485`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 3.0 MB (2952049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed51e8c5b479355cbc1a67efa4e338a5bd1be6fdff9a800d8abda36a54e59efe`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 15.7 KB (15728 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:739e9c44ab04cad8a5cae8a72fb94a9dc22f468a50a6e6dfd1d3fe0fbb20ba54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67737795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d4dde17dd744b0a849c0144e9be23ad6d04325071de2ed2f8814df911083eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9846545bf6ec84f12c0d8881fee4290e6f53a72f19df063e73f6348eb3fcbb65`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 5.2 MB (5208186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e45ef53794e79783a4426eaed5e0721862838558d97eb080ae7a6b18cba7b07`  
		Last Modified: Thu, 17 Oct 2024 07:51:56 GMT  
		Size: 32.4 MB (32429458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854982b51a7116d9d20cf2f988f54734fa04e59b538e2bc5a5404742eb799d3d`  
		Last Modified: Thu, 17 Oct 2024 07:51:54 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4be59e981f0b551163989eb73ea46871d414bc07ed00ab9557908e745ed768`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0600b162f4663be747b351b728b0ad007750e69300c57677ca8f3b9499821f`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:f628d1daf4c73f72a2512306952fb84877d3dd9403984634c3e5fdf114916df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89de6994ed34fbf50a8743e2280541e7eb126a016701b0dd2ac9cfe52005ab9f`

```dockerfile
```

-	Layers:
	-	`sha256:0253f040e274cfcbb7139a3adc3b86d52ddf8c9dec7da5a968986124218834eb`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 3.0 MB (2950027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e4deaa5667fd68beb20216bd3d9a9d7ae1465d098e7d3a6661d560c27c8f63`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 15.7 KB (15749 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:92dc915f49a171a9bff9c19efc9a24e8c79d4b27b352785d02e8b337da5c9289
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bcb0d37b5c18fb36680f7eb5ce3e0453be8e8385449c26644be8e3f92518aa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be622339b1663b25fee8bc1addea46f9fe079dbde554e6cea10b9988b928b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f837f0e9fa34b0ee2116e7f1db559192bed2b3210feab89b723dd970f6fdb28b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c112ae596e0cf07497f1016dc504b80fd0ad68cc723f7f2066e1aa7c0a55`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 290.9 KB (290887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7272e467da9f0a75a0f807ca4b262a06aee61541f7014b554868ade8fc95b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 19.2 MB (19204040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29657181aa450b81b61910eeb70b371a8216c40ae4a395a7a79a49f5956181f7`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2062c76035454d3284bbc7ca4f0c61310bbb4d60df320b9c9c456b4fdd023e8`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b05a1c7abb5eb31b653dd382a993cea9700df0838f570c317de0e5d211af6fc`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:f8bddac8d03188aa5158f46ab76e02927dc923117f8eac59fa9ab0750bf56ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beca0b115f7a7d4f457168aa29385f5b3134e4b669263817d46a2a82e0370a4`

```dockerfile
```

-	Layers:
	-	`sha256:35214902caaa7ed50f2443bb8424883e23a2fe8f20c545e1260430164b8c05d9`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 228.3 KB (228310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14c355a1a64de3b8bb5d6a1704de421d53d0023b84d87ae4e790f4724694481`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:17bd61e41088c5e06c318b9241e74fee0838a02b08ee1712251f99db896388d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:c6e9646764e6944c7c8fc138539632b3bd8cc064914a36174e6c576ae6465403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70860520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389c547c19e9286bc658a37a71155ccd5486f7d8fbc5d51268af58036fbbf446`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7074b6f8a051b34df09afd81984702756eac1a6d80ba80df612d4e91b9dbe3`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 5.0 MB (5020317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8ce1b138a4e7eb1283d723db328262df8d9d3856abe75faa754077f200881`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 34.4 MB (34364253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73f9633ce34099e462eab26842cf9f3573f170e0f4d0ffdaf317e269f5c8d73`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120606c6913bce6b726210d1c4b0140fda3e7b5fc8a4414471d50fe1dbb6da81`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383e51ee302fafcf5b6a9f4152f42d85cc2539d4b381d9d88c85799a610537af`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:43f24eee2e8d6fb1ad09c47e1a7fe8c9e702bc0f131c2cefbd795e740d2f8f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c42cfda542739a5405cfc3abc2e1d0aab363bfc81fe03c246d12d32c34ca3e`

```dockerfile
```

-	Layers:
	-	`sha256:818a923debf8be6a6daa6a0ce0a06e8c5920c4d05e010ae252bbb4363deade66`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 3.0 MB (2965808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6739731f2a91e929f4d41f825d19d398803be2aa001feef1d0b9c709e05b699`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5250943732e87285bdbc2d0bb6d6be84405396c6540dc1b4744e55cddc49dec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63639016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dffcd8d691c33d7a51f2114870f6b9c89a6c116f2c2f80f8775cdc055f6e98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0c2bdb87b9efc4ecca70915ec74c43dc3af4aca3ed73584c2eeb0c3543701d`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 4.5 MB (4490255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5da11fe81201a6faae1c472f334265a15409d0b7d1e618d13aaacfb169a28a8`  
		Last Modified: Thu, 17 Oct 2024 06:27:19 GMT  
		Size: 32.5 MB (32534813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba73a12d5f0271f9a763276eb1c68d0b96c41b9972c282076cf779a4a17cc4`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447cf80ce0c3f1a8b335d9919e56ed7bceb2e448d68aaf68b6cf8d889e051f72`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a851f64386fb21307229edbefb8db1ab09423335733e93c5c463bce8e7b35b`  
		Last Modified: Thu, 17 Oct 2024 06:27:19 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:89fc084d758f59141109e6fb71dfcc7e8d8b90c46bda80bf60510c450f2f71eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89b03f7e40189a9b6426d1abbcd01f2c297e02f8da0081614708a20f8879543`

```dockerfile
```

-	Layers:
	-	`sha256:ed985b33017babec1d73f1242e161c0ee753192bfa5846d490aa6489f9834485`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 3.0 MB (2952049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed51e8c5b479355cbc1a67efa4e338a5bd1be6fdff9a800d8abda36a54e59efe`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 15.7 KB (15728 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:739e9c44ab04cad8a5cae8a72fb94a9dc22f468a50a6e6dfd1d3fe0fbb20ba54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67737795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d4dde17dd744b0a849c0144e9be23ad6d04325071de2ed2f8814df911083eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9846545bf6ec84f12c0d8881fee4290e6f53a72f19df063e73f6348eb3fcbb65`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 5.2 MB (5208186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e45ef53794e79783a4426eaed5e0721862838558d97eb080ae7a6b18cba7b07`  
		Last Modified: Thu, 17 Oct 2024 07:51:56 GMT  
		Size: 32.4 MB (32429458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854982b51a7116d9d20cf2f988f54734fa04e59b538e2bc5a5404742eb799d3d`  
		Last Modified: Thu, 17 Oct 2024 07:51:54 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4be59e981f0b551163989eb73ea46871d414bc07ed00ab9557908e745ed768`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0600b162f4663be747b351b728b0ad007750e69300c57677ca8f3b9499821f`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:f628d1daf4c73f72a2512306952fb84877d3dd9403984634c3e5fdf114916df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89de6994ed34fbf50a8743e2280541e7eb126a016701b0dd2ac9cfe52005ab9f`

```dockerfile
```

-	Layers:
	-	`sha256:0253f040e274cfcbb7139a3adc3b86d52ddf8c9dec7da5a968986124218834eb`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 3.0 MB (2950027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e4deaa5667fd68beb20216bd3d9a9d7ae1465d098e7d3a6661d560c27c8f63`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 15.7 KB (15749 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:92dc915f49a171a9bff9c19efc9a24e8c79d4b27b352785d02e8b337da5c9289
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:bcb0d37b5c18fb36680f7eb5ce3e0453be8e8385449c26644be8e3f92518aa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be622339b1663b25fee8bc1addea46f9fe079dbde554e6cea10b9988b928b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f837f0e9fa34b0ee2116e7f1db559192bed2b3210feab89b723dd970f6fdb28b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3982c112ae596e0cf07497f1016dc504b80fd0ad68cc723f7f2066e1aa7c0a55`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 290.9 KB (290887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7272e467da9f0a75a0f807ca4b262a06aee61541f7014b554868ade8fc95b`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 19.2 MB (19204040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29657181aa450b81b61910eeb70b371a8216c40ae4a395a7a79a49f5956181f7`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2062c76035454d3284bbc7ca4f0c61310bbb4d60df320b9c9c456b4fdd023e8`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b05a1c7abb5eb31b653dd382a993cea9700df0838f570c317de0e5d211af6fc`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:f8bddac8d03188aa5158f46ab76e02927dc923117f8eac59fa9ab0750bf56ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beca0b115f7a7d4f457168aa29385f5b3134e4b669263817d46a2a82e0370a4`

```dockerfile
```

-	Layers:
	-	`sha256:35214902caaa7ed50f2443bb8424883e23a2fe8f20c545e1260430164b8c05d9`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 228.3 KB (228310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14c355a1a64de3b8bb5d6a1704de421d53d0023b84d87ae4e790f4724694481`  
		Last Modified: Tue, 12 Nov 2024 02:38:08 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:d1d40e2f3452d6a6eb68a40da083cd92d2524fef25706184d60265ddcede1756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:50f64bb06992802aa96de3033cf731c736f1621cded83feb97eda1dd42166e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71507977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc626241470aaf35f5fe1d297c6353899e98a2324d39e8863317365d9cd53a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38acb0bdae8b7299b96bef5f8d902e06eaa5730c3353379420ad02145e6ea8e5`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 5.0 MB (5020322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0badaffefb66097a9ebaef1b2a1698156c9e65188a72882f4dc3419e05eec`  
		Last Modified: Tue, 12 Nov 2024 02:38:18 GMT  
		Size: 35.0 MB (35011707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281a0a1524081d8e4a61cac212e2a2c5134e0c2a5c0d194a4ee158128fc06da`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac6883e6ccb3f1e5a4a1492b27006fe8cdf3e0f52a8bbfdd8a41432df91ed3b`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6c6eb440cc51a6837c2ebf0c98b854b841dbc69474306bad8d42ff03d78946`  
		Last Modified: Tue, 12 Nov 2024 02:38:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:13662c24a905ca7e3f1c449c9cb46fdad1e5413ba932ec9949986a7247ca174e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0e4422cf787b178201e3619b3205102559c6d459e9a73bf0901e7770f43bf`

```dockerfile
```

-	Layers:
	-	`sha256:708ce5c455fb8bc4b30f6c09c73121f1e8bdc2192c4ab924d32cbd6cfd8a5826`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 3.0 MB (2970958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fcacb9190786f8752ff5e11b6c18da279269f786f6d08106626b1ca38baa6e`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:66e07c79b974b8ba3f4ecb890a002b515335aecd49944e61248d1d7c6758a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64415690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664bf9f28a946ed53db120376de96e594c7961f7ded44a3082fbbb0adacc1321`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0c2bdb87b9efc4ecca70915ec74c43dc3af4aca3ed73584c2eeb0c3543701d`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 4.5 MB (4490255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b8a49f7752245ef56cca7656634b57feaff2873138c1d04eb9f4f5840aafe5`  
		Last Modified: Thu, 17 Oct 2024 06:27:54 GMT  
		Size: 33.3 MB (33311483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe294a155bde60096b5541a27954bc37bee351cbd7582a3564bd0984760d49a`  
		Last Modified: Thu, 17 Oct 2024 06:27:53 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deda7bd8833e114c59ed24e50dc269dbe262196b80cb7d17489e75f8626e6a37`  
		Last Modified: Thu, 17 Oct 2024 06:27:53 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffca7f42be10b627951c46f9eb09c334efeae65898556f2635fe5d14721952a4`  
		Last Modified: Thu, 17 Oct 2024 06:27:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:bd9f4aaa1a1aa1257447db4161bdc10b669a7a12943df11914a3ccecb68e07f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613a7f3a3a1922e816bd6d317d901db1274e4fa5a181ced865caf5a19d745385`

```dockerfile
```

-	Layers:
	-	`sha256:4b2048f5fb5157670bf40aad668f269820921d3c2b33cb1d9fa19325e92fca37`  
		Last Modified: Thu, 17 Oct 2024 06:27:54 GMT  
		Size: 3.0 MB (2957199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7c803354a118377a96393b924a4df8212df6b1630995641a982b4727850274`  
		Last Modified: Thu, 17 Oct 2024 06:27:53 GMT  
		Size: 15.7 KB (15720 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ffe2226dfc5afb450f5809fb3a87ff6e725f334c6a691cdf146885f501c7d53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68489820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9324521f3f13967d8679fc066c7d829f1cd477a4a55dfc51058c9ff25e6e4af8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9846545bf6ec84f12c0d8881fee4290e6f53a72f19df063e73f6348eb3fcbb65`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 5.2 MB (5208186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd03e2d2312bf14a6a646371d4e3468e84837762080e7420153fb6e992cd42c6`  
		Last Modified: Thu, 17 Oct 2024 07:52:23 GMT  
		Size: 33.2 MB (33181501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d7d659a5332b69b4b6f46051e3753d656830909a7ff732e2c56865820b108e`  
		Last Modified: Thu, 17 Oct 2024 07:52:22 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b5ac179121779ba2d5701f4fcbe70ba7b23149c3fd9871b435001698ff58cb`  
		Last Modified: Thu, 17 Oct 2024 07:52:22 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda8b31d58c842070264b00d7ad3294bd1c78a79c6cea5a6d2e97674f3b0aafd`  
		Last Modified: Thu, 17 Oct 2024 07:52:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:247cd84a0da3e34375b45e9fa4dbc1cbdc52d7b4ed46a2abbe86f6a9cf1638ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a791d93f981bbae38e7fb5de7998dea9852bd6e6a5827c38804e205bd6d63f57`

```dockerfile
```

-	Layers:
	-	`sha256:ee46371609253090c66c0fdff139b3c39a902a67b6b19a6d4f06582c7c5a93da`  
		Last Modified: Thu, 17 Oct 2024 07:52:23 GMT  
		Size: 3.0 MB (2955177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628be7648b29edad74f3567ee36abc5eb46e57bcdb11939737a20d6823a93fc2`  
		Last Modified: Thu, 17 Oct 2024 07:52:22 GMT  
		Size: 15.7 KB (15743 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:b52ddf6c80429a91e462840afcb013b449c5fa7b4b356c92a83490e61debe3c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e0b078ddef48edabb3edd67587d73dce0886f1676d777da47062ab1eed88b0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c5bb53ba7aca946cba46980d5ab416af7a303ae1e8c442f2ddfdd0486a3297`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a938a04d3b903456f3b0c899a1ee719f0fbe0c20572ce8f8a333cbd7204c9424`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403debb40518414e6b358a892a18b3e5f0f7e54081cfeb9b07c2b3101c971a6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 290.9 KB (290888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac7ca426c5927695eb459153d6e03440a125f298ee6e62fc6919e2107e3567b`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 19.7 MB (19672077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b5a34d409580ae00a43acde566afb4380ddaf799697c813b6950eb6182c8e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed6f91e2c5f917da15268635d210a1b9b6578179b3c6e3ca8ddf34bfe965eb`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e9b4f4321537230681e57bb52a6ee546109b0a5ce852c867370658982bab4a`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e401a0ae1338217c8774af1a7e7659865b503b32642d6b625261d45b377ad8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3f1efc9c7e0a00983a84864956c0978fe19267c7224a63934dad2143b6116b`

```dockerfile
```

-	Layers:
	-	`sha256:b6b58d80490c4f66b398d6fe9770891de0d7a7dc51a5f8f529ef457e3b7c94f6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 233.5 KB (233462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fe607b78ca533bf4dab527c8ab91e259f9b0e65f7abef6ead17fae5eb09ef2`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:d1d40e2f3452d6a6eb68a40da083cd92d2524fef25706184d60265ddcede1756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:50f64bb06992802aa96de3033cf731c736f1621cded83feb97eda1dd42166e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71507977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc626241470aaf35f5fe1d297c6353899e98a2324d39e8863317365d9cd53a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38acb0bdae8b7299b96bef5f8d902e06eaa5730c3353379420ad02145e6ea8e5`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 5.0 MB (5020322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0badaffefb66097a9ebaef1b2a1698156c9e65188a72882f4dc3419e05eec`  
		Last Modified: Tue, 12 Nov 2024 02:38:18 GMT  
		Size: 35.0 MB (35011707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8281a0a1524081d8e4a61cac212e2a2c5134e0c2a5c0d194a4ee158128fc06da`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac6883e6ccb3f1e5a4a1492b27006fe8cdf3e0f52a8bbfdd8a41432df91ed3b`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6c6eb440cc51a6837c2ebf0c98b854b841dbc69474306bad8d42ff03d78946`  
		Last Modified: Tue, 12 Nov 2024 02:38:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:13662c24a905ca7e3f1c449c9cb46fdad1e5413ba932ec9949986a7247ca174e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0e4422cf787b178201e3619b3205102559c6d459e9a73bf0901e7770f43bf`

```dockerfile
```

-	Layers:
	-	`sha256:708ce5c455fb8bc4b30f6c09c73121f1e8bdc2192c4ab924d32cbd6cfd8a5826`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 3.0 MB (2970958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2fcacb9190786f8752ff5e11b6c18da279269f786f6d08106626b1ca38baa6e`  
		Last Modified: Tue, 12 Nov 2024 02:38:17 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:66e07c79b974b8ba3f4ecb890a002b515335aecd49944e61248d1d7c6758a9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64415690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664bf9f28a946ed53db120376de96e594c7961f7ded44a3082fbbb0adacc1321`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0c2bdb87b9efc4ecca70915ec74c43dc3af4aca3ed73584c2eeb0c3543701d`  
		Last Modified: Thu, 17 Oct 2024 06:27:18 GMT  
		Size: 4.5 MB (4490255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b8a49f7752245ef56cca7656634b57feaff2873138c1d04eb9f4f5840aafe5`  
		Last Modified: Thu, 17 Oct 2024 06:27:54 GMT  
		Size: 33.3 MB (33311483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe294a155bde60096b5541a27954bc37bee351cbd7582a3564bd0984760d49a`  
		Last Modified: Thu, 17 Oct 2024 06:27:53 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deda7bd8833e114c59ed24e50dc269dbe262196b80cb7d17489e75f8626e6a37`  
		Last Modified: Thu, 17 Oct 2024 06:27:53 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffca7f42be10b627951c46f9eb09c334efeae65898556f2635fe5d14721952a4`  
		Last Modified: Thu, 17 Oct 2024 06:27:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:bd9f4aaa1a1aa1257447db4161bdc10b669a7a12943df11914a3ccecb68e07f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613a7f3a3a1922e816bd6d317d901db1274e4fa5a181ced865caf5a19d745385`

```dockerfile
```

-	Layers:
	-	`sha256:4b2048f5fb5157670bf40aad668f269820921d3c2b33cb1d9fa19325e92fca37`  
		Last Modified: Thu, 17 Oct 2024 06:27:54 GMT  
		Size: 3.0 MB (2957199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7c803354a118377a96393b924a4df8212df6b1630995641a982b4727850274`  
		Last Modified: Thu, 17 Oct 2024 06:27:53 GMT  
		Size: 15.7 KB (15720 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ffe2226dfc5afb450f5809fb3a87ff6e725f334c6a691cdf146885f501c7d53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68489820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9324521f3f13967d8679fc066c7d829f1cd477a4a55dfc51058c9ff25e6e4af8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9846545bf6ec84f12c0d8881fee4290e6f53a72f19df063e73f6348eb3fcbb65`  
		Last Modified: Thu, 17 Oct 2024 07:51:55 GMT  
		Size: 5.2 MB (5208186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd03e2d2312bf14a6a646371d4e3468e84837762080e7420153fb6e992cd42c6`  
		Last Modified: Thu, 17 Oct 2024 07:52:23 GMT  
		Size: 33.2 MB (33181501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d7d659a5332b69b4b6f46051e3753d656830909a7ff732e2c56865820b108e`  
		Last Modified: Thu, 17 Oct 2024 07:52:22 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b5ac179121779ba2d5701f4fcbe70ba7b23149c3fd9871b435001698ff58cb`  
		Last Modified: Thu, 17 Oct 2024 07:52:22 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda8b31d58c842070264b00d7ad3294bd1c78a79c6cea5a6d2e97674f3b0aafd`  
		Last Modified: Thu, 17 Oct 2024 07:52:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:247cd84a0da3e34375b45e9fa4dbc1cbdc52d7b4ed46a2abbe86f6a9cf1638ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a791d93f981bbae38e7fb5de7998dea9852bd6e6a5827c38804e205bd6d63f57`

```dockerfile
```

-	Layers:
	-	`sha256:ee46371609253090c66c0fdff139b3c39a902a67b6b19a6d4f06582c7c5a93da`  
		Last Modified: Thu, 17 Oct 2024 07:52:23 GMT  
		Size: 3.0 MB (2955177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628be7648b29edad74f3567ee36abc5eb46e57bcdb11939737a20d6823a93fc2`  
		Last Modified: Thu, 17 Oct 2024 07:52:22 GMT  
		Size: 15.7 KB (15743 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:b52ddf6c80429a91e462840afcb013b449c5fa7b4b356c92a83490e61debe3c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:e0b078ddef48edabb3edd67587d73dce0886f1676d777da47062ab1eed88b0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c5bb53ba7aca946cba46980d5ab416af7a303ae1e8c442f2ddfdd0486a3297`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a938a04d3b903456f3b0c899a1ee719f0fbe0c20572ce8f8a333cbd7204c9424`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403debb40518414e6b358a892a18b3e5f0f7e54081cfeb9b07c2b3101c971a6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 290.9 KB (290888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac7ca426c5927695eb459153d6e03440a125f298ee6e62fc6919e2107e3567b`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 19.7 MB (19672077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b5a34d409580ae00a43acde566afb4380ddaf799697c813b6950eb6182c8e3`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eed6f91e2c5f917da15268635d210a1b9b6578179b3c6e3ca8ddf34bfe965eb`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e9b4f4321537230681e57bb52a6ee546109b0a5ce852c867370658982bab4a`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:e401a0ae1338217c8774af1a7e7659865b503b32642d6b625261d45b377ad8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3f1efc9c7e0a00983a84864956c0978fe19267c7224a63934dad2143b6116b`

```dockerfile
```

-	Layers:
	-	`sha256:b6b58d80490c4f66b398d6fe9770891de0d7a7dc51a5f8f529ef457e3b7c94f6`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 233.5 KB (233462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9fe607b78ca533bf4dab527c8ab91e259f9b0e65f7abef6ead17fae5eb09ef2`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:e917c05d49569ffc91363b69db1139b3aec3ea352d7e4ab116ac73b5276c1e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9177fbf8d1abc0941d457afc9b0e50767dab53c0fa38968d0935948927429e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31808028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbf6891fc635a202a911272984b230346ed88f7ed61e7c5b4e6699d84faef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d999415b039365cadf590cb0dee4382b11889c724dd0eab32e010a66c2dda7`  
		Last Modified: Tue, 12 Nov 2024 02:38:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85d2cc53952cb93e416bed6638ae8631ac933e78edf15edc8f453889c78a4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 292.6 KB (292626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8ac47ff12105d7e2e63bdfecfe44bad8e9ed2abbb6bf69e824e6185e38c30`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 27.9 MB (27866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e56c6035356fa99cb81386116d4e7f9647b9d607a8d8bf3c7bad00f71e5ae4`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404105c04126e648e925115b31e8503e9be79bff0ac07d22b960fce01cc68627`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2d0f282dc22ee43b73a0bfff8802169fb0b6a1285ee756c538a46c2ffc4303`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:fcf8a567d3540090f865ac052c59bda542cc0aebd2c1ad4413eadd03d956c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 KB (257758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6ab8b16a87c767b2f89aa09b99f84a49a0f574642aff41a53d43e44085627d`

```dockerfile
```

-	Layers:
	-	`sha256:608de47fe583d55de96c34e4f648a275957c4723931f32f5bf45243c183b05fb`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 239.9 KB (239903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf620aebcdf5b9e70ca057c32bcd31da203ea2fc4f7048080488c8522073c0c`  
		Last Modified: Tue, 12 Nov 2024 02:38:09 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:bc97d8bd9b619b8188a7cec64bb4787ca46efa0be66ea89e650e24ad702fc1c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:cbb2398ca1e9c1e79905f76a6f508c0b84e124ed19d8bd1ef329113df6bd0554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84245436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef430dd9bd942ea971170a9ad41a7b86bf2b0bd54963f64e172414e8bbf7b6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224e7e2d3fcfa467dc4f217326c057f4f2dd7300e13ef8f9e857ce39d3b4a1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 7.9 MB (7875383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156341f7966c50570025c0aa511f08d25d6323a659a42aed5dbf0d667f59476a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 47.2 MB (47217593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc833227a91630f06fdbd4aa78c70728725f847e7108c30819c0dd7b1bcc2f1`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942d7292f5707350b55e75b6962c10f687a2f79cd6897f52184d0d756f3640af`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b128af6ad42b6a2e4237a81330a24126fa56928cb1282247f5a0b2e934cce`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d283d9166d23e08f8f2ecab79a9506abca9aca59180582cf53a41af1716e8570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff9e10e6a0907fdc037209f268bd74095409b257480933f04b1cad3729d68f`

```dockerfile
```

-	Layers:
	-	`sha256:3e81168bed413e125218f95a0a4120c7164a7f95a704ffc312fa47035416659c`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 2.7 MB (2706777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da14de2590a125267c353c750cc1c061c345a17e9a5da32b3651a9e5dc1c2ec`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:13a78f4c253093cf30fca5c89c1bb696e1fc682c1b7810e70e5a4c3ed0cc5151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75516412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d71adce3a94e5289bac0d13f5cc4efb87d068f50d800592bc297e2793cbe9ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a2e66a49258f3d38a009ec8390c0ca30e9b21e10c1f97f033935a3cc5547d`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 6.5 MB (6497599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab246a3e9d45eb0ec1e5d6429010eebe6b5030c07dbb87501a3ceca74ea685b9`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 44.3 MB (44276153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6311c1ec06eb271b214b2fb3b0ec782a808c8ccbf31c6753f73123807ef5811`  
		Last Modified: Thu, 17 Oct 2024 06:28:45 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6079489fc1564886a6fb52e0420b2c1478c533f5d728c5f252a9020d11ff0a`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f8925067ffa8213682865f92f9c8e961b3a242bf92478a328aa37bafa4db9b`  
		Last Modified: Thu, 17 Oct 2024 06:28:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:4d5d473389d12da9d271eb185b6a74cb3f4555b5f0067cca46a140fa3143c38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837b3ca99f4b4f58ae00c768cdda7420b29c4d4adbb04fe379004c82e8e8019a`

```dockerfile
```

-	Layers:
	-	`sha256:0bc9dce96a65ba948929d290d404f8baa6920851fe61442b3dddea26a887d674`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 2.7 MB (2693256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6257c8555aefbf425ff0fc7ba80af9cfaff204b57d960f0c1ed989a1ea96928`  
		Last Modified: Thu, 17 Oct 2024 06:28:46 GMT  
		Size: 16.0 KB (16047 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8fb487b848793c15136e02fc531d8a600c1dbe1ec7f1e418a2e5aea62ed7a608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81802481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dea180108a03c10165a2e50c3cbc5225dadc03aa48168a2036fb7bc765d5005`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb962cc4d13593ec1e24aa00be579a90629298b3683b14cae17fb4a8c2fe8380`  
		Last Modified: Thu, 17 Oct 2024 07:53:09 GMT  
		Size: 7.7 MB (7651303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200d97f9a1d8c647ce3047b313528d76f945a2926ad045b195e466d07555aaba`  
		Last Modified: Thu, 17 Oct 2024 07:53:10 GMT  
		Size: 45.0 MB (44970383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1878e31ec9c4489a3f688ef4d78f6e5ecf3a69d2cd8b6a9bbfdc90cee6ab6`  
		Last Modified: Thu, 17 Oct 2024 07:53:08 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f088a8bc8a57f96ba34779583e83565f82f1f269de5c2919c90cff4b146ea27`  
		Last Modified: Thu, 17 Oct 2024 07:53:08 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c773560ba85255bf61546e83fa0ce860ab100ea9a8f11a0a2b5b8447d834b0`  
		Last Modified: Thu, 17 Oct 2024 07:53:09 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:20c5461af83dfb820f38f35c139fb0b294b249b23c65840fd8e87e1bb7c4b1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89f10a644756e7e03f46303a18af6db2d8ff06de4416e4616c60a0d1adcd844`

```dockerfile
```

-	Layers:
	-	`sha256:88003a62b99096f1793d902b4a71d21463c3d6ad917e6cfbc59f5aa71c4a7059`  
		Last Modified: Thu, 17 Oct 2024 07:53:09 GMT  
		Size: 2.7 MB (2691232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3caa001d0cbf97f812f486c523302cbf267b994639b6dcab87ba924b738a63`  
		Last Modified: Thu, 17 Oct 2024 07:53:08 GMT  
		Size: 16.1 KB (16073 bytes)  
		MIME: application/vnd.in-toto+json
