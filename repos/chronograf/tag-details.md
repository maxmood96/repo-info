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
$ docker pull chronograf@sha256:b0ae594f24c582852736f2030bf0f0c0e606fc9cfc4ae9abad9c8e9d73d242ad
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
$ docker pull chronograf@sha256:153a02a215aaa8961d19beda4981b50a1e5cd136ac706d1fc8c5b9641b56ebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84239561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aeaf681ced1b72825e4f1ea24e8ca4eb6186b32e21b84ef885ae64f4987f01b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1d932a0ae4fdac27b3d3763ea9c42fbaa86dd7c24d4d5219d1abe974862e8`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 7.9 MB (7871459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d41db8d398ef2de7c4620f217b1c37524af4c25cec52653ec55c18914493eb9`  
		Last Modified: Tue, 23 Jul 2024 07:13:40 GMT  
		Size: 47.2 MB (47217352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae19e153971ef49a3da0003f8b6e6ec2bb5dc1435c3967c9a0a6436b922f62`  
		Last Modified: Tue, 23 Jul 2024 07:13:37 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16db583eb504f5d3efeda6a5d49fb5a24e96504e7094a6a533901af06d5a386`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773892334f3852b1fc38a2c88d95dbf20614ea9379fbb88b286feebb62fd3a0`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5f6fe6f20c6467aad2452498eb3fda01eda0ca9ed4d37ff84e39b0723bdbac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad5d155c937d2270cab7ac97116aaf5f6cc25c66c0d3e4e4184ca1fe3feb8d`

```dockerfile
```

-	Layers:
	-	`sha256:7f57cc014e3606b8332ceb8b0fd7730433284ac470e57d7479f939a33ab99fd4`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 2.7 MB (2690949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c214efb73472ebcb8fe23c68e09f034c40b367e852eb592742c9dbae868cf64b`  
		Last Modified: Tue, 23 Jul 2024 07:13:37 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1a1925253a4af6b859760bfc65ea234be4fa7ed68788ba95cfd59e355f75ece7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75514726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124223ba49bd9c978dfd626d0ec5c9bd4a4dc2b2e2308b79a14e6b1b68692996`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
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
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5263b97046c18ec1cc9eed5f67597f161262db97ff87e0a1c9e1ac3991819094`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 6.5 MB (6495958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e255b5aa2e3d8552515670a3387bdb0ee916433eca1005ef3243027f6a472151`  
		Last Modified: Tue, 23 Jul 2024 11:59:05 GMT  
		Size: 44.3 MB (44276098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5134aee981e8f0f8a23da3cdd01a18deab37c4da521c23f6d707cbc87e7d12b`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd13a3c43a4e3a18af3ad90b1b11596d67a6819e3f01eb1276d6ca0b326c801`  
		Last Modified: Tue, 23 Jul 2024 11:59:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cba087ac927520c3d3e4df8d1834088d770890e6216b847a8cde21c288661c`  
		Last Modified: Tue, 23 Jul 2024 11:59:05 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d5fe9141952828d92418ed319d71d9283e715d9be23eb23c93e2988fa8152c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1367b14f917b079b093810d72cb8dcf9f614642a19c713218a8c8f9a6ed52064`

```dockerfile
```

-	Layers:
	-	`sha256:a4cc31fbf6e9f89859fe236515ba0d01a3833903385c0ec41235f45cf5701b38`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 2.7 MB (2693245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92720a9583d26aa8d4f17c73aaa8128ebda7bbd47316561a16f9133cb584d151`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 16.0 KB (16008 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a3e74028deff6e8e750d6aa10c72b4d4ff6d577038dce48df6f9009d2f84552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81800653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e7bffceb49651ea4c8eec41dbd854083d633a69611f8954dc37a61fee377c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc8462b74326e175d556882ef423e4edaaa2ddd6578a0c551e50a500f1012aa`  
		Last Modified: Tue, 23 Jul 2024 12:01:21 GMT  
		Size: 7.6 MB (7649266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c445e41bd816107ae6464a7bc0c85a212f7ae11185771e90913b3b4072c6250`  
		Last Modified: Tue, 23 Jul 2024 12:01:22 GMT  
		Size: 45.0 MB (44970354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e58fcfff7ad0a484da120de538f623575d2da0dbe423d1d046e4ef8ed22722`  
		Last Modified: Tue, 23 Jul 2024 12:01:20 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79818630a46556198aa1441833c8c128c48a838c9339c945a3215d839994d090`  
		Last Modified: Tue, 23 Jul 2024 12:01:20 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f81446c3eac6af221d2244531848ac90e7d7ecf22daccce78a27a9eca07c32`  
		Last Modified: Tue, 23 Jul 2024 12:01:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:58b03acf392a1c6532ffb666bf95feeb6e7adc826df9dec0de0abad573a27902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfec816f07ed8726ec44850bae2c50a29fd8493ab18df9681f99e175ff3eb102`

```dockerfile
```

-	Layers:
	-	`sha256:2380ee8e1620b0de38df95a336e5fd0df31bee359c0829d0b090142bcfad375d`  
		Last Modified: Tue, 23 Jul 2024 12:01:21 GMT  
		Size: 2.7 MB (2691221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d146b7e8f243ee30705f182c43db7088ba5ad1b70989fd726127c9abc058e2`  
		Last Modified: Tue, 23 Jul 2024 12:01:20 GMT  
		Size: 16.2 KB (16231 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:bda6f3cb67284c0da5c9011100201d870ac597821831c340fc1dfc0d314766a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2901c06ba0aa8e1ca321512279411eae4fcc4cd07d1cdd2c9381c46fd51de58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31806919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1e35742a524fbb3a01981ea10844eb8ae62ef954762a43772bcb695a2f9d68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0558a15ffd5fd7dc1a320904adf4538b87b67a939d5d006b98a9b36017947502`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da05f34e03c0428cf96e2e8e8754fecd048b4672e1675c8dfd091987120152`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 292.6 KB (292596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f4131f7e5257e9bc0a1099c0b2f6bced312d6e6f67a5aacc49361fc2c644`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 27.9 MB (27866731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fe17f4dd5d6655838dc7645cfdc88d3d95367154f129fe3d96acac7ee78a03`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c01279850cada9d2f470c39fdb304fc4ce71db414de5c5711c4bf17239418f`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacddbfa4fec719daff43f784bec28523cd8ee4fcc4786ce979c93515cadf4ed`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6529e5937f5575e4cfb5f64c28d37ad905a0661f7072532e29e5ad2854533e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 KB (257227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ed52c6d0f8dbb2cbd26f76933a42d8893154547aa43e6e3b1189777362aae3`

```dockerfile
```

-	Layers:
	-	`sha256:2b633ff9323f7d9bf699a774058c48c851bf8eca1471aba989ded877d8c6b88d`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 239.6 KB (239587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c025800fabbad37f8d0a4823f2cd8491208afe5abbb959cf08ed7afa251e434`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:b0ae594f24c582852736f2030bf0f0c0e606fc9cfc4ae9abad9c8e9d73d242ad
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
$ docker pull chronograf@sha256:153a02a215aaa8961d19beda4981b50a1e5cd136ac706d1fc8c5b9641b56ebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84239561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aeaf681ced1b72825e4f1ea24e8ca4eb6186b32e21b84ef885ae64f4987f01b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1d932a0ae4fdac27b3d3763ea9c42fbaa86dd7c24d4d5219d1abe974862e8`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 7.9 MB (7871459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d41db8d398ef2de7c4620f217b1c37524af4c25cec52653ec55c18914493eb9`  
		Last Modified: Tue, 23 Jul 2024 07:13:40 GMT  
		Size: 47.2 MB (47217352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae19e153971ef49a3da0003f8b6e6ec2bb5dc1435c3967c9a0a6436b922f62`  
		Last Modified: Tue, 23 Jul 2024 07:13:37 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16db583eb504f5d3efeda6a5d49fb5a24e96504e7094a6a533901af06d5a386`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773892334f3852b1fc38a2c88d95dbf20614ea9379fbb88b286feebb62fd3a0`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5f6fe6f20c6467aad2452498eb3fda01eda0ca9ed4d37ff84e39b0723bdbac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad5d155c937d2270cab7ac97116aaf5f6cc25c66c0d3e4e4184ca1fe3feb8d`

```dockerfile
```

-	Layers:
	-	`sha256:7f57cc014e3606b8332ceb8b0fd7730433284ac470e57d7479f939a33ab99fd4`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 2.7 MB (2690949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c214efb73472ebcb8fe23c68e09f034c40b367e852eb592742c9dbae868cf64b`  
		Last Modified: Tue, 23 Jul 2024 07:13:37 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1a1925253a4af6b859760bfc65ea234be4fa7ed68788ba95cfd59e355f75ece7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75514726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124223ba49bd9c978dfd626d0ec5c9bd4a4dc2b2e2308b79a14e6b1b68692996`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
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
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5263b97046c18ec1cc9eed5f67597f161262db97ff87e0a1c9e1ac3991819094`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 6.5 MB (6495958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e255b5aa2e3d8552515670a3387bdb0ee916433eca1005ef3243027f6a472151`  
		Last Modified: Tue, 23 Jul 2024 11:59:05 GMT  
		Size: 44.3 MB (44276098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5134aee981e8f0f8a23da3cdd01a18deab37c4da521c23f6d707cbc87e7d12b`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd13a3c43a4e3a18af3ad90b1b11596d67a6819e3f01eb1276d6ca0b326c801`  
		Last Modified: Tue, 23 Jul 2024 11:59:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cba087ac927520c3d3e4df8d1834088d770890e6216b847a8cde21c288661c`  
		Last Modified: Tue, 23 Jul 2024 11:59:05 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:d5fe9141952828d92418ed319d71d9283e715d9be23eb23c93e2988fa8152c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1367b14f917b079b093810d72cb8dcf9f614642a19c713218a8c8f9a6ed52064`

```dockerfile
```

-	Layers:
	-	`sha256:a4cc31fbf6e9f89859fe236515ba0d01a3833903385c0ec41235f45cf5701b38`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 2.7 MB (2693245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92720a9583d26aa8d4f17c73aaa8128ebda7bbd47316561a16f9133cb584d151`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 16.0 KB (16008 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a3e74028deff6e8e750d6aa10c72b4d4ff6d577038dce48df6f9009d2f84552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81800653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e7bffceb49651ea4c8eec41dbd854083d633a69611f8954dc37a61fee377c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc8462b74326e175d556882ef423e4edaaa2ddd6578a0c551e50a500f1012aa`  
		Last Modified: Tue, 23 Jul 2024 12:01:21 GMT  
		Size: 7.6 MB (7649266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c445e41bd816107ae6464a7bc0c85a212f7ae11185771e90913b3b4072c6250`  
		Last Modified: Tue, 23 Jul 2024 12:01:22 GMT  
		Size: 45.0 MB (44970354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e58fcfff7ad0a484da120de538f623575d2da0dbe423d1d046e4ef8ed22722`  
		Last Modified: Tue, 23 Jul 2024 12:01:20 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79818630a46556198aa1441833c8c128c48a838c9339c945a3215d839994d090`  
		Last Modified: Tue, 23 Jul 2024 12:01:20 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f81446c3eac6af221d2244531848ac90e7d7ecf22daccce78a27a9eca07c32`  
		Last Modified: Tue, 23 Jul 2024 12:01:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:58b03acf392a1c6532ffb666bf95feeb6e7adc826df9dec0de0abad573a27902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfec816f07ed8726ec44850bae2c50a29fd8493ab18df9681f99e175ff3eb102`

```dockerfile
```

-	Layers:
	-	`sha256:2380ee8e1620b0de38df95a336e5fd0df31bee359c0829d0b090142bcfad375d`  
		Last Modified: Tue, 23 Jul 2024 12:01:21 GMT  
		Size: 2.7 MB (2691221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d146b7e8f243ee30705f182c43db7088ba5ad1b70989fd726127c9abc058e2`  
		Last Modified: Tue, 23 Jul 2024 12:01:20 GMT  
		Size: 16.2 KB (16231 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:bda6f3cb67284c0da5c9011100201d870ac597821831c340fc1dfc0d314766a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2901c06ba0aa8e1ca321512279411eae4fcc4cd07d1cdd2c9381c46fd51de58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31806919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1e35742a524fbb3a01981ea10844eb8ae62ef954762a43772bcb695a2f9d68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0558a15ffd5fd7dc1a320904adf4538b87b67a939d5d006b98a9b36017947502`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da05f34e03c0428cf96e2e8e8754fecd048b4672e1675c8dfd091987120152`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 292.6 KB (292596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f4131f7e5257e9bc0a1099c0b2f6bced312d6e6f67a5aacc49361fc2c644`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 27.9 MB (27866731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fe17f4dd5d6655838dc7645cfdc88d3d95367154f129fe3d96acac7ee78a03`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c01279850cada9d2f470c39fdb304fc4ce71db414de5c5711c4bf17239418f`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacddbfa4fec719daff43f784bec28523cd8ee4fcc4786ce979c93515cadf4ed`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6529e5937f5575e4cfb5f64c28d37ad905a0661f7072532e29e5ad2854533e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 KB (257227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ed52c6d0f8dbb2cbd26f76933a42d8893154547aa43e6e3b1189777362aae3`

```dockerfile
```

-	Layers:
	-	`sha256:2b633ff9323f7d9bf699a774058c48c851bf8eca1471aba989ded877d8c6b88d`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 239.6 KB (239587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c025800fabbad37f8d0a4823f2cd8491208afe5abbb959cf08ed7afa251e434`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:97cc1001e2675eb674195421efc213e02a79c112a33773c52182b905091dcc75
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
$ docker pull chronograf@sha256:e5388fc7f8856e93bf58153cbca7082dd8310ef11d32da652b5a236e38e0694c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70400363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fcd33d4e18fbeb4dabe3bf8ee2491831b3b22df3d892a20e66b4a1a25f9fe6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ef49ab95ed86f265e63020c4dd9d5abc15956a4345356b18cf392fd3d868d5`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 4.2 MB (4209296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f208c4d37a5af78456802ce8d9c75385fe4b071ae6fed79a6e50aa569c6447`  
		Last Modified: Tue, 23 Jul 2024 07:13:36 GMT  
		Size: 34.7 MB (34738355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d22cfd3b0c52905d3ef3986034366b23d428dae01577f399c2ddc759845438`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5051cc7cc549409c465d565b739b0b31327965121659369afa4ce218cdb121ec`  
		Last Modified: Tue, 23 Jul 2024 07:13:36 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2f89445218b7e0171e1c936cb6263e5e9d75d11939758a295a1e2605b337ef`  
		Last Modified: Tue, 23 Jul 2024 07:13:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:ff9ed27159bf5ee95765aa85217a17dd6ff318c91441668ff737f2394a7168b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8630087d2923114f28d8285ca8d3013b07487c766efec55d5fb1bcb2e3e0ce8`

```dockerfile
```

-	Layers:
	-	`sha256:4f3358c1be620718c02c052265a7129a696b2186f101c00f2fe99e9a3fe2edb8`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 2.9 MB (2893542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd3676ef043d0f3001782c5153bdac731d225f92be8c3475d928371ddf37be0`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2d760f9231102e41229b57c1c891474f12e3ea8f98319a51318c13ff81f9f7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256e9b5bdb781983f8599e873bca549b5bbfccd8a257209a0d85b3310b3fdc6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c0148be954c424420888ef600c5f9749f0cf70bc34b2e472d8bd0ccdd5900f`  
		Last Modified: Tue, 23 Jul 2024 11:56:36 GMT  
		Size: 3.5 MB (3511545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361bf0955a42eba99d2032b667d5299d8678139c8caf8388131090be112af124`  
		Last Modified: Tue, 23 Jul 2024 11:56:37 GMT  
		Size: 33.1 MB (33097392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5426960a9edaba574f1c37024c4b918b7e226ae4fcdb4718bb048bd1bab5eb9`  
		Last Modified: Tue, 23 Jul 2024 11:56:36 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4244b93faea4366aec0669156fdcbe4d63aef1daf6946265e094bf6e8261c933`  
		Last Modified: Tue, 23 Jul 2024 11:56:37 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314021ea4c8fbf9bd9451eedff51d1a0afed25094b6115989867815c8463e55`  
		Last Modified: Tue, 23 Jul 2024 11:56:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:b730dc669e00aa35a1737b1b5c680aa92e5f0eccb1fa27cc90bc17ebab3b2191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2911462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b3529a61e311157a2d52f1f7df866045e7ae1e2d27fd16cee10eaee25844e1`

```dockerfile
```

-	Layers:
	-	`sha256:67dba20b400a109ef5a3c164206e370dc1f8a04e7589909292c83947b69ec41a`  
		Last Modified: Tue, 23 Jul 2024 11:56:36 GMT  
		Size: 2.9 MB (2895812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b31da20ea30039ca964f34b267dfd0de090590eb43cbc3e88a4559e7f730a7`  
		Last Modified: Tue, 23 Jul 2024 11:56:36 GMT  
		Size: 15.7 KB (15650 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7e047e43f10e6265597ab5fe377934073ca979db6ef300d378a48a0b57583b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67548909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ddec0c310980e3767266f5dea167c80702d4797211f520e5f47da146e7ae9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c05c631b1b9331826c7db3cce5b27aeeaafd9a5d9e0fd3085723d0e968cc5c`  
		Last Modified: Tue, 23 Jul 2024 11:59:35 GMT  
		Size: 4.2 MB (4210551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934498212884f01884f79d6259ee2d2cc1d943030c02d34f558f31bf21295c91`  
		Last Modified: Tue, 23 Jul 2024 11:59:36 GMT  
		Size: 33.2 MB (33237879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a270e0dd3563f86c60b93ee4c38ed61ce32e673993555bb22a12be31452dff`  
		Last Modified: Tue, 23 Jul 2024 11:59:34 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2245139148fe62dadb0663ead804087639d88e17dab3f9e06c028f5fb1a2f338`  
		Last Modified: Tue, 23 Jul 2024 11:59:35 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bd05f452c16975220dbc2585c03ec071912da68d3a0ebfc5ddfc727bbf90e9`  
		Last Modified: Tue, 23 Jul 2024 11:59:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:6305ce5400c8fcb642a6ace26d5eff7c95393f9a2a09c423aeb4e348864fb30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce6ed50be52d939c1f8840e1b2a1a438af8629945756ba6b4c9b00c6db879e3`

```dockerfile
```

-	Layers:
	-	`sha256:0691cde7439d985e7caf4a189c7a0d1d63fa862028ef25a6cd8e1cbf16a3e09e`  
		Last Modified: Tue, 23 Jul 2024 11:59:35 GMT  
		Size: 2.9 MB (2893790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b654f8a2889353dbbe5729a28997e99180bbaa1299077f982f14d37514439b2`  
		Last Modified: Tue, 23 Jul 2024 11:59:34 GMT  
		Size: 15.9 KB (15867 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:e076570af40910c04efbba588f7e69fadc72997f6ffd18f573b083a5a3cd0c0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9c4a9e0fa4070786186ea4dd657975095b5a7c9b43d99daa9f149d4c93d86778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23495089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb3e8f98549c764cb30435669d0fe70e391cc6c763301074c4cf0cdc63f8b80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a458ecf643d4b38a9d0f5a8c542818186c774012314ec58a6bf203fd3d00611`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ee544247fdf24a9cfcadc3d2a2282d29da319e04d841a6cd7b1349a3a50a9a`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 290.9 KB (290877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966bf807ca8f8c02903c4573657e08918f2be7f9c43dcc98028f1f976eed0f8d`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 19.6 MB (19556675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f09c8af63d3d0b14737d53437c86578913bec994953020983954bb22ead0d63`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55608b4c7c5c813817fbd9110ca98c08ac9149d7b47ab46bc30a093e17b706e`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97760b26e0bb6da82f69f96432d997dfb983637c797de94fd70494b5ccf8f812`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:19e9252df9346f0db1ba5824a23c0fbaf4d0fbf77c435338c54eead471bd6f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 KB (187930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6d66c4da2363609efeabe7c0c6ae20d1ee4ab4e54bcbc019caaf9e31166bea`

```dockerfile
```

-	Layers:
	-	`sha256:31f108328416532d39a4056060f7684e879c7ea0e5f926b9fd2dbeaae36649c8`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 171.2 KB (171233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8f5427a928d36d75ae8c30f6bc99190ac1475da30b0bc8bfb62aa59b559a4f`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:97cc1001e2675eb674195421efc213e02a79c112a33773c52182b905091dcc75
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
$ docker pull chronograf@sha256:e5388fc7f8856e93bf58153cbca7082dd8310ef11d32da652b5a236e38e0694c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70400363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fcd33d4e18fbeb4dabe3bf8ee2491831b3b22df3d892a20e66b4a1a25f9fe6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ef49ab95ed86f265e63020c4dd9d5abc15956a4345356b18cf392fd3d868d5`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 4.2 MB (4209296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f208c4d37a5af78456802ce8d9c75385fe4b071ae6fed79a6e50aa569c6447`  
		Last Modified: Tue, 23 Jul 2024 07:13:36 GMT  
		Size: 34.7 MB (34738355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d22cfd3b0c52905d3ef3986034366b23d428dae01577f399c2ddc759845438`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5051cc7cc549409c465d565b739b0b31327965121659369afa4ce218cdb121ec`  
		Last Modified: Tue, 23 Jul 2024 07:13:36 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2f89445218b7e0171e1c936cb6263e5e9d75d11939758a295a1e2605b337ef`  
		Last Modified: Tue, 23 Jul 2024 07:13:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:ff9ed27159bf5ee95765aa85217a17dd6ff318c91441668ff737f2394a7168b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8630087d2923114f28d8285ca8d3013b07487c766efec55d5fb1bcb2e3e0ce8`

```dockerfile
```

-	Layers:
	-	`sha256:4f3358c1be620718c02c052265a7129a696b2186f101c00f2fe99e9a3fe2edb8`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 2.9 MB (2893542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd3676ef043d0f3001782c5153bdac731d225f92be8c3475d928371ddf37be0`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2d760f9231102e41229b57c1c891474f12e3ea8f98319a51318c13ff81f9f7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256e9b5bdb781983f8599e873bca549b5bbfccd8a257209a0d85b3310b3fdc6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c0148be954c424420888ef600c5f9749f0cf70bc34b2e472d8bd0ccdd5900f`  
		Last Modified: Tue, 23 Jul 2024 11:56:36 GMT  
		Size: 3.5 MB (3511545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361bf0955a42eba99d2032b667d5299d8678139c8caf8388131090be112af124`  
		Last Modified: Tue, 23 Jul 2024 11:56:37 GMT  
		Size: 33.1 MB (33097392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5426960a9edaba574f1c37024c4b918b7e226ae4fcdb4718bb048bd1bab5eb9`  
		Last Modified: Tue, 23 Jul 2024 11:56:36 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4244b93faea4366aec0669156fdcbe4d63aef1daf6946265e094bf6e8261c933`  
		Last Modified: Tue, 23 Jul 2024 11:56:37 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3314021ea4c8fbf9bd9451eedff51d1a0afed25094b6115989867815c8463e55`  
		Last Modified: Tue, 23 Jul 2024 11:56:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:b730dc669e00aa35a1737b1b5c680aa92e5f0eccb1fa27cc90bc17ebab3b2191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2911462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b3529a61e311157a2d52f1f7df866045e7ae1e2d27fd16cee10eaee25844e1`

```dockerfile
```

-	Layers:
	-	`sha256:67dba20b400a109ef5a3c164206e370dc1f8a04e7589909292c83947b69ec41a`  
		Last Modified: Tue, 23 Jul 2024 11:56:36 GMT  
		Size: 2.9 MB (2895812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b31da20ea30039ca964f34b267dfd0de090590eb43cbc3e88a4559e7f730a7`  
		Last Modified: Tue, 23 Jul 2024 11:56:36 GMT  
		Size: 15.7 KB (15650 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7e047e43f10e6265597ab5fe377934073ca979db6ef300d378a48a0b57583b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67548909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ddec0c310980e3767266f5dea167c80702d4797211f520e5f47da146e7ae9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c05c631b1b9331826c7db3cce5b27aeeaafd9a5d9e0fd3085723d0e968cc5c`  
		Last Modified: Tue, 23 Jul 2024 11:59:35 GMT  
		Size: 4.2 MB (4210551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934498212884f01884f79d6259ee2d2cc1d943030c02d34f558f31bf21295c91`  
		Last Modified: Tue, 23 Jul 2024 11:59:36 GMT  
		Size: 33.2 MB (33237879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a270e0dd3563f86c60b93ee4c38ed61ce32e673993555bb22a12be31452dff`  
		Last Modified: Tue, 23 Jul 2024 11:59:34 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2245139148fe62dadb0663ead804087639d88e17dab3f9e06c028f5fb1a2f338`  
		Last Modified: Tue, 23 Jul 2024 11:59:35 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bd05f452c16975220dbc2585c03ec071912da68d3a0ebfc5ddfc727bbf90e9`  
		Last Modified: Tue, 23 Jul 2024 11:59:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:6305ce5400c8fcb642a6ace26d5eff7c95393f9a2a09c423aeb4e348864fb30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce6ed50be52d939c1f8840e1b2a1a438af8629945756ba6b4c9b00c6db879e3`

```dockerfile
```

-	Layers:
	-	`sha256:0691cde7439d985e7caf4a189c7a0d1d63fa862028ef25a6cd8e1cbf16a3e09e`  
		Last Modified: Tue, 23 Jul 2024 11:59:35 GMT  
		Size: 2.9 MB (2893790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b654f8a2889353dbbe5729a28997e99180bbaa1299077f982f14d37514439b2`  
		Last Modified: Tue, 23 Jul 2024 11:59:34 GMT  
		Size: 15.9 KB (15867 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:e076570af40910c04efbba588f7e69fadc72997f6ffd18f573b083a5a3cd0c0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9c4a9e0fa4070786186ea4dd657975095b5a7c9b43d99daa9f149d4c93d86778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23495089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb3e8f98549c764cb30435669d0fe70e391cc6c763301074c4cf0cdc63f8b80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a458ecf643d4b38a9d0f5a8c542818186c774012314ec58a6bf203fd3d00611`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ee544247fdf24a9cfcadc3d2a2282d29da319e04d841a6cd7b1349a3a50a9a`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 290.9 KB (290877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966bf807ca8f8c02903c4573657e08918f2be7f9c43dcc98028f1f976eed0f8d`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 19.6 MB (19556675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f09c8af63d3d0b14737d53437c86578913bec994953020983954bb22ead0d63`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55608b4c7c5c813817fbd9110ca98c08ac9149d7b47ab46bc30a093e17b706e`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97760b26e0bb6da82f69f96432d997dfb983637c797de94fd70494b5ccf8f812`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:19e9252df9346f0db1ba5824a23c0fbaf4d0fbf77c435338c54eead471bd6f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 KB (187930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6d66c4da2363609efeabe7c0c6ae20d1ee4ab4e54bcbc019caaf9e31166bea`

```dockerfile
```

-	Layers:
	-	`sha256:31f108328416532d39a4056060f7684e879c7ea0e5f926b9fd2dbeaae36649c8`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 171.2 KB (171233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8f5427a928d36d75ae8c30f6bc99190ac1475da30b0bc8bfb62aa59b559a4f`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:207cbf3a15224b5fb0b7675b1379929ced4c5e964b88e3e39e9e86e4cc96927d
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
$ docker pull chronograf@sha256:8ca591ffa39f2b71a290bd909c288d62768f9cf6e7423489402c9ac86fa9be73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71041029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0ffcc9240da989bc066ee753e1b6f6494f13bde478748d0f09e46e7269a12e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5effecf7f5f81de21494b4bd6c25231c0afaab10a5b581d9efafc74bb6d6ace`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 5.2 MB (5224201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcd7febb7d02d8c55c58d416c30218cdd846f8a2704ee308e41edb7d1e7348b`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 34.4 MB (34364102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2f03c3d0524343c2bf797b0ace1e305840d0baba57a1e0d94fa15c85e7d1d`  
		Last Modified: Tue, 23 Jul 2024 07:13:34 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9560dcf2f6dd500fa7a7dbc966a1f39d3feadd569db8af1e2ebceda9439798c3`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc56fb3557d563e09ea0b1003ec76a6d3f2981f790106ab62621d60057cef93`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:353cafc1dac20f25d4290a361d4fc416ef1f2555a720a4759d48cfeabd91a171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ee1141a9497eaf337fd6dba1200119c218fd69459d7fe6efb43501855d2209`

```dockerfile
```

-	Layers:
	-	`sha256:a950b266642fe02f2fe7ec6bf5ce35c6ddbbbc016c02c18105eec6892a3b0263`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 2.9 MB (2949640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d7c4a3c3a96f7490e70fdc6fb50891c6dbf7885534cb0dd6b872c249473f1f`  
		Last Modified: Tue, 23 Jul 2024 07:13:34 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4275e7123188296c40161f093eb96d0d817a7888813b112575d783b7f4469f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63638305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30ad7824cfd51a53c5d91d231677c544a675590af49136bfa46e47d48c0245f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edac3d0276ac9d6ade31106514c5d64d96aacc1978a3f9bcbba2ebb37aa88cf1`  
		Last Modified: Tue, 23 Jul 2024 11:57:27 GMT  
		Size: 4.5 MB (4490062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2dabf9d934a3a67c4a19b662e253d44d88b21dd48b8a8399eac61758977bd7`  
		Last Modified: Tue, 23 Jul 2024 11:57:28 GMT  
		Size: 32.5 MB (32534716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684afc78ed771001c575cf0892118b59dca5c6fd69d823662685469ac8ef9776`  
		Last Modified: Tue, 23 Jul 2024 11:57:26 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a3756d58225898367825130079e8809b5342fa91f64c054804550f1845090`  
		Last Modified: Tue, 23 Jul 2024 11:57:26 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedf1667e68d043f35b22863c9cc84e23511477d6a4617db7eec534912a0c2e`  
		Last Modified: Tue, 23 Jul 2024 11:57:27 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:d392db8205dbb0db1d8b28391882719959909e14d5e1953c25f66d168a90659c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475dc6890b35720bb9d598463811b79afddef8c4dac233aab68bbd6308285e0b`

```dockerfile
```

-	Layers:
	-	`sha256:b2b808904106abfa8802a295197b2a3273dddc9a8467e7c9a758e599056a3ff4`  
		Last Modified: Tue, 23 Jul 2024 11:57:27 GMT  
		Size: 3.0 MB (2951910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280575eb35a2c5d38fa84b474dfbb5e7be795997ee0359ed84985c164b4106c7`  
		Last Modified: Tue, 23 Jul 2024 11:57:26 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:65a29ebdd7e3aefa3e1938475164cdf1e2b639c1ab646c540a78b6393b25cf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67738087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4657fd64fe6c43261f0f1b5198bab96d0820eb0048756b7bde38979009afbe1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f347046b5c74437a482b5713080e2d6cc4da816e2cdb5067edbd4620446f1f0`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 5.2 MB (5208102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d0e76b4206c4f759bcbe878aa5250f60afa75e2744cc0e982bea97e6cfbe5b`  
		Last Modified: Tue, 23 Jul 2024 12:00:10 GMT  
		Size: 32.4 MB (32429502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512fce2bd22e779a260e672f08c269bf4ef92f35e6f88c54a7fc3f5e3de82f3a`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3fdfd102aa825096cf75fa3acab8d39f73c7d06ecd591e8ed7453362405996`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3df21f7000ef469ae427abb1ed0a5a45735e2070d0d1e38f14e1c2a7325950`  
		Last Modified: Tue, 23 Jul 2024 12:00:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:b82d83a32b40af05e88418d9447752a025dc49b846a183f944dca6738e31c810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b961fb51f68d2bd99c6dfb6278350204607fedc141148d7a7b6eede01b8e69f4`

```dockerfile
```

-	Layers:
	-	`sha256:c9c4a111f79c9c8cf9f3fc9b6c12a34625a03d7975df0f50d99bea3fd4fb7c1a`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 2.9 MB (2949888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36c5e04b357b43019ac42b75b9f70c9fed9905a6c8ba69baf17b1f5e8e52c59`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:84636f9de5bd20bd74a0e53a63d3ca2eb601f7fd9ffe1e064698881c271a0f47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b41f511f95cba62df1a7b8d1eff43097ecd52773576bde144be38804c605b0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23142481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7252dc2f7f31b46df25bdf463a51f6910ae30bdeceaf6700fc6e443127e40d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2135683639d6f1ac29f32353435e0c9f71502450d8efe82cc50570a76a309`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1732046335dccd437c12b1d58356d25e6add8b61ef68da210262efc74c90e2ca`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 290.9 KB (290876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb871ce98c9a9bfc7d1e14e8eb80733cb3bec1c2ab533e8cf7671515c635670`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 19.2 MB (19204052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022c6486f232f3fe2c159c6e71907f5225bfef243c3e5fe83cdc44b304e1f54b`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2f5ed72c42736195ab9ae1e0735af61365cfd87b7915f52199f06da9f2059d`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2a1c4a2512bb98c33670490243e1fa71eb88b46b5d4949df73c3dd4f06d22`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:24dfc0e1109ea89bc6cf799749fd90fdd2537b6204cc671979a2a70576fdb081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 KB (244689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d1fb878be116591237463229b2ee139489e0c6da84b3105d62b62bfdef9ebd`

```dockerfile
```

-	Layers:
	-	`sha256:c28864f6601cb5284a624f63c2fbec85d77b38da889f27eeee3f88ef0861538f`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 228.0 KB (227992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9593c9c9e0043991569cb67339498b0a4308662d9857a89487862580d07257f2`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:207cbf3a15224b5fb0b7675b1379929ced4c5e964b88e3e39e9e86e4cc96927d
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
$ docker pull chronograf@sha256:8ca591ffa39f2b71a290bd909c288d62768f9cf6e7423489402c9ac86fa9be73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71041029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0ffcc9240da989bc066ee753e1b6f6494f13bde478748d0f09e46e7269a12e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5effecf7f5f81de21494b4bd6c25231c0afaab10a5b581d9efafc74bb6d6ace`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 5.2 MB (5224201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcd7febb7d02d8c55c58d416c30218cdd846f8a2704ee308e41edb7d1e7348b`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 34.4 MB (34364102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2f03c3d0524343c2bf797b0ace1e305840d0baba57a1e0d94fa15c85e7d1d`  
		Last Modified: Tue, 23 Jul 2024 07:13:34 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9560dcf2f6dd500fa7a7dbc966a1f39d3feadd569db8af1e2ebceda9439798c3`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc56fb3557d563e09ea0b1003ec76a6d3f2981f790106ab62621d60057cef93`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:353cafc1dac20f25d4290a361d4fc416ef1f2555a720a4759d48cfeabd91a171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ee1141a9497eaf337fd6dba1200119c218fd69459d7fe6efb43501855d2209`

```dockerfile
```

-	Layers:
	-	`sha256:a950b266642fe02f2fe7ec6bf5ce35c6ddbbbc016c02c18105eec6892a3b0263`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 2.9 MB (2949640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d7c4a3c3a96f7490e70fdc6fb50891c6dbf7885534cb0dd6b872c249473f1f`  
		Last Modified: Tue, 23 Jul 2024 07:13:34 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4275e7123188296c40161f093eb96d0d817a7888813b112575d783b7f4469f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63638305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30ad7824cfd51a53c5d91d231677c544a675590af49136bfa46e47d48c0245f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edac3d0276ac9d6ade31106514c5d64d96aacc1978a3f9bcbba2ebb37aa88cf1`  
		Last Modified: Tue, 23 Jul 2024 11:57:27 GMT  
		Size: 4.5 MB (4490062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2dabf9d934a3a67c4a19b662e253d44d88b21dd48b8a8399eac61758977bd7`  
		Last Modified: Tue, 23 Jul 2024 11:57:28 GMT  
		Size: 32.5 MB (32534716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684afc78ed771001c575cf0892118b59dca5c6fd69d823662685469ac8ef9776`  
		Last Modified: Tue, 23 Jul 2024 11:57:26 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a3756d58225898367825130079e8809b5342fa91f64c054804550f1845090`  
		Last Modified: Tue, 23 Jul 2024 11:57:26 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bedf1667e68d043f35b22863c9cc84e23511477d6a4617db7eec534912a0c2e`  
		Last Modified: Tue, 23 Jul 2024 11:57:27 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d392db8205dbb0db1d8b28391882719959909e14d5e1953c25f66d168a90659c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475dc6890b35720bb9d598463811b79afddef8c4dac233aab68bbd6308285e0b`

```dockerfile
```

-	Layers:
	-	`sha256:b2b808904106abfa8802a295197b2a3273dddc9a8467e7c9a758e599056a3ff4`  
		Last Modified: Tue, 23 Jul 2024 11:57:27 GMT  
		Size: 3.0 MB (2951910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280575eb35a2c5d38fa84b474dfbb5e7be795997ee0359ed84985c164b4106c7`  
		Last Modified: Tue, 23 Jul 2024 11:57:26 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:65a29ebdd7e3aefa3e1938475164cdf1e2b639c1ab646c540a78b6393b25cf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67738087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4657fd64fe6c43261f0f1b5198bab96d0820eb0048756b7bde38979009afbe1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f347046b5c74437a482b5713080e2d6cc4da816e2cdb5067edbd4620446f1f0`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 5.2 MB (5208102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d0e76b4206c4f759bcbe878aa5250f60afa75e2744cc0e982bea97e6cfbe5b`  
		Last Modified: Tue, 23 Jul 2024 12:00:10 GMT  
		Size: 32.4 MB (32429502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512fce2bd22e779a260e672f08c269bf4ef92f35e6f88c54a7fc3f5e3de82f3a`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3fdfd102aa825096cf75fa3acab8d39f73c7d06ecd591e8ed7453362405996`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3df21f7000ef469ae427abb1ed0a5a45735e2070d0d1e38f14e1c2a7325950`  
		Last Modified: Tue, 23 Jul 2024 12:00:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:b82d83a32b40af05e88418d9447752a025dc49b846a183f944dca6738e31c810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b961fb51f68d2bd99c6dfb6278350204607fedc141148d7a7b6eede01b8e69f4`

```dockerfile
```

-	Layers:
	-	`sha256:c9c4a111f79c9c8cf9f3fc9b6c12a34625a03d7975df0f50d99bea3fd4fb7c1a`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 2.9 MB (2949888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36c5e04b357b43019ac42b75b9f70c9fed9905a6c8ba69baf17b1f5e8e52c59`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:84636f9de5bd20bd74a0e53a63d3ca2eb601f7fd9ffe1e064698881c271a0f47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b41f511f95cba62df1a7b8d1eff43097ecd52773576bde144be38804c605b0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23142481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7252dc2f7f31b46df25bdf463a51f6910ae30bdeceaf6700fc6e443127e40d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2135683639d6f1ac29f32353435e0c9f71502450d8efe82cc50570a76a309`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1732046335dccd437c12b1d58356d25e6add8b61ef68da210262efc74c90e2ca`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 290.9 KB (290876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb871ce98c9a9bfc7d1e14e8eb80733cb3bec1c2ab533e8cf7671515c635670`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 19.2 MB (19204052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022c6486f232f3fe2c159c6e71907f5225bfef243c3e5fe83cdc44b304e1f54b`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2f5ed72c42736195ab9ae1e0735af61365cfd87b7915f52199f06da9f2059d`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2a1c4a2512bb98c33670490243e1fa71eb88b46b5d4949df73c3dd4f06d22`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:24dfc0e1109ea89bc6cf799749fd90fdd2537b6204cc671979a2a70576fdb081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 KB (244689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d1fb878be116591237463229b2ee139489e0c6da84b3105d62b62bfdef9ebd`

```dockerfile
```

-	Layers:
	-	`sha256:c28864f6601cb5284a624f63c2fbec85d77b38da889f27eeee3f88ef0861538f`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 228.0 KB (227992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9593c9c9e0043991569cb67339498b0a4308662d9857a89487862580d07257f2`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:e241cef4287f5dd99eff52925b7c738d55f2f06dc2f0037de73a2cb79f4dd5ac
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
$ docker pull chronograf@sha256:0726897d97837bb75fef99a80c997dea5c10aea934ccb87e59d2f917fcace061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71688508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345c21b4fd51f01f9e4932250c0d6485ffff4ee9949c43b8ded69c9e5c1c4957`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed50889e88bf7f179e8479cfc178fad75984cbae5b2de99d7fc2d88dfe2eeb5`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 5.2 MB (5224231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a40dfbe4696b53c05dd3a865b2d7d1e193670d2a71e02a160182e066e425a8`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 35.0 MB (35011563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba0c1b13052bf02b1293c5f73488ec8d100076105988ebe5934a7cbf466949c`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e6bca57b8841e1f1f6af6f57d5ba1cb7a832b433821556d7282cc7fe51636c`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc56fb3557d563e09ea0b1003ec76a6d3f2981f790106ab62621d60057cef93`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:97047d1430bbf0817bb2998dbae05dd60ff7fd3b9716a012a51b05e11fe1812a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbab2b9e922ea4e6bcd3e45c89f0d91a2c3a22d0cc8bbc9683fbe0c6137c55`

```dockerfile
```

-	Layers:
	-	`sha256:cb8dbe82e5939ec98e82506fafe7f13793575bd83ee8fe3c9d646fdd0fc16ff6`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 3.0 MB (2954790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c96fc5b3a84ee69bfd92f8f72c72000542d616558da50be580ff15fecedec7`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 15.6 KB (15616 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f3bcfe8e271b1331ee772d2c30c4a31dd1fc9f4d813b7a6d26885494d44e5d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64414921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeedec8e730eab4f307008abc9b8382636fb99dc56033184dc35ee57d16b3366`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edac3d0276ac9d6ade31106514c5d64d96aacc1978a3f9bcbba2ebb37aa88cf1`  
		Last Modified: Tue, 23 Jul 2024 11:57:27 GMT  
		Size: 4.5 MB (4490062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24b1373d3aa3a44222f1fb835ee6fae5801db7830101b4d505044d76ac60c4`  
		Last Modified: Tue, 23 Jul 2024 11:58:05 GMT  
		Size: 33.3 MB (33311330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea38efbe5fb3f35e9edf70a5a30872528911c832a34265ad4e1481c6403c366f`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f1a4ff82d73c67e073d667597f0d9f4a0939372dd771cddb145b26293e03c`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a2690af97e0dfd2c29ac54f0990857413909966989e55a3a60595346f4c3a0`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:65e87a371d6c487773862cb5fb301384bb1bb1c509b5592a520f393510968577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9631b5f3464c31278c6f6c0aafa6386737d32886cb78b5ccb7288d77de94a8a5`

```dockerfile
```

-	Layers:
	-	`sha256:713468c9149344adc7cadb24c9530de9f2fb832ca8b3601d40de47784ba0d665`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 3.0 MB (2957060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe96e6a0d400257e4b0f5e9ab34166f3f6dc18422d32a2a28a6fe1b6ec68fa7f`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 15.7 KB (15682 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:feec9687f6023dc922acf9ae61c1a9fd34437982de15ac3fb46ac7bf3483bbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68490091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52179b16a80461dd83f840aa0dc901b36ba3968ecd17bbe0edfa139a369c5a7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f347046b5c74437a482b5713080e2d6cc4da816e2cdb5067edbd4620446f1f0`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 5.2 MB (5208102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e21b73d670a54b4cb80e36064ada7c609573adb3438015fd9a86f8f1f2e23e`  
		Last Modified: Tue, 23 Jul 2024 12:00:38 GMT  
		Size: 33.2 MB (33181507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6b274456e298642783419324049111d67a0faee0313869912a37aaac37f2ef`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b16cb741b6b539739374480b29f231bfb396ff1c93e6e07509dc39ff523a70b`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8367243c918d52ff324291d1e1bd252d7dd3402b6fd8bd187e0d452bb7a34c5f`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:aed0552382e9c97e490056b8ba2ca9bf227a0248990b4bf706930e7743bb5e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0522fd11b97cc85006d9d813bc8f23fefd1086fbe70907080af3bff235c95aa`

```dockerfile
```

-	Layers:
	-	`sha256:9d11a2227e142a549aa7459b579b8addcfbbbe13a8c9be5c2d38ba045de36f2c`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 3.0 MB (2955038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310f352b01d558a8cc86fb36cf6f4d6398297948df08ce972d40e8e67c7275e7`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:30d4c22f1bdcaa419e3bfc304bc5fc6477c2cc0fc847b7308a11b6723e77d297
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:972452f512ec59acfcdb335b8da0921d1e4d4119bfaed4b6f292490c06ba651d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23610495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a24b20930e6f092cf0f0d8be254eed7059519c47dc305c0b3d848b4cbb7529`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cbc68499bebfe1f81d8a584c2290268f7365b28c23da5a3860d0729d59983`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e78acb78a04f3ae804af66169259d77bd32d13af803eff651bd37596d91231`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 290.9 KB (290878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf1a38691cdeff82091527a2135e760756e7039a38896be0f636670532a7512`  
		Last Modified: Mon, 22 Jul 2024 23:03:16 GMT  
		Size: 19.7 MB (19672079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a187f5518cd7aafa59ed25d443f855ad1851a82e0dcbed7ce1cc213582c31a6c`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0848f0932c3c202a603d894c63722653db8712e2fc4725c3f5fa6b3f1b2ff583`  
		Last Modified: Mon, 22 Jul 2024 23:03:16 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586248d439ca4aedc9c4d7211a22efeab78949d7334bd48f8de407e9438c937b`  
		Last Modified: Mon, 22 Jul 2024 23:03:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:da223938c0e1ceec8ecec30dbe404b78d94c781155484bf3e560301cc3948145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 KB (249837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c37ec97241809ed56681829e4096bcdb84c6a35a34bb2a5c72dc46d6f68194`

```dockerfile
```

-	Layers:
	-	`sha256:d31f61614b789009b94376ca8ade08b9b0fdce5664da572017c46730f30d2037`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 233.1 KB (233144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86014d5c9da161b79a46726b391786e84f53a9dbd3faf97e49e7509d67fdb2b8`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:e241cef4287f5dd99eff52925b7c738d55f2f06dc2f0037de73a2cb79f4dd5ac
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
$ docker pull chronograf@sha256:0726897d97837bb75fef99a80c997dea5c10aea934ccb87e59d2f917fcace061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71688508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345c21b4fd51f01f9e4932250c0d6485ffff4ee9949c43b8ded69c9e5c1c4957`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed50889e88bf7f179e8479cfc178fad75984cbae5b2de99d7fc2d88dfe2eeb5`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 5.2 MB (5224231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a40dfbe4696b53c05dd3a865b2d7d1e193670d2a71e02a160182e066e425a8`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 35.0 MB (35011563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba0c1b13052bf02b1293c5f73488ec8d100076105988ebe5934a7cbf466949c`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e6bca57b8841e1f1f6af6f57d5ba1cb7a832b433821556d7282cc7fe51636c`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc56fb3557d563e09ea0b1003ec76a6d3f2981f790106ab62621d60057cef93`  
		Last Modified: Tue, 23 Jul 2024 07:13:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:97047d1430bbf0817bb2998dbae05dd60ff7fd3b9716a012a51b05e11fe1812a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dbab2b9e922ea4e6bcd3e45c89f0d91a2c3a22d0cc8bbc9683fbe0c6137c55`

```dockerfile
```

-	Layers:
	-	`sha256:cb8dbe82e5939ec98e82506fafe7f13793575bd83ee8fe3c9d646fdd0fc16ff6`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 3.0 MB (2954790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c96fc5b3a84ee69bfd92f8f72c72000542d616558da50be580ff15fecedec7`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 15.6 KB (15616 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f3bcfe8e271b1331ee772d2c30c4a31dd1fc9f4d813b7a6d26885494d44e5d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64414921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeedec8e730eab4f307008abc9b8382636fb99dc56033184dc35ee57d16b3366`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
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
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edac3d0276ac9d6ade31106514c5d64d96aacc1978a3f9bcbba2ebb37aa88cf1`  
		Last Modified: Tue, 23 Jul 2024 11:57:27 GMT  
		Size: 4.5 MB (4490062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24b1373d3aa3a44222f1fb835ee6fae5801db7830101b4d505044d76ac60c4`  
		Last Modified: Tue, 23 Jul 2024 11:58:05 GMT  
		Size: 33.3 MB (33311330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea38efbe5fb3f35e9edf70a5a30872528911c832a34265ad4e1481c6403c366f`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f1a4ff82d73c67e073d667597f0d9f4a0939372dd771cddb145b26293e03c`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a2690af97e0dfd2c29ac54f0990857413909966989e55a3a60595346f4c3a0`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:65e87a371d6c487773862cb5fb301384bb1bb1c509b5592a520f393510968577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9631b5f3464c31278c6f6c0aafa6386737d32886cb78b5ccb7288d77de94a8a5`

```dockerfile
```

-	Layers:
	-	`sha256:713468c9149344adc7cadb24c9530de9f2fb832ca8b3601d40de47784ba0d665`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 3.0 MB (2957060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe96e6a0d400257e4b0f5e9ab34166f3f6dc18422d32a2a28a6fe1b6ec68fa7f`  
		Last Modified: Tue, 23 Jul 2024 11:58:04 GMT  
		Size: 15.7 KB (15682 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:feec9687f6023dc922acf9ae61c1a9fd34437982de15ac3fb46ac7bf3483bbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68490091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52179b16a80461dd83f840aa0dc901b36ba3968ecd17bbe0edfa139a369c5a7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f347046b5c74437a482b5713080e2d6cc4da816e2cdb5067edbd4620446f1f0`  
		Last Modified: Tue, 23 Jul 2024 12:00:09 GMT  
		Size: 5.2 MB (5208102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e21b73d670a54b4cb80e36064ada7c609573adb3438015fd9a86f8f1f2e23e`  
		Last Modified: Tue, 23 Jul 2024 12:00:38 GMT  
		Size: 33.2 MB (33181507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6b274456e298642783419324049111d67a0faee0313869912a37aaac37f2ef`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b16cb741b6b539739374480b29f231bfb396ff1c93e6e07509dc39ff523a70b`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8367243c918d52ff324291d1e1bd252d7dd3402b6fd8bd187e0d452bb7a34c5f`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:aed0552382e9c97e490056b8ba2ca9bf227a0248990b4bf706930e7743bb5e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0522fd11b97cc85006d9d813bc8f23fefd1086fbe70907080af3bff235c95aa`

```dockerfile
```

-	Layers:
	-	`sha256:9d11a2227e142a549aa7459b579b8addcfbbbe13a8c9be5c2d38ba045de36f2c`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 3.0 MB (2955038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310f352b01d558a8cc86fb36cf6f4d6398297948df08ce972d40e8e67c7275e7`  
		Last Modified: Tue, 23 Jul 2024 12:00:37 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:30d4c22f1bdcaa419e3bfc304bc5fc6477c2cc0fc847b7308a11b6723e77d297
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:972452f512ec59acfcdb335b8da0921d1e4d4119bfaed4b6f292490c06ba651d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23610495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a24b20930e6f092cf0f0d8be254eed7059519c47dc305c0b3d848b4cbb7529`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434cbc68499bebfe1f81d8a584c2290268f7365b28c23da5a3860d0729d59983`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e78acb78a04f3ae804af66169259d77bd32d13af803eff651bd37596d91231`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 290.9 KB (290878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf1a38691cdeff82091527a2135e760756e7039a38896be0f636670532a7512`  
		Last Modified: Mon, 22 Jul 2024 23:03:16 GMT  
		Size: 19.7 MB (19672079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a187f5518cd7aafa59ed25d443f855ad1851a82e0dcbed7ce1cc213582c31a6c`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0848f0932c3c202a603d894c63722653db8712e2fc4725c3f5fa6b3f1b2ff583`  
		Last Modified: Mon, 22 Jul 2024 23:03:16 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586248d439ca4aedc9c4d7211a22efeab78949d7334bd48f8de407e9438c937b`  
		Last Modified: Mon, 22 Jul 2024 23:03:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:da223938c0e1ceec8ecec30dbe404b78d94c781155484bf3e560301cc3948145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 KB (249837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c37ec97241809ed56681829e4096bcdb84c6a35a34bb2a5c72dc46d6f68194`

```dockerfile
```

-	Layers:
	-	`sha256:d31f61614b789009b94376ca8ade08b9b0fdce5664da572017c46730f30d2037`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 233.1 KB (233144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86014d5c9da161b79a46726b391786e84f53a9dbd3faf97e49e7509d67fdb2b8`  
		Last Modified: Mon, 22 Jul 2024 23:03:15 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:bda6f3cb67284c0da5c9011100201d870ac597821831c340fc1dfc0d314766a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2901c06ba0aa8e1ca321512279411eae4fcc4cd07d1cdd2c9381c46fd51de58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31806919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1e35742a524fbb3a01981ea10844eb8ae62ef954762a43772bcb695a2f9d68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0558a15ffd5fd7dc1a320904adf4538b87b67a939d5d006b98a9b36017947502`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da05f34e03c0428cf96e2e8e8754fecd048b4672e1675c8dfd091987120152`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 292.6 KB (292596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1f4131f7e5257e9bc0a1099c0b2f6bced312d6e6f67a5aacc49361fc2c644`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 27.9 MB (27866731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fe17f4dd5d6655838dc7645cfdc88d3d95367154f129fe3d96acac7ee78a03`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c01279850cada9d2f470c39fdb304fc4ce71db414de5c5711c4bf17239418f`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacddbfa4fec719daff43f784bec28523cd8ee4fcc4786ce979c93515cadf4ed`  
		Last Modified: Mon, 22 Jul 2024 23:03:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6529e5937f5575e4cfb5f64c28d37ad905a0661f7072532e29e5ad2854533e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 KB (257227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ed52c6d0f8dbb2cbd26f76933a42d8893154547aa43e6e3b1189777362aae3`

```dockerfile
```

-	Layers:
	-	`sha256:2b633ff9323f7d9bf699a774058c48c851bf8eca1471aba989ded877d8c6b88d`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 239.6 KB (239587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c025800fabbad37f8d0a4823f2cd8491208afe5abbb959cf08ed7afa251e434`  
		Last Modified: Mon, 22 Jul 2024 23:03:13 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:b0ae594f24c582852736f2030bf0f0c0e606fc9cfc4ae9abad9c8e9d73d242ad
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
$ docker pull chronograf@sha256:153a02a215aaa8961d19beda4981b50a1e5cd136ac706d1fc8c5b9641b56ebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84239561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aeaf681ced1b72825e4f1ea24e8ca4eb6186b32e21b84ef885ae64f4987f01b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1d932a0ae4fdac27b3d3763ea9c42fbaa86dd7c24d4d5219d1abe974862e8`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 7.9 MB (7871459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d41db8d398ef2de7c4620f217b1c37524af4c25cec52653ec55c18914493eb9`  
		Last Modified: Tue, 23 Jul 2024 07:13:40 GMT  
		Size: 47.2 MB (47217352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae19e153971ef49a3da0003f8b6e6ec2bb5dc1435c3967c9a0a6436b922f62`  
		Last Modified: Tue, 23 Jul 2024 07:13:37 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16db583eb504f5d3efeda6a5d49fb5a24e96504e7094a6a533901af06d5a386`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773892334f3852b1fc38a2c88d95dbf20614ea9379fbb88b286feebb62fd3a0`  
		Last Modified: Tue, 23 Jul 2024 07:13:39 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5f6fe6f20c6467aad2452498eb3fda01eda0ca9ed4d37ff84e39b0723bdbac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad5d155c937d2270cab7ac97116aaf5f6cc25c66c0d3e4e4184ca1fe3feb8d`

```dockerfile
```

-	Layers:
	-	`sha256:7f57cc014e3606b8332ceb8b0fd7730433284ac470e57d7479f939a33ab99fd4`  
		Last Modified: Tue, 23 Jul 2024 07:13:38 GMT  
		Size: 2.7 MB (2690949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c214efb73472ebcb8fe23c68e09f034c40b367e852eb592742c9dbae868cf64b`  
		Last Modified: Tue, 23 Jul 2024 07:13:37 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1a1925253a4af6b859760bfc65ea234be4fa7ed68788ba95cfd59e355f75ece7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75514726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124223ba49bd9c978dfd626d0ec5c9bd4a4dc2b2e2308b79a14e6b1b68692996`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
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
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5263b97046c18ec1cc9eed5f67597f161262db97ff87e0a1c9e1ac3991819094`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 6.5 MB (6495958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e255b5aa2e3d8552515670a3387bdb0ee916433eca1005ef3243027f6a472151`  
		Last Modified: Tue, 23 Jul 2024 11:59:05 GMT  
		Size: 44.3 MB (44276098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5134aee981e8f0f8a23da3cdd01a18deab37c4da521c23f6d707cbc87e7d12b`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd13a3c43a4e3a18af3ad90b1b11596d67a6819e3f01eb1276d6ca0b326c801`  
		Last Modified: Tue, 23 Jul 2024 11:59:05 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cba087ac927520c3d3e4df8d1834088d770890e6216b847a8cde21c288661c`  
		Last Modified: Tue, 23 Jul 2024 11:59:05 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d5fe9141952828d92418ed319d71d9283e715d9be23eb23c93e2988fa8152c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1367b14f917b079b093810d72cb8dcf9f614642a19c713218a8c8f9a6ed52064`

```dockerfile
```

-	Layers:
	-	`sha256:a4cc31fbf6e9f89859fe236515ba0d01a3833903385c0ec41235f45cf5701b38`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 2.7 MB (2693245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92720a9583d26aa8d4f17c73aaa8128ebda7bbd47316561a16f9133cb584d151`  
		Last Modified: Tue, 23 Jul 2024 11:59:04 GMT  
		Size: 16.0 KB (16008 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a3e74028deff6e8e750d6aa10c72b4d4ff6d577038dce48df6f9009d2f84552e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81800653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e7bffceb49651ea4c8eec41dbd854083d633a69611f8954dc37a61fee377c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc8462b74326e175d556882ef423e4edaaa2ddd6578a0c551e50a500f1012aa`  
		Last Modified: Tue, 23 Jul 2024 12:01:21 GMT  
		Size: 7.6 MB (7649266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c445e41bd816107ae6464a7bc0c85a212f7ae11185771e90913b3b4072c6250`  
		Last Modified: Tue, 23 Jul 2024 12:01:22 GMT  
		Size: 45.0 MB (44970354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e58fcfff7ad0a484da120de538f623575d2da0dbe423d1d046e4ef8ed22722`  
		Last Modified: Tue, 23 Jul 2024 12:01:20 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79818630a46556198aa1441833c8c128c48a838c9339c945a3215d839994d090`  
		Last Modified: Tue, 23 Jul 2024 12:01:20 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f81446c3eac6af221d2244531848ac90e7d7ecf22daccce78a27a9eca07c32`  
		Last Modified: Tue, 23 Jul 2024 12:01:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:58b03acf392a1c6532ffb666bf95feeb6e7adc826df9dec0de0abad573a27902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfec816f07ed8726ec44850bae2c50a29fd8493ab18df9681f99e175ff3eb102`

```dockerfile
```

-	Layers:
	-	`sha256:2380ee8e1620b0de38df95a336e5fd0df31bee359c0829d0b090142bcfad375d`  
		Last Modified: Tue, 23 Jul 2024 12:01:21 GMT  
		Size: 2.7 MB (2691221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d146b7e8f243ee30705f182c43db7088ba5ad1b70989fd726127c9abc058e2`  
		Last Modified: Tue, 23 Jul 2024 12:01:20 GMT  
		Size: 16.2 KB (16231 bytes)  
		MIME: application/vnd.in-toto+json
