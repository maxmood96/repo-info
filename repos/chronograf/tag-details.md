<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8.4`](#chronograf184)
-	[`chronograf:1.8.4-alpine`](#chronograf184-alpine)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:796188cfeb6cecef6ecf4126d79b63e99b0d10348be0ab1c344ef2ca0825a379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:6700af7c246e818c12a557a5bc116eee27071a94b81891977454d9acd281150c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49103653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f04dd9cce852b4850362cf80e3c49a4dc3ee1ff2132830576bd9cc29fe4313`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:27:47 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 14:27:48 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 22 Jul 2020 14:27:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 14:27:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 14:27:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 14:27:59 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 14:27:59 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 14:28:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 14:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 14:28:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011add3cc110ad3f6b35112efe187883f225c05f5fd2b6a18970832cd666dba3`  
		Last Modified: Wed, 22 Jul 2020 14:29:04 GMT  
		Size: 4.5 MB (4504495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8f79c2ae69a0011f4e8fa0cca8286907d16844997f9e540ac4e2cf374e1696`  
		Last Modified: Wed, 22 Jul 2020 14:29:08 GMT  
		Size: 22.1 MB (22059129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8777822333ab85f3b9f5721283867cfceffe0d293e95011b972bd0188ddab952`  
		Last Modified: Wed, 22 Jul 2020 14:29:03 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a664af4ed9fabf9d51c9ea562efbbf5c3e38150be1f6e91d6d64494224e1d3`  
		Last Modified: Wed, 22 Jul 2020 14:29:03 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db67c489e156b6d2641ab49d4f1a30345b6ed8a82ee67ab547bae21961fbb2ca`  
		Last Modified: Wed, 22 Jul 2020 14:29:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b472157993683c6521c6a749dcaf5f738644f3f53d8052992f1d6f2a58241134
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43682171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474e080ebd414279ac5cc1b391d09fd14f2c0f0f2b5d4163e2b7b511dc0bf63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:30 GMT
ADD file:3d69e3d8fb19d3a9c5fc738b4c9b3c436f9ba10b16c057523360b3443dcd7570 in / 
# Tue, 04 Aug 2020 05:01:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:40:09 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 08:40:21 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 04 Aug 2020 08:41:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 08:41:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 08:41:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 08:42:00 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 08:42:09 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 08:42:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 08:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 08:42:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b33d4edf196b4a005f13932d074987a85eb6c927dc64b40989598b3ade8ebc5c`  
		Last Modified: Tue, 04 Aug 2020 05:09:01 GMT  
		Size: 19.3 MB (19304611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb933ad4bb85672991fffc11bb98b3d11d98ccd0523793e0699c1eb81ca6817e`  
		Last Modified: Tue, 04 Aug 2020 08:45:40 GMT  
		Size: 3.9 MB (3878320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e7f92e0d97f7611b2ea85e9ce43ed573114f4c05315e5d29761d14cf10d2b4`  
		Last Modified: Tue, 04 Aug 2020 08:45:46 GMT  
		Size: 20.5 MB (20474838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42b56a534c9cb1da08e138f42d23c5be9ffc1cbeacf3ec51a7866ad149101df`  
		Last Modified: Tue, 04 Aug 2020 08:45:39 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed665ba4db94e43d7a67f3fea32ee117825dcda905a01295961cd5ddad302f`  
		Last Modified: Tue, 04 Aug 2020 08:45:39 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90ffec65b1574e6f5d51cbfcdf5db44742f82d7679002cd2222194163bc4a25`  
		Last Modified: Tue, 04 Aug 2020 08:45:39 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:45936e18f936091d7200098777edbbcb79ee53eb11ec23a0f653b5971088e04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45155274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a57ed0a0378f67bd01e15acde6dee49623da81750ba04c1fbf2455ce14c7f95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:54:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 03:54:34 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 22 Jul 2020 03:54:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 03:54:54 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 03:54:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 03:54:56 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 03:54:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 03:54:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 03:54:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 03:55:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d8f60d00fb56595938836c6faea921ccfa56f27f56a535aaebaef899109b70`  
		Last Modified: Wed, 22 Jul 2020 03:56:35 GMT  
		Size: 4.1 MB (4081117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d4ca58cd5006cf2417d04b400827cf07799ae8671f2557f633ceed2c0844e`  
		Last Modified: Wed, 22 Jul 2020 03:56:39 GMT  
		Size: 20.7 MB (20678603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f4dc2d67f6780a29082efb8284cda3b1a219f3d2693b1aea277b1a0aa2e6e3`  
		Last Modified: Wed, 22 Jul 2020 03:56:33 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7684d56f9d244e46f9d78b441e3364a1b40abaf0c268ffecde8fd1e9a49992`  
		Last Modified: Wed, 22 Jul 2020 03:56:33 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb33685dacbd4224b2a0c462cb4225a5e3190516c334c8210a50f4b20c24434`  
		Last Modified: Wed, 22 Jul 2020 03:56:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:796188cfeb6cecef6ecf4126d79b63e99b0d10348be0ab1c344ef2ca0825a379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:6700af7c246e818c12a557a5bc116eee27071a94b81891977454d9acd281150c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49103653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f04dd9cce852b4850362cf80e3c49a4dc3ee1ff2132830576bd9cc29fe4313`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:27:47 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 14:27:48 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 22 Jul 2020 14:27:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 14:27:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 14:27:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 14:27:59 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 14:27:59 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 14:28:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 14:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 14:28:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011add3cc110ad3f6b35112efe187883f225c05f5fd2b6a18970832cd666dba3`  
		Last Modified: Wed, 22 Jul 2020 14:29:04 GMT  
		Size: 4.5 MB (4504495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8f79c2ae69a0011f4e8fa0cca8286907d16844997f9e540ac4e2cf374e1696`  
		Last Modified: Wed, 22 Jul 2020 14:29:08 GMT  
		Size: 22.1 MB (22059129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8777822333ab85f3b9f5721283867cfceffe0d293e95011b972bd0188ddab952`  
		Last Modified: Wed, 22 Jul 2020 14:29:03 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a664af4ed9fabf9d51c9ea562efbbf5c3e38150be1f6e91d6d64494224e1d3`  
		Last Modified: Wed, 22 Jul 2020 14:29:03 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db67c489e156b6d2641ab49d4f1a30345b6ed8a82ee67ab547bae21961fbb2ca`  
		Last Modified: Wed, 22 Jul 2020 14:29:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b472157993683c6521c6a749dcaf5f738644f3f53d8052992f1d6f2a58241134
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43682171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5474e080ebd414279ac5cc1b391d09fd14f2c0f0f2b5d4163e2b7b511dc0bf63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:30 GMT
ADD file:3d69e3d8fb19d3a9c5fc738b4c9b3c436f9ba10b16c057523360b3443dcd7570 in / 
# Tue, 04 Aug 2020 05:01:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:40:09 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 08:40:21 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Tue, 04 Aug 2020 08:41:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 08:41:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 08:41:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 08:42:00 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 08:42:09 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 08:42:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 08:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 08:42:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b33d4edf196b4a005f13932d074987a85eb6c927dc64b40989598b3ade8ebc5c`  
		Last Modified: Tue, 04 Aug 2020 05:09:01 GMT  
		Size: 19.3 MB (19304611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb933ad4bb85672991fffc11bb98b3d11d98ccd0523793e0699c1eb81ca6817e`  
		Last Modified: Tue, 04 Aug 2020 08:45:40 GMT  
		Size: 3.9 MB (3878320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e7f92e0d97f7611b2ea85e9ce43ed573114f4c05315e5d29761d14cf10d2b4`  
		Last Modified: Tue, 04 Aug 2020 08:45:46 GMT  
		Size: 20.5 MB (20474838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42b56a534c9cb1da08e138f42d23c5be9ffc1cbeacf3ec51a7866ad149101df`  
		Last Modified: Tue, 04 Aug 2020 08:45:39 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed665ba4db94e43d7a67f3fea32ee117825dcda905a01295961cd5ddad302f`  
		Last Modified: Tue, 04 Aug 2020 08:45:39 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90ffec65b1574e6f5d51cbfcdf5db44742f82d7679002cd2222194163bc4a25`  
		Last Modified: Tue, 04 Aug 2020 08:45:39 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:45936e18f936091d7200098777edbbcb79ee53eb11ec23a0f653b5971088e04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45155274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a57ed0a0378f67bd01e15acde6dee49623da81750ba04c1fbf2455ce14c7f95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:54:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 03:54:34 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Wed, 22 Jul 2020 03:54:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 03:54:54 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 03:54:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 03:54:56 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 03:54:57 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 03:54:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 03:54:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 03:55:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d8f60d00fb56595938836c6faea921ccfa56f27f56a535aaebaef899109b70`  
		Last Modified: Wed, 22 Jul 2020 03:56:35 GMT  
		Size: 4.1 MB (4081117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d4ca58cd5006cf2417d04b400827cf07799ae8671f2557f633ceed2c0844e`  
		Last Modified: Wed, 22 Jul 2020 03:56:39 GMT  
		Size: 20.7 MB (20678603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f4dc2d67f6780a29082efb8284cda3b1a219f3d2693b1aea277b1a0aa2e6e3`  
		Last Modified: Wed, 22 Jul 2020 03:56:33 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7684d56f9d244e46f9d78b441e3364a1b40abaf0c268ffecde8fd1e9a49992`  
		Last Modified: Wed, 22 Jul 2020 03:56:33 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb33685dacbd4224b2a0c462cb4225a5e3190516c334c8210a50f4b20c24434`  
		Last Modified: Wed, 22 Jul 2020 03:56:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:8b5e2793e1570559ff7247f7c5450da4a4a6ca7aead6954385e96ff6d5e38e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ce263c3be955de8c981a1ab27ec8e9f708b5ad6f8c5bbf9a24de6a37a55f4a2b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14835877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8649ced6b1592966bbebd732ee346cb3d11ce69ae0d304e2af61f49e1df52ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 14:15:55 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Mon, 03 Aug 2020 21:32:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 21:32:45 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Mon, 03 Aug 2020 21:32:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 03 Aug 2020 21:32:46 GMT
EXPOSE 8888
# Mon, 03 Aug 2020 21:32:46 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Aug 2020 21:32:47 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 03 Aug 2020 21:32:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 21:32:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad2a461d94a9e83c05e7ac3100b51a9d0865b7a98a91aba6e7bd49df2e7369d`  
		Last Modified: Mon, 03 Aug 2020 21:33:44 GMT  
		Size: 11.7 MB (11736844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cdc432f9cfe4724a455ed16902607feca2aa6dcab7e0e8fb5c237d46fb0515`  
		Last Modified: Mon, 03 Aug 2020 21:33:42 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94c68972d4a6047da03e71631450ae74dc4b1a9f68619970ff24ae4031d6e79`  
		Last Modified: Mon, 03 Aug 2020 21:33:42 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac1d6f07fe2d197c07705e1a7730bcbaa12e52ac234649b362c07a519a4a4b6`  
		Last Modified: Mon, 03 Aug 2020 21:33:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:8b5e2793e1570559ff7247f7c5450da4a4a6ca7aead6954385e96ff6d5e38e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ce263c3be955de8c981a1ab27ec8e9f708b5ad6f8c5bbf9a24de6a37a55f4a2b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14835877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8649ced6b1592966bbebd732ee346cb3d11ce69ae0d304e2af61f49e1df52ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 14:15:55 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Mon, 03 Aug 2020 21:32:45 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 21:32:45 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Mon, 03 Aug 2020 21:32:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 03 Aug 2020 21:32:46 GMT
EXPOSE 8888
# Mon, 03 Aug 2020 21:32:46 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Aug 2020 21:32:47 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 03 Aug 2020 21:32:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 21:32:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad2a461d94a9e83c05e7ac3100b51a9d0865b7a98a91aba6e7bd49df2e7369d`  
		Last Modified: Mon, 03 Aug 2020 21:33:44 GMT  
		Size: 11.7 MB (11736844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cdc432f9cfe4724a455ed16902607feca2aa6dcab7e0e8fb5c237d46fb0515`  
		Last Modified: Mon, 03 Aug 2020 21:33:42 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94c68972d4a6047da03e71631450ae74dc4b1a9f68619970ff24ae4031d6e79`  
		Last Modified: Mon, 03 Aug 2020 21:33:42 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac1d6f07fe2d197c07705e1a7730bcbaa12e52ac234649b362c07a519a4a4b6`  
		Last Modified: Mon, 03 Aug 2020 21:33:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:c242065a4f8eb4b4c3941d3a752020844acd270dc2a663db83d3a1c99eff4eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:ac98cc5a84399bb190edc5726f95c6f9941b79b300d1c54a4841d72601bc93d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65353555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02beacc6b92a50d48288339cb359b6c066177daea79acbd0832e8cbe8db21f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:27:47 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 14:28:09 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 22 Jul 2020 14:28:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 14:28:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 14:28:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 14:28:21 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 14:28:21 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 14:28:21 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 14:28:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 14:28:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011add3cc110ad3f6b35112efe187883f225c05f5fd2b6a18970832cd666dba3`  
		Last Modified: Wed, 22 Jul 2020 14:29:04 GMT  
		Size: 4.5 MB (4504495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a73b9a9291e166af23c99406c6b2c0706cb6b56c26f994951cdc5ad031f54`  
		Last Modified: Wed, 22 Jul 2020 14:29:20 GMT  
		Size: 38.3 MB (38309033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e77eb1ddaa8684c1b7bc0e2a8ef044c6269b77779b16c214d1d22a95a856e4e`  
		Last Modified: Wed, 22 Jul 2020 14:29:13 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a73014a64d1363b61ec49526b7072dba40bf3d69fab22a9b91fb3f221312b9`  
		Last Modified: Wed, 22 Jul 2020 14:29:14 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae39773046373e8c50432e49bc2b8e44244616a1b76697803d00e75ba64c1a69`  
		Last Modified: Wed, 22 Jul 2020 14:29:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9bfa82e88c4e414e26d3de28d4eccc868fadddfb7fe05a1a4f4e04334f69f36c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58959657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c488391ea19f9edcfb2c6a344c0478d602672053e1ab0240a288cc372c897`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:30 GMT
ADD file:3d69e3d8fb19d3a9c5fc738b4c9b3c436f9ba10b16c057523360b3443dcd7570 in / 
# Tue, 04 Aug 2020 05:01:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:40:09 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 08:43:09 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Aug 2020 08:44:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 08:44:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 08:44:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 08:44:23 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 08:44:26 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 08:44:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 08:44:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 08:44:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b33d4edf196b4a005f13932d074987a85eb6c927dc64b40989598b3ade8ebc5c`  
		Last Modified: Tue, 04 Aug 2020 05:09:01 GMT  
		Size: 19.3 MB (19304611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb933ad4bb85672991fffc11bb98b3d11d98ccd0523793e0699c1eb81ca6817e`  
		Last Modified: Tue, 04 Aug 2020 08:45:40 GMT  
		Size: 3.9 MB (3878320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fa3e46c20d6342a32f4bd3473fe5daf746811c4063cb533a8e86344b016ea5`  
		Last Modified: Tue, 04 Aug 2020 08:46:07 GMT  
		Size: 35.8 MB (35752327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e3f2101a123761af772978b35c286415d31462d0e9d0762c721f241261eb7d`  
		Last Modified: Tue, 04 Aug 2020 08:45:53 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c29ae49c457f8714c437eac4d0befc8c927bd54fd383eb41ff112daa2c5a76`  
		Last Modified: Tue, 04 Aug 2020 08:45:53 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e397f9f1bd96ce9ac240b8b1ec7c03c20b63c0d0de27a1637d00606ed2052ee6`  
		Last Modified: Tue, 04 Aug 2020 08:45:53 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0b505507f0228462fb26ba4e1c9ce623c92e2c9b7ce49faab0b412745de8d485
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60438171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddd148edc211baad7730baef4cacf90b6979e26b7fc778534907922300133f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:54:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 03:55:10 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 22 Jul 2020 03:55:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 03:55:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 03:55:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 03:55:37 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 03:55:39 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 03:55:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 03:55:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 03:55:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d8f60d00fb56595938836c6faea921ccfa56f27f56a535aaebaef899109b70`  
		Last Modified: Wed, 22 Jul 2020 03:56:35 GMT  
		Size: 4.1 MB (4081117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22a65e43813c3e3c1f8b563bda8af972632ccb410b20e4936efe55cf3436c02`  
		Last Modified: Wed, 22 Jul 2020 03:56:58 GMT  
		Size: 36.0 MB (35961503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b928c4d4087286cbe74d4bf880530136bd0003d1e2e0c188ed6d00f4545e11`  
		Last Modified: Wed, 22 Jul 2020 03:56:46 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d337cb5f8321a8300d5e0907df8213f28793e13f42ddb3565921a33654e2384`  
		Last Modified: Wed, 22 Jul 2020 03:56:46 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20374d91cb0b683a03b8cac133b1412736b80e70861e0bec0681847f0dbe1f8`  
		Last Modified: Wed, 22 Jul 2020 03:56:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:c242065a4f8eb4b4c3941d3a752020844acd270dc2a663db83d3a1c99eff4eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:ac98cc5a84399bb190edc5726f95c6f9941b79b300d1c54a4841d72601bc93d3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65353555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02beacc6b92a50d48288339cb359b6c066177daea79acbd0832e8cbe8db21f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:27:47 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 14:28:09 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 22 Jul 2020 14:28:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 14:28:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 14:28:21 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 14:28:21 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 14:28:21 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 14:28:21 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 14:28:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 14:28:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011add3cc110ad3f6b35112efe187883f225c05f5fd2b6a18970832cd666dba3`  
		Last Modified: Wed, 22 Jul 2020 14:29:04 GMT  
		Size: 4.5 MB (4504495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a73b9a9291e166af23c99406c6b2c0706cb6b56c26f994951cdc5ad031f54`  
		Last Modified: Wed, 22 Jul 2020 14:29:20 GMT  
		Size: 38.3 MB (38309033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e77eb1ddaa8684c1b7bc0e2a8ef044c6269b77779b16c214d1d22a95a856e4e`  
		Last Modified: Wed, 22 Jul 2020 14:29:13 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a73014a64d1363b61ec49526b7072dba40bf3d69fab22a9b91fb3f221312b9`  
		Last Modified: Wed, 22 Jul 2020 14:29:14 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae39773046373e8c50432e49bc2b8e44244616a1b76697803d00e75ba64c1a69`  
		Last Modified: Wed, 22 Jul 2020 14:29:13 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9bfa82e88c4e414e26d3de28d4eccc868fadddfb7fe05a1a4f4e04334f69f36c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58959657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c488391ea19f9edcfb2c6a344c0478d602672053e1ab0240a288cc372c897`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:30 GMT
ADD file:3d69e3d8fb19d3a9c5fc738b4c9b3c436f9ba10b16c057523360b3443dcd7570 in / 
# Tue, 04 Aug 2020 05:01:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:40:09 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 08:43:09 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Aug 2020 08:44:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 08:44:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 08:44:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 08:44:23 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 08:44:26 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 08:44:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 08:44:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 08:44:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b33d4edf196b4a005f13932d074987a85eb6c927dc64b40989598b3ade8ebc5c`  
		Last Modified: Tue, 04 Aug 2020 05:09:01 GMT  
		Size: 19.3 MB (19304611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb933ad4bb85672991fffc11bb98b3d11d98ccd0523793e0699c1eb81ca6817e`  
		Last Modified: Tue, 04 Aug 2020 08:45:40 GMT  
		Size: 3.9 MB (3878320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fa3e46c20d6342a32f4bd3473fe5daf746811c4063cb533a8e86344b016ea5`  
		Last Modified: Tue, 04 Aug 2020 08:46:07 GMT  
		Size: 35.8 MB (35752327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e3f2101a123761af772978b35c286415d31462d0e9d0762c721f241261eb7d`  
		Last Modified: Tue, 04 Aug 2020 08:45:53 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c29ae49c457f8714c437eac4d0befc8c927bd54fd383eb41ff112daa2c5a76`  
		Last Modified: Tue, 04 Aug 2020 08:45:53 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e397f9f1bd96ce9ac240b8b1ec7c03c20b63c0d0de27a1637d00606ed2052ee6`  
		Last Modified: Tue, 04 Aug 2020 08:45:53 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0b505507f0228462fb26ba4e1c9ce623c92e2c9b7ce49faab0b412745de8d485
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60438171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddd148edc211baad7730baef4cacf90b6979e26b7fc778534907922300133f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:54:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 03:55:10 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 22 Jul 2020 03:55:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 03:55:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 03:55:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 03:55:37 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 03:55:39 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 03:55:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 03:55:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 03:55:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d8f60d00fb56595938836c6faea921ccfa56f27f56a535aaebaef899109b70`  
		Last Modified: Wed, 22 Jul 2020 03:56:35 GMT  
		Size: 4.1 MB (4081117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22a65e43813c3e3c1f8b563bda8af972632ccb410b20e4936efe55cf3436c02`  
		Last Modified: Wed, 22 Jul 2020 03:56:58 GMT  
		Size: 36.0 MB (35961503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b928c4d4087286cbe74d4bf880530136bd0003d1e2e0c188ed6d00f4545e11`  
		Last Modified: Wed, 22 Jul 2020 03:56:46 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d337cb5f8321a8300d5e0907df8213f28793e13f42ddb3565921a33654e2384`  
		Last Modified: Wed, 22 Jul 2020 03:56:46 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20374d91cb0b683a03b8cac133b1412736b80e70861e0bec0681847f0dbe1f8`  
		Last Modified: Wed, 22 Jul 2020 03:56:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:9e142f96d1e59f2d16bc911d8218f32c7fcb953bd9219ed4aa6a1aec80feafd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6de3038de5bfa3c30e29f92cb692891ad5589bfd0685791e8dcd0cd9e7738fbd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22654480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955a8a8d49d6556ddff70295ba506a92749c8a3d9649f42112bce1c131d0d0d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 14:16:07 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Aug 2020 21:33:05 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 21:33:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 03 Aug 2020 21:33:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 03 Aug 2020 21:33:06 GMT
EXPOSE 8888
# Mon, 03 Aug 2020 21:33:06 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Aug 2020 21:33:07 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 03 Aug 2020 21:33:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 21:33:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fb3c1fd27ac60812f13b8431fe6b568c8ec036d41060b0e9af28a14ae347c2`  
		Last Modified: Mon, 03 Aug 2020 21:33:53 GMT  
		Size: 19.6 MB (19555445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea987ddcdf39356383a402c25ee31e41ba5f01b1ab246d404283554548bd8c7`  
		Last Modified: Mon, 03 Aug 2020 21:33:48 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d601a83cf3261202419211d707c9f65ff27b7506ecb6a3f8cac9311742d2d8f1`  
		Last Modified: Mon, 03 Aug 2020 21:33:47 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dd6de70ac133ce6e468c9bc620a1e68a425760493002a271500163536679c7`  
		Last Modified: Mon, 03 Aug 2020 21:33:47 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:9e142f96d1e59f2d16bc911d8218f32c7fcb953bd9219ed4aa6a1aec80feafd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6de3038de5bfa3c30e29f92cb692891ad5589bfd0685791e8dcd0cd9e7738fbd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22654480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955a8a8d49d6556ddff70295ba506a92749c8a3d9649f42112bce1c131d0d0d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Apr 2020 14:16:07 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Aug 2020 21:33:05 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 21:33:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 03 Aug 2020 21:33:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 03 Aug 2020 21:33:06 GMT
EXPOSE 8888
# Mon, 03 Aug 2020 21:33:06 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Aug 2020 21:33:07 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 03 Aug 2020 21:33:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 21:33:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fb3c1fd27ac60812f13b8431fe6b568c8ec036d41060b0e9af28a14ae347c2`  
		Last Modified: Mon, 03 Aug 2020 21:33:53 GMT  
		Size: 19.6 MB (19555445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea987ddcdf39356383a402c25ee31e41ba5f01b1ab246d404283554548bd8c7`  
		Last Modified: Mon, 03 Aug 2020 21:33:48 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d601a83cf3261202419211d707c9f65ff27b7506ecb6a3f8cac9311742d2d8f1`  
		Last Modified: Mon, 03 Aug 2020 21:33:47 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dd6de70ac133ce6e468c9bc620a1e68a425760493002a271500163536679c7`  
		Last Modified: Mon, 03 Aug 2020 21:33:47 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:affd5ca87751dd1c9b236e2e6f28319cbd6618eb06a545b3c268336a72bf4ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:eb16ce93b2ac9e43efb558def0c0b32d4585808318131aa738651528a9490ec1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70156009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90084dc4d6557ed11f483f58df4e580061197f64660d4b29c5f72ee284462f07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:27:47 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 14:28:33 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Wed, 22 Jul 2020 14:28:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 14:28:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 14:28:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 14:28:47 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 14:28:47 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 14:28:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 14:28:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 14:28:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011add3cc110ad3f6b35112efe187883f225c05f5fd2b6a18970832cd666dba3`  
		Last Modified: Wed, 22 Jul 2020 14:29:04 GMT  
		Size: 4.5 MB (4504495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9039be444701e86baea26bfbcd66174c432346cbe6e7799bd2493e72ff1b2e09`  
		Last Modified: Wed, 22 Jul 2020 14:29:35 GMT  
		Size: 43.1 MB (43111489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590482f0c329d0629f168ed1bf1ad04d98183d02468092a006530d3365351d5e`  
		Last Modified: Wed, 22 Jul 2020 14:29:25 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87193b8748c39dc2acb32fe225498ca24f2cb4d6bb606426ecdb541aaf0f04a6`  
		Last Modified: Wed, 22 Jul 2020 14:29:25 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e38caae5cf53acb8089425cbc26d123d0c5bd53df546911a75911d0bc3fda60`  
		Last Modified: Wed, 22 Jul 2020 14:29:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c0803f5c98a9b606fea7ea6fa6fb50a2bc93750996bc83ffb304c47f528ad71c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63563753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f9b03033028bf7afdee09c44e3a2f5ca551e4e125528907c13098da0d98858`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:30 GMT
ADD file:3d69e3d8fb19d3a9c5fc738b4c9b3c436f9ba10b16c057523360b3443dcd7570 in / 
# Tue, 04 Aug 2020 05:01:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:40:09 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 08:44:50 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Tue, 04 Aug 2020 08:45:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 08:45:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 08:45:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 08:45:22 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 08:45:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 08:45:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 08:45:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 08:45:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b33d4edf196b4a005f13932d074987a85eb6c927dc64b40989598b3ade8ebc5c`  
		Last Modified: Tue, 04 Aug 2020 05:09:01 GMT  
		Size: 19.3 MB (19304611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb933ad4bb85672991fffc11bb98b3d11d98ccd0523793e0699c1eb81ca6817e`  
		Last Modified: Tue, 04 Aug 2020 08:45:40 GMT  
		Size: 3.9 MB (3878320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56d04542cfbbb40ecceb3fb0857d765f0e9907bf4600635efb17582d63075af`  
		Last Modified: Tue, 04 Aug 2020 08:46:24 GMT  
		Size: 40.4 MB (40356413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc095732d5a67cce2400ab2414f1df138953b3f3dced02f04ef888cf7bca469`  
		Last Modified: Tue, 04 Aug 2020 08:46:13 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd518336b8728bf95dafdf81b66d9663cbea4d2f4c704d43ae4c87a67e08f06`  
		Last Modified: Tue, 04 Aug 2020 08:46:14 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5247c0d8a61cdbdcb822b8b41db097f237b43fcef962c21317e43f883533ec1d`  
		Last Modified: Tue, 04 Aug 2020 08:46:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6823b65d59f8309d89c1f8c2f59342f68094749504a9f2675379975134c3e4df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64678184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d2cd5edf5e8a5659f21fa5819cdd81786858310d4dd02e9c39c80a6599a3c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:54:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 03:55:52 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Wed, 22 Jul 2020 03:56:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 03:56:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 03:56:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 03:56:17 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 03:56:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 03:56:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 03:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 03:56:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d8f60d00fb56595938836c6faea921ccfa56f27f56a535aaebaef899109b70`  
		Last Modified: Wed, 22 Jul 2020 03:56:35 GMT  
		Size: 4.1 MB (4081117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba97713f436dec5d766866f77e876bfb1e218ca8e3dd9634f26846b295c94ab7`  
		Last Modified: Wed, 22 Jul 2020 03:57:15 GMT  
		Size: 40.2 MB (40201524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a8411313dcabd189e88b78f970053bd9626a33a395b99514d0313785d9f19f`  
		Last Modified: Wed, 22 Jul 2020 03:57:04 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150fa78e42d7d7391a444df85d25f63729b4cb5e4fa419c6dbcbdeac641756fa`  
		Last Modified: Wed, 22 Jul 2020 03:57:04 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433807d0fa44d021351e4e7fd89136a35ff3bb79fe6ea2eeb9f08f1695809c8`  
		Last Modified: Wed, 22 Jul 2020 03:57:04 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.4`

```console
$ docker pull chronograf@sha256:affd5ca87751dd1c9b236e2e6f28319cbd6618eb06a545b3c268336a72bf4ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.4` - linux; amd64

```console
$ docker pull chronograf@sha256:eb16ce93b2ac9e43efb558def0c0b32d4585808318131aa738651528a9490ec1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70156009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90084dc4d6557ed11f483f58df4e580061197f64660d4b29c5f72ee284462f07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:27:47 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 14:28:33 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Wed, 22 Jul 2020 14:28:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 14:28:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 14:28:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 14:28:47 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 14:28:47 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 14:28:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 14:28:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 14:28:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011add3cc110ad3f6b35112efe187883f225c05f5fd2b6a18970832cd666dba3`  
		Last Modified: Wed, 22 Jul 2020 14:29:04 GMT  
		Size: 4.5 MB (4504495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9039be444701e86baea26bfbcd66174c432346cbe6e7799bd2493e72ff1b2e09`  
		Last Modified: Wed, 22 Jul 2020 14:29:35 GMT  
		Size: 43.1 MB (43111489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590482f0c329d0629f168ed1bf1ad04d98183d02468092a006530d3365351d5e`  
		Last Modified: Wed, 22 Jul 2020 14:29:25 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87193b8748c39dc2acb32fe225498ca24f2cb4d6bb606426ecdb541aaf0f04a6`  
		Last Modified: Wed, 22 Jul 2020 14:29:25 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e38caae5cf53acb8089425cbc26d123d0c5bd53df546911a75911d0bc3fda60`  
		Last Modified: Wed, 22 Jul 2020 14:29:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c0803f5c98a9b606fea7ea6fa6fb50a2bc93750996bc83ffb304c47f528ad71c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63563753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f9b03033028bf7afdee09c44e3a2f5ca551e4e125528907c13098da0d98858`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:30 GMT
ADD file:3d69e3d8fb19d3a9c5fc738b4c9b3c436f9ba10b16c057523360b3443dcd7570 in / 
# Tue, 04 Aug 2020 05:01:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:40:09 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 08:44:50 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Tue, 04 Aug 2020 08:45:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 08:45:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 08:45:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 08:45:22 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 08:45:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 08:45:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 08:45:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 08:45:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b33d4edf196b4a005f13932d074987a85eb6c927dc64b40989598b3ade8ebc5c`  
		Last Modified: Tue, 04 Aug 2020 05:09:01 GMT  
		Size: 19.3 MB (19304611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb933ad4bb85672991fffc11bb98b3d11d98ccd0523793e0699c1eb81ca6817e`  
		Last Modified: Tue, 04 Aug 2020 08:45:40 GMT  
		Size: 3.9 MB (3878320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56d04542cfbbb40ecceb3fb0857d765f0e9907bf4600635efb17582d63075af`  
		Last Modified: Tue, 04 Aug 2020 08:46:24 GMT  
		Size: 40.4 MB (40356413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc095732d5a67cce2400ab2414f1df138953b3f3dced02f04ef888cf7bca469`  
		Last Modified: Tue, 04 Aug 2020 08:46:13 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd518336b8728bf95dafdf81b66d9663cbea4d2f4c704d43ae4c87a67e08f06`  
		Last Modified: Tue, 04 Aug 2020 08:46:14 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5247c0d8a61cdbdcb822b8b41db097f237b43fcef962c21317e43f883533ec1d`  
		Last Modified: Tue, 04 Aug 2020 08:46:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6823b65d59f8309d89c1f8c2f59342f68094749504a9f2675379975134c3e4df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64678184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d2cd5edf5e8a5659f21fa5819cdd81786858310d4dd02e9c39c80a6599a3c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:54:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 03:55:52 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Wed, 22 Jul 2020 03:56:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 03:56:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 03:56:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 03:56:17 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 03:56:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 03:56:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 03:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 03:56:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d8f60d00fb56595938836c6faea921ccfa56f27f56a535aaebaef899109b70`  
		Last Modified: Wed, 22 Jul 2020 03:56:35 GMT  
		Size: 4.1 MB (4081117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba97713f436dec5d766866f77e876bfb1e218ca8e3dd9634f26846b295c94ab7`  
		Last Modified: Wed, 22 Jul 2020 03:57:15 GMT  
		Size: 40.2 MB (40201524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a8411313dcabd189e88b78f970053bd9626a33a395b99514d0313785d9f19f`  
		Last Modified: Wed, 22 Jul 2020 03:57:04 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150fa78e42d7d7391a444df85d25f63729b4cb5e4fa419c6dbcbdeac641756fa`  
		Last Modified: Wed, 22 Jul 2020 03:57:04 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433807d0fa44d021351e4e7fd89136a35ff3bb79fe6ea2eeb9f08f1695809c8`  
		Last Modified: Wed, 22 Jul 2020 03:57:04 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.4-alpine`

```console
$ docker pull chronograf@sha256:a6b13d0a51eb1b4a0951f7f8c643a0b8912d5c3e90b4bebf36e59ea55dd4b08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d97c84648622edbbcc4a17368d391d8019d06b5a8b37f563cf9f782703c270f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25332564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a897eb8d8ae312666e53b0a5637e8bcaef01895a2f262c8b18394bbbd8bfd54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 02 May 2020 01:26:58 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Mon, 03 Aug 2020 21:33:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 21:33:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 03 Aug 2020 21:33:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 03 Aug 2020 21:33:27 GMT
EXPOSE 8888
# Mon, 03 Aug 2020 21:33:28 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Aug 2020 21:33:28 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 03 Aug 2020 21:33:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 21:33:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2779a624bcff151fcd76c8575c9afd21e7e6bd9680f3133353f0cbd95e35086e`  
		Last Modified: Mon, 03 Aug 2020 21:34:04 GMT  
		Size: 22.2 MB (22233529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abc082624ce1eba1e966d8f966ed74e677b75fcb1e6d1fcc4a4ee4405d49310`  
		Last Modified: Mon, 03 Aug 2020 21:33:58 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350b64ea4f91f91a969b180e2e736101b32383ebccfa6705f7d9bffc12ed281a`  
		Last Modified: Mon, 03 Aug 2020 21:33:58 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0666c9baa39669e204205a50a47f1f49b6fff7ad97a1870fa3eb44c4cf2b7d9`  
		Last Modified: Mon, 03 Aug 2020 21:33:58 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:a6b13d0a51eb1b4a0951f7f8c643a0b8912d5c3e90b4bebf36e59ea55dd4b08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d97c84648622edbbcc4a17368d391d8019d06b5a8b37f563cf9f782703c270f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25332564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a897eb8d8ae312666e53b0a5637e8bcaef01895a2f262c8b18394bbbd8bfd54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 02 May 2020 01:26:58 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Mon, 03 Aug 2020 21:33:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 21:33:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 03 Aug 2020 21:33:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 03 Aug 2020 21:33:27 GMT
EXPOSE 8888
# Mon, 03 Aug 2020 21:33:28 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Aug 2020 21:33:28 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 03 Aug 2020 21:33:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 21:33:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2779a624bcff151fcd76c8575c9afd21e7e6bd9680f3133353f0cbd95e35086e`  
		Last Modified: Mon, 03 Aug 2020 21:34:04 GMT  
		Size: 22.2 MB (22233529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abc082624ce1eba1e966d8f966ed74e677b75fcb1e6d1fcc4a4ee4405d49310`  
		Last Modified: Mon, 03 Aug 2020 21:33:58 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350b64ea4f91f91a969b180e2e736101b32383ebccfa6705f7d9bffc12ed281a`  
		Last Modified: Mon, 03 Aug 2020 21:33:58 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0666c9baa39669e204205a50a47f1f49b6fff7ad97a1870fa3eb44c4cf2b7d9`  
		Last Modified: Mon, 03 Aug 2020 21:33:58 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:a6b13d0a51eb1b4a0951f7f8c643a0b8912d5c3e90b4bebf36e59ea55dd4b08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d97c84648622edbbcc4a17368d391d8019d06b5a8b37f563cf9f782703c270f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25332564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a897eb8d8ae312666e53b0a5637e8bcaef01895a2f262c8b18394bbbd8bfd54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 14:15:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 02 May 2020 01:26:58 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Mon, 03 Aug 2020 21:33:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 21:33:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 03 Aug 2020 21:33:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 03 Aug 2020 21:33:27 GMT
EXPOSE 8888
# Mon, 03 Aug 2020 21:33:28 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Aug 2020 21:33:28 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 03 Aug 2020 21:33:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 21:33:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c949b60b63fb4b31e70314aba2aff2223f42a54c0d76cdb28917f161840b03`  
		Last Modified: Fri, 24 Apr 2020 14:16:39 GMT  
		Size: 301.1 KB (301092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2779a624bcff151fcd76c8575c9afd21e7e6bd9680f3133353f0cbd95e35086e`  
		Last Modified: Mon, 03 Aug 2020 21:34:04 GMT  
		Size: 22.2 MB (22233529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abc082624ce1eba1e966d8f966ed74e677b75fcb1e6d1fcc4a4ee4405d49310`  
		Last Modified: Mon, 03 Aug 2020 21:33:58 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350b64ea4f91f91a969b180e2e736101b32383ebccfa6705f7d9bffc12ed281a`  
		Last Modified: Mon, 03 Aug 2020 21:33:58 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0666c9baa39669e204205a50a47f1f49b6fff7ad97a1870fa3eb44c4cf2b7d9`  
		Last Modified: Mon, 03 Aug 2020 21:33:58 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:affd5ca87751dd1c9b236e2e6f28319cbd6618eb06a545b3c268336a72bf4ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:eb16ce93b2ac9e43efb558def0c0b32d4585808318131aa738651528a9490ec1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70156009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90084dc4d6557ed11f483f58df4e580061197f64660d4b29c5f72ee284462f07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:27:47 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 14:28:33 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Wed, 22 Jul 2020 14:28:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 14:28:46 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 14:28:46 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 14:28:47 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 14:28:47 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 14:28:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 14:28:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 14:28:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011add3cc110ad3f6b35112efe187883f225c05f5fd2b6a18970832cd666dba3`  
		Last Modified: Wed, 22 Jul 2020 14:29:04 GMT  
		Size: 4.5 MB (4504495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9039be444701e86baea26bfbcd66174c432346cbe6e7799bd2493e72ff1b2e09`  
		Last Modified: Wed, 22 Jul 2020 14:29:35 GMT  
		Size: 43.1 MB (43111489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590482f0c329d0629f168ed1bf1ad04d98183d02468092a006530d3365351d5e`  
		Last Modified: Wed, 22 Jul 2020 14:29:25 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87193b8748c39dc2acb32fe225498ca24f2cb4d6bb606426ecdb541aaf0f04a6`  
		Last Modified: Wed, 22 Jul 2020 14:29:25 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e38caae5cf53acb8089425cbc26d123d0c5bd53df546911a75911d0bc3fda60`  
		Last Modified: Wed, 22 Jul 2020 14:29:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c0803f5c98a9b606fea7ea6fa6fb50a2bc93750996bc83ffb304c47f528ad71c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63563753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f9b03033028bf7afdee09c44e3a2f5ca551e4e125528907c13098da0d98858`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:30 GMT
ADD file:3d69e3d8fb19d3a9c5fc738b4c9b3c436f9ba10b16c057523360b3443dcd7570 in / 
# Tue, 04 Aug 2020 05:01:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:40:09 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 08:44:50 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Tue, 04 Aug 2020 08:45:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 08:45:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 08:45:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 08:45:22 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 08:45:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 08:45:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 08:45:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 08:45:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b33d4edf196b4a005f13932d074987a85eb6c927dc64b40989598b3ade8ebc5c`  
		Last Modified: Tue, 04 Aug 2020 05:09:01 GMT  
		Size: 19.3 MB (19304611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb933ad4bb85672991fffc11bb98b3d11d98ccd0523793e0699c1eb81ca6817e`  
		Last Modified: Tue, 04 Aug 2020 08:45:40 GMT  
		Size: 3.9 MB (3878320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56d04542cfbbb40ecceb3fb0857d765f0e9907bf4600635efb17582d63075af`  
		Last Modified: Tue, 04 Aug 2020 08:46:24 GMT  
		Size: 40.4 MB (40356413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc095732d5a67cce2400ab2414f1df138953b3f3dced02f04ef888cf7bca469`  
		Last Modified: Tue, 04 Aug 2020 08:46:13 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd518336b8728bf95dafdf81b66d9663cbea4d2f4c704d43ae4c87a67e08f06`  
		Last Modified: Tue, 04 Aug 2020 08:46:14 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5247c0d8a61cdbdcb822b8b41db097f237b43fcef962c21317e43f883533ec1d`  
		Last Modified: Tue, 04 Aug 2020 08:46:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6823b65d59f8309d89c1f8c2f59342f68094749504a9f2675379975134c3e4df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64678184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d2cd5edf5e8a5659f21fa5819cdd81786858310d4dd02e9c39c80a6599a3c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:54:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 22 Jul 2020 03:55:52 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Wed, 22 Jul 2020 03:56:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 03:56:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 22 Jul 2020 03:56:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 22 Jul 2020 03:56:17 GMT
EXPOSE 8888
# Wed, 22 Jul 2020 03:56:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Jul 2020 03:56:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 22 Jul 2020 03:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 03:56:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d8f60d00fb56595938836c6faea921ccfa56f27f56a535aaebaef899109b70`  
		Last Modified: Wed, 22 Jul 2020 03:56:35 GMT  
		Size: 4.1 MB (4081117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba97713f436dec5d766866f77e876bfb1e218ca8e3dd9634f26846b295c94ab7`  
		Last Modified: Wed, 22 Jul 2020 03:57:15 GMT  
		Size: 40.2 MB (40201524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a8411313dcabd189e88b78f970053bd9626a33a395b99514d0313785d9f19f`  
		Last Modified: Wed, 22 Jul 2020 03:57:04 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150fa78e42d7d7391a444df85d25f63729b4cb5e4fa419c6dbcbdeac641756fa`  
		Last Modified: Wed, 22 Jul 2020 03:57:04 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5433807d0fa44d021351e4e7fd89136a35ff3bb79fe6ea2eeb9f08f1695809c8`  
		Last Modified: Wed, 22 Jul 2020 03:57:04 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
