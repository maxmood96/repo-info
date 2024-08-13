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
$ docker pull chronograf@sha256:7501ef406fe9cb5edd43c702abe4de2a399ada7af5db4930c2966b8389eba7d9
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
$ docker pull chronograf@sha256:7103a0bb3d05646aac948fded55ac5201a5dc034df0aea97a3e9a497efaba292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84239467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257d3e20f92a7d73776d501432bd55abbd7e5164af3752fc8a081997f3909d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a769aefe23aebedcc5633ec6f52ebe4f5aa8eb5e942fb6ca9909454f3c5db7f4`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 7.9 MB (7871448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb49135b5a2b70e24894ece5df348bc1a45b19deb65faf4f99a30bbc92c65c8b`  
		Last Modified: Tue, 13 Aug 2024 01:11:04 GMT  
		Size: 47.2 MB (47217317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f6e528c458b87aa12af4f246a3929e0b8a17601531416271de9963650eb175`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b351d1b71edfa42cc9ddbf889b7b08d51afdba224a131837a2613690e255bc90`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30089f8784c53073e232ca2754a37eb5bfdc1e99a4c21b0b2a8303f4fd7b1ea2`  
		Last Modified: Tue, 13 Aug 2024 01:11:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:a50f53cfbec4cd00eca332ec9faab269a575a00fbd18818d189f88c076b38e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1004bd7be2d69aec9e0a3a5beedd32f3d874967b4614667db44cc32bc9fb8e8`

```dockerfile
```

-	Layers:
	-	`sha256:a577157f8d99c2f5526035aea9fcb37666a4e74dd74eb58292711f05f93839bc`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 2.7 MB (2690947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15565333f9c38d7a0464b70ad77a25b8c8c5e7b89c3976379a852393d75e3d06`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:39319375770d59f58ba8f8cf452889082a3fe121ef1678a4b0b9d088408f317a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75514585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b275637aa1c6b1edbe24465e3a37c48bbc4e2a1de237585d38c67c2bbb2acc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
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
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e8801ac7c9368437cbe587ff1aad7e371dd42bdd6f04c05928a914df092f1`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 6.5 MB (6495882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca6877c9cb8387a29111e067ff33053781c94cfb57f5e0c6080b2a4bb8a2ac2`  
		Last Modified: Tue, 13 Aug 2024 06:14:33 GMT  
		Size: 44.3 MB (44276093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf074a2d2ee71fc778577394598994ba79defcfebcf8234714bb4403b9beff71`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2eff715fc140f8d8673333b8b3aab68990ba7d103400a9ed714554174df64f`  
		Last Modified: Tue, 13 Aug 2024 06:14:33 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c612dfb3807513faf229144dad75f2bb5af9caa5ff171426664c4d066e5de`  
		Last Modified: Tue, 13 Aug 2024 06:14:33 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d6bd28a190c6284da0493f4bf5fa1eb8436b144ba0d225566d48ae1eabf69698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e127ca5f80ddb8faab9a53351caec5483836a4a6738c368717b7f46e0030d979`

```dockerfile
```

-	Layers:
	-	`sha256:14ebf33d780e54d524ec0a4908348ea4474d4accab3dc3ad65b3e00406692a31`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 2.7 MB (2693243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5cfcf687e51c4a3124d5bd766fe1c3223794717b0e762523e87079e60613b6`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8306fc57783667796d04956a0bc9824e5519cdc86e79404c52f451cadc33f515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81800593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3536354914de845fb9e6d00f012373ae54397a015642b573264b25a8550b88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b117a832b332535ec3b83dd4ded35fc32749ddc63215f1f9833a5c935b07c949`  
		Last Modified: Tue, 13 Aug 2024 06:13:19 GMT  
		Size: 7.6 MB (7649263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be30bd17377c5a726f876fd22fffb7968096a80be7bfca26c99ec53b524bada`  
		Last Modified: Tue, 13 Aug 2024 06:13:20 GMT  
		Size: 45.0 MB (44970331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc38e7253a66c453288470d2eeb66250ac8924124680f7c439e1fab10d84a1`  
		Last Modified: Tue, 13 Aug 2024 06:13:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e92d47cf4e44a4f24e075c908bd9ac7c41897e6f8f9a293d9b156a57e3e3a7`  
		Last Modified: Tue, 13 Aug 2024 06:13:19 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fe3e644c2ff8d6e442d809b70add3b01aae6ec1777836f0a2e651281b301db`  
		Last Modified: Tue, 13 Aug 2024 06:13:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:88687fdcc1eefed32ab2275cc83992f5a64c85187a4ea20f7d27bd99e6c1813f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe0aea431654dea6f946f5c5fe4112e3be07021c6fb56189d65276b85241406`

```dockerfile
```

-	Layers:
	-	`sha256:678d7c4634f51f7383dba93c13f2e6f0585bb1ece7dcc1de576de512a492a910`  
		Last Modified: Tue, 13 Aug 2024 06:13:18 GMT  
		Size: 2.7 MB (2691219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d54af3efccd2dba33916dc3fa3e8cfde425809f2ff3ea9d46dff8d7508855e`  
		Last Modified: Tue, 13 Aug 2024 06:13:18 GMT  
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
$ docker pull chronograf@sha256:7501ef406fe9cb5edd43c702abe4de2a399ada7af5db4930c2966b8389eba7d9
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
$ docker pull chronograf@sha256:7103a0bb3d05646aac948fded55ac5201a5dc034df0aea97a3e9a497efaba292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84239467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257d3e20f92a7d73776d501432bd55abbd7e5164af3752fc8a081997f3909d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a769aefe23aebedcc5633ec6f52ebe4f5aa8eb5e942fb6ca9909454f3c5db7f4`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 7.9 MB (7871448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb49135b5a2b70e24894ece5df348bc1a45b19deb65faf4f99a30bbc92c65c8b`  
		Last Modified: Tue, 13 Aug 2024 01:11:04 GMT  
		Size: 47.2 MB (47217317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f6e528c458b87aa12af4f246a3929e0b8a17601531416271de9963650eb175`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b351d1b71edfa42cc9ddbf889b7b08d51afdba224a131837a2613690e255bc90`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30089f8784c53073e232ca2754a37eb5bfdc1e99a4c21b0b2a8303f4fd7b1ea2`  
		Last Modified: Tue, 13 Aug 2024 01:11:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:a50f53cfbec4cd00eca332ec9faab269a575a00fbd18818d189f88c076b38e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1004bd7be2d69aec9e0a3a5beedd32f3d874967b4614667db44cc32bc9fb8e8`

```dockerfile
```

-	Layers:
	-	`sha256:a577157f8d99c2f5526035aea9fcb37666a4e74dd74eb58292711f05f93839bc`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 2.7 MB (2690947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15565333f9c38d7a0464b70ad77a25b8c8c5e7b89c3976379a852393d75e3d06`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:39319375770d59f58ba8f8cf452889082a3fe121ef1678a4b0b9d088408f317a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75514585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b275637aa1c6b1edbe24465e3a37c48bbc4e2a1de237585d38c67c2bbb2acc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
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
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e8801ac7c9368437cbe587ff1aad7e371dd42bdd6f04c05928a914df092f1`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 6.5 MB (6495882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca6877c9cb8387a29111e067ff33053781c94cfb57f5e0c6080b2a4bb8a2ac2`  
		Last Modified: Tue, 13 Aug 2024 06:14:33 GMT  
		Size: 44.3 MB (44276093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf074a2d2ee71fc778577394598994ba79defcfebcf8234714bb4403b9beff71`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2eff715fc140f8d8673333b8b3aab68990ba7d103400a9ed714554174df64f`  
		Last Modified: Tue, 13 Aug 2024 06:14:33 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c612dfb3807513faf229144dad75f2bb5af9caa5ff171426664c4d066e5de`  
		Last Modified: Tue, 13 Aug 2024 06:14:33 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:d6bd28a190c6284da0493f4bf5fa1eb8436b144ba0d225566d48ae1eabf69698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e127ca5f80ddb8faab9a53351caec5483836a4a6738c368717b7f46e0030d979`

```dockerfile
```

-	Layers:
	-	`sha256:14ebf33d780e54d524ec0a4908348ea4474d4accab3dc3ad65b3e00406692a31`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 2.7 MB (2693243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5cfcf687e51c4a3124d5bd766fe1c3223794717b0e762523e87079e60613b6`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8306fc57783667796d04956a0bc9824e5519cdc86e79404c52f451cadc33f515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81800593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3536354914de845fb9e6d00f012373ae54397a015642b573264b25a8550b88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b117a832b332535ec3b83dd4ded35fc32749ddc63215f1f9833a5c935b07c949`  
		Last Modified: Tue, 13 Aug 2024 06:13:19 GMT  
		Size: 7.6 MB (7649263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be30bd17377c5a726f876fd22fffb7968096a80be7bfca26c99ec53b524bada`  
		Last Modified: Tue, 13 Aug 2024 06:13:20 GMT  
		Size: 45.0 MB (44970331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc38e7253a66c453288470d2eeb66250ac8924124680f7c439e1fab10d84a1`  
		Last Modified: Tue, 13 Aug 2024 06:13:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e92d47cf4e44a4f24e075c908bd9ac7c41897e6f8f9a293d9b156a57e3e3a7`  
		Last Modified: Tue, 13 Aug 2024 06:13:19 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fe3e644c2ff8d6e442d809b70add3b01aae6ec1777836f0a2e651281b301db`  
		Last Modified: Tue, 13 Aug 2024 06:13:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:88687fdcc1eefed32ab2275cc83992f5a64c85187a4ea20f7d27bd99e6c1813f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe0aea431654dea6f946f5c5fe4112e3be07021c6fb56189d65276b85241406`

```dockerfile
```

-	Layers:
	-	`sha256:678d7c4634f51f7383dba93c13f2e6f0585bb1ece7dcc1de576de512a492a910`  
		Last Modified: Tue, 13 Aug 2024 06:13:18 GMT  
		Size: 2.7 MB (2691219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d54af3efccd2dba33916dc3fa3e8cfde425809f2ff3ea9d46dff8d7508855e`  
		Last Modified: Tue, 13 Aug 2024 06:13:18 GMT  
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
$ docker pull chronograf@sha256:7f630d57f28b6323f69889f2a84c65770149a16903566fb1e06d9973a92c0862
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
$ docker pull chronograf@sha256:ed58ebdd45b2968693114803d98dcd20bb2a0293ee289fc70b862dbdab538846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70400184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae3e31c03d8856c624bd0d72f88c6691a35d2f8722976abbff853f2e4fa277a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1aef2e3a5d5cd26838c900ee03d65496748b071a335a970600831fe1c2c1d`  
		Last Modified: Tue, 13 Aug 2024 01:10:51 GMT  
		Size: 4.2 MB (4209269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7c3fda4e5926545c408a513857cf84ac71fc5837cf7c5151baf389ba8cc7e`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 34.7 MB (34738243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873a729c8d41b180cf813c557c10a3ce485bf83d6b13c64d273267b02c414c3f`  
		Last Modified: Tue, 13 Aug 2024 01:10:51 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb414545ffb9356f8e9c5f80322d579af0cfea846da3561a17f54a868251993`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab72208668e1a95c44c285240b965305e4bf13e20269e8907767b1e96a8f56`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:9ee90421e73001f4b399726646dae68f0a66f32e80c768c08410b0da19809760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a657df4f0ab7e8a49cd0b4cacebc1bb68dbb95cec80bd7053b87279639e752`

```dockerfile
```

-	Layers:
	-	`sha256:648e995982dab3388cc719480d616b69a64fc4ff54643e58f80d6d66940438c6`  
		Last Modified: Tue, 13 Aug 2024 01:10:51 GMT  
		Size: 2.9 MB (2893542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff242b1b95a38425642530483513512dac933e99f3609289249a1251b2d9454b`  
		Last Modified: Tue, 13 Aug 2024 01:10:51 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:53e61391245417cf2f1e8a1be0da72443d47749c030a7c3666f8fdb6f01fed4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d51b74c53407778a386cb8f5679e606aa83e110ff6df843eaa203817eca717a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9f6a2e97ea42608bfeab22c77e01d6614f64a00a2be04ed1cff9909375d517a8 in / 
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
	-	`sha256:1a1ab1e12ebdbe1b5383067049fc746bcb9b882bd309b8befaa11c47eed5d4dd`  
		Last Modified: Tue, 13 Aug 2024 01:01:38 GMT  
		Size: 26.6 MB (26589215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f321bcbdc4699be601fb54a7920daab2380bc3bbe1d198eebdf1525bc59bd`  
		Last Modified: Tue, 13 Aug 2024 04:28:58 GMT  
		Size: 3.5 MB (3511564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef3d40c094b07e507900a17343eed605c2fb42557d90e6196272e50e5f5357`  
		Last Modified: Tue, 13 Aug 2024 04:28:59 GMT  
		Size: 33.1 MB (33097362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca247a79d1fc3ea113de3ab51152a4ee2ccff57568e470138659d79578d7c3b7`  
		Last Modified: Tue, 13 Aug 2024 04:28:57 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61c62ae30f3e5b59ed01307026742fd06ba7b2e9111b15e1218621ae87be049`  
		Last Modified: Tue, 13 Aug 2024 04:28:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecf7d96a772c3478f6a720a0b82e63454778c5d7c03d75bffdcb4a503c42d59`  
		Last Modified: Tue, 13 Aug 2024 04:28:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:af9b53e05dfbcbb503bdbfbf09404f1fc32743b33c07be13853e91d6be721388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2911462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0c4bb9a128c41f10ff1cc8df5683be9b0e635c41f31808252b7d001005328e`

```dockerfile
```

-	Layers:
	-	`sha256:5d776e6e99ba36a9a7a40e6bb49c6b145c2fc6e6608a326b0454bef990b5614d`  
		Last Modified: Tue, 13 Aug 2024 04:28:58 GMT  
		Size: 2.9 MB (2895812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea336893ff4dcf04f1247957b10a1953fd934a14aaf3519288ac3694850aca1`  
		Last Modified: Tue, 13 Aug 2024 04:28:57 GMT  
		Size: 15.7 KB (15650 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:93a0005cc94a9e6962ce7b0cc7bf99c6ba066c62b0373a31baaf9f556b0e4257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67548788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47e13d7200359e0a1bcef47372144c6e2d6e93e21dfbb9c4f0fb555c7c8f0d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890f2a6836d05b57c2a638e661fc71ab5e8977e788f1a4625fefb534b54e6fbf`  
		Last Modified: Tue, 13 Aug 2024 03:43:57 GMT  
		Size: 4.2 MB (4210492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86562559c1a7a318e7aa4212c3f5abdc138c873557b528c6a57b3f0636f36b25`  
		Last Modified: Tue, 13 Aug 2024 03:43:58 GMT  
		Size: 33.2 MB (33237809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35f5ac1cc99021909472a2cb9f33a041239e86e8153924b6e034760ba442e7b`  
		Last Modified: Tue, 13 Aug 2024 03:43:57 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c1414eae447bf7409b1096c38eeb3e59bee4e9229c9ac0ec7f6fa00fe5b192`  
		Last Modified: Tue, 13 Aug 2024 03:43:58 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8a4c7ed63a27153ad688d0a966314ca42d9eced56ce62b115f03b216904f36`  
		Last Modified: Tue, 13 Aug 2024 03:43:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:b10389735719d0281d7948944610a17d7e3495b2cb722bcd236e6e30ed27a1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b5760005b62a859aa732c989cb66af3e62e9ae8a2dbefaaa95c334d9c5e39e`

```dockerfile
```

-	Layers:
	-	`sha256:62d7cb569c7403a93e90882e24c5934290bba79d610ce624896065cb04f36735`  
		Last Modified: Tue, 13 Aug 2024 03:43:57 GMT  
		Size: 2.9 MB (2893790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8be897ca109d9a3bc875d4a07eaa5bb21efeb7e76d351f0eb727d102215236c`  
		Last Modified: Tue, 13 Aug 2024 03:43:57 GMT  
		Size: 15.9 KB (15868 bytes)  
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
$ docker pull chronograf@sha256:7f630d57f28b6323f69889f2a84c65770149a16903566fb1e06d9973a92c0862
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
$ docker pull chronograf@sha256:ed58ebdd45b2968693114803d98dcd20bb2a0293ee289fc70b862dbdab538846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70400184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae3e31c03d8856c624bd0d72f88c6691a35d2f8722976abbff853f2e4fa277a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd1aef2e3a5d5cd26838c900ee03d65496748b071a335a970600831fe1c2c1d`  
		Last Modified: Tue, 13 Aug 2024 01:10:51 GMT  
		Size: 4.2 MB (4209269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7c3fda4e5926545c408a513857cf84ac71fc5837cf7c5151baf389ba8cc7e`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 34.7 MB (34738243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873a729c8d41b180cf813c557c10a3ce485bf83d6b13c64d273267b02c414c3f`  
		Last Modified: Tue, 13 Aug 2024 01:10:51 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb414545ffb9356f8e9c5f80322d579af0cfea846da3561a17f54a868251993`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab72208668e1a95c44c285240b965305e4bf13e20269e8907767b1e96a8f56`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:9ee90421e73001f4b399726646dae68f0a66f32e80c768c08410b0da19809760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a657df4f0ab7e8a49cd0b4cacebc1bb68dbb95cec80bd7053b87279639e752`

```dockerfile
```

-	Layers:
	-	`sha256:648e995982dab3388cc719480d616b69a64fc4ff54643e58f80d6d66940438c6`  
		Last Modified: Tue, 13 Aug 2024 01:10:51 GMT  
		Size: 2.9 MB (2893542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff242b1b95a38425642530483513512dac933e99f3609289249a1251b2d9454b`  
		Last Modified: Tue, 13 Aug 2024 01:10:51 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:53e61391245417cf2f1e8a1be0da72443d47749c030a7c3666f8fdb6f01fed4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d51b74c53407778a386cb8f5679e606aa83e110ff6df843eaa203817eca717a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9f6a2e97ea42608bfeab22c77e01d6614f64a00a2be04ed1cff9909375d517a8 in / 
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
	-	`sha256:1a1ab1e12ebdbe1b5383067049fc746bcb9b882bd309b8befaa11c47eed5d4dd`  
		Last Modified: Tue, 13 Aug 2024 01:01:38 GMT  
		Size: 26.6 MB (26589215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f321bcbdc4699be601fb54a7920daab2380bc3bbe1d198eebdf1525bc59bd`  
		Last Modified: Tue, 13 Aug 2024 04:28:58 GMT  
		Size: 3.5 MB (3511564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef3d40c094b07e507900a17343eed605c2fb42557d90e6196272e50e5f5357`  
		Last Modified: Tue, 13 Aug 2024 04:28:59 GMT  
		Size: 33.1 MB (33097362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca247a79d1fc3ea113de3ab51152a4ee2ccff57568e470138659d79578d7c3b7`  
		Last Modified: Tue, 13 Aug 2024 04:28:57 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61c62ae30f3e5b59ed01307026742fd06ba7b2e9111b15e1218621ae87be049`  
		Last Modified: Tue, 13 Aug 2024 04:28:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecf7d96a772c3478f6a720a0b82e63454778c5d7c03d75bffdcb4a503c42d59`  
		Last Modified: Tue, 13 Aug 2024 04:28:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:af9b53e05dfbcbb503bdbfbf09404f1fc32743b33c07be13853e91d6be721388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2911462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0c4bb9a128c41f10ff1cc8df5683be9b0e635c41f31808252b7d001005328e`

```dockerfile
```

-	Layers:
	-	`sha256:5d776e6e99ba36a9a7a40e6bb49c6b145c2fc6e6608a326b0454bef990b5614d`  
		Last Modified: Tue, 13 Aug 2024 04:28:58 GMT  
		Size: 2.9 MB (2895812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea336893ff4dcf04f1247957b10a1953fd934a14aaf3519288ac3694850aca1`  
		Last Modified: Tue, 13 Aug 2024 04:28:57 GMT  
		Size: 15.7 KB (15650 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:93a0005cc94a9e6962ce7b0cc7bf99c6ba066c62b0373a31baaf9f556b0e4257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67548788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47e13d7200359e0a1bcef47372144c6e2d6e93e21dfbb9c4f0fb555c7c8f0d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890f2a6836d05b57c2a638e661fc71ab5e8977e788f1a4625fefb534b54e6fbf`  
		Last Modified: Tue, 13 Aug 2024 03:43:57 GMT  
		Size: 4.2 MB (4210492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86562559c1a7a318e7aa4212c3f5abdc138c873557b528c6a57b3f0636f36b25`  
		Last Modified: Tue, 13 Aug 2024 03:43:58 GMT  
		Size: 33.2 MB (33237809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35f5ac1cc99021909472a2cb9f33a041239e86e8153924b6e034760ba442e7b`  
		Last Modified: Tue, 13 Aug 2024 03:43:57 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c1414eae447bf7409b1096c38eeb3e59bee4e9229c9ac0ec7f6fa00fe5b192`  
		Last Modified: Tue, 13 Aug 2024 03:43:58 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8a4c7ed63a27153ad688d0a966314ca42d9eced56ce62b115f03b216904f36`  
		Last Modified: Tue, 13 Aug 2024 03:43:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:b10389735719d0281d7948944610a17d7e3495b2cb722bcd236e6e30ed27a1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b5760005b62a859aa732c989cb66af3e62e9ae8a2dbefaaa95c334d9c5e39e`

```dockerfile
```

-	Layers:
	-	`sha256:62d7cb569c7403a93e90882e24c5934290bba79d610ce624896065cb04f36735`  
		Last Modified: Tue, 13 Aug 2024 03:43:57 GMT  
		Size: 2.9 MB (2893790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8be897ca109d9a3bc875d4a07eaa5bb21efeb7e76d351f0eb727d102215236c`  
		Last Modified: Tue, 13 Aug 2024 03:43:57 GMT  
		Size: 15.9 KB (15868 bytes)  
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
$ docker pull chronograf@sha256:bc8b9ea757c37dac27ea2e050ce9cddf8db19aad6cd55d2e9a4a7032a241ba1b
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
$ docker pull chronograf@sha256:c84ddd810046ecad7d7ce7eae758fb5b9e88d2da681bebb43a52c3813022cbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71040954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903f8304b0b4a8478daeb520a10801885715e79412e2471a584598b183144e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7270a75c0dceb6de53fd6e273d59232b969970ba1e59663e8137cfd1ef67f46f`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 5.2 MB (5224225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee3388f0e5abab1585d0ef768f649aa1761fe059f70d4ce467e6f35ee70d3e3`  
		Last Modified: Tue, 13 Aug 2024 01:10:54 GMT  
		Size: 34.4 MB (34364059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31b7e010667719bd0131269ba63ce10ee90b1e5e03d1118479b5c7f3ecddf8`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7f2ef81baa0a30b0a3f0928fae888e1e555bd02b8528f6040cff68031682d6`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc77ee52cbf3cd485713acd95289d9bd870f6dde9bf13becffecd9c7eadd260`  
		Last Modified: Tue, 13 Aug 2024 01:10:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:37e72e4cbc0a99e856cd428f5ec6136f1fcf51e91659bb09bb09afafd4af2c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420355e28d4304daf37ecab246179c7bb0df72614e6b5a0b34dc1d08d393e5f9`

```dockerfile
```

-	Layers:
	-	`sha256:81b3df1d74554391e41ad14b60ea911767c2566e72f4b3f0cfa564665c90d5e2`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 2.9 MB (2949640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3409000ed29ff41d95fd15dc29750a00a90ad9f06769a7e3e57c77b4bbac864d`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:aae8e5af68eb2a5cce60a591d0219cbff332d27326a3913f4e9dada3e384f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63638318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0ffd5a0a5d0a2ea0676701d90ff3386f21503160f5802f04ce7e3419bb6da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9f6a2e97ea42608bfeab22c77e01d6614f64a00a2be04ed1cff9909375d517a8 in / 
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
	-	`sha256:1a1ab1e12ebdbe1b5383067049fc746bcb9b882bd309b8befaa11c47eed5d4dd`  
		Last Modified: Tue, 13 Aug 2024 01:01:38 GMT  
		Size: 26.6 MB (26589215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a42e5baaebef08161604543d0178fada8481884bdae577deb3ca2f61dd1b74a`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 4.5 MB (4490067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a008fe5670ccbca64de527982e46593a50293d2f90f82b05885d407c7604562e`  
		Last Modified: Tue, 13 Aug 2024 06:12:18 GMT  
		Size: 32.5 MB (32534647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80731278352bd1aa487ade403bca1464eb8edd5b0c6dd8cc6e9b71844a92931f`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8192e21175861780b6a856ecee709e8ec02fb8da73addf2ce0f6cd2310961d18`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137fb33ecd585deca23c82faf8aaf67ff638f76feaa1a54134cd39fc8b0fc821`  
		Last Modified: Tue, 13 Aug 2024 06:12:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:01b142f721ca660d1adfed65c3ac1e64575460562e7b6378242e9673f28b4606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee3c84352e875938a3366938459f21632ed533a4e2394a090f75c06deaff291`

```dockerfile
```

-	Layers:
	-	`sha256:74157ea1b67ddff12d6e0684e767100001d1d6fcddbc6fca0d9832da78b79c2d`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 3.0 MB (2951910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da53ea3c6c3d880fbd25bf67e300e97d625a22617fd20969c77df31581d353e0`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:14eca5891cb4dde0228d55164de8db5513cfea38bfff018180dfa6fd9526e145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67737955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e66d5336359047ea6396bf0d4d0d7482e55bedb88b3571f01d0b1c7ddf5741b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97c21cd1bb86458c52804743230c6bcbc316e8ec413238350ae254600532714`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 5.2 MB (5207980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322c439bca740603f3dc12c3fdceba7f60d7f1ee8cd39bf0ae0d352d7dce939a`  
		Last Modified: Tue, 13 Aug 2024 06:09:13 GMT  
		Size: 32.4 MB (32429488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c332f20a194ece80813e825f107da8e618e9084a63bed07d3693de1cd8530a38`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1baf866eacca2fb0774ccc512697ddae9ac7f7ca8607a09554126f15abb2db`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9cab8f3eadeada24de206cb69cc11bd79eb1654fbf01fd997c6919d2ae6e48`  
		Last Modified: Tue, 13 Aug 2024 06:09:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:191e80fa5abad7fadf7079b003fb04b0e3dc71c61408e4afac89a8650cbf8a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8143c15632fec2db91823b36e10fad1927795763e9b372ecbc8b737a28cb0521`

```dockerfile
```

-	Layers:
	-	`sha256:1f961395096426e85e38c4f2814f6e0df2795e9b5950950cc6b8ddbd9e3cdfc2`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 2.9 MB (2949888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b5008826bfc995f89c05b59a152f29909187bb04ce758b0b3957419c74e8689`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
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
$ docker pull chronograf@sha256:bc8b9ea757c37dac27ea2e050ce9cddf8db19aad6cd55d2e9a4a7032a241ba1b
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
$ docker pull chronograf@sha256:c84ddd810046ecad7d7ce7eae758fb5b9e88d2da681bebb43a52c3813022cbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71040954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903f8304b0b4a8478daeb520a10801885715e79412e2471a584598b183144e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7270a75c0dceb6de53fd6e273d59232b969970ba1e59663e8137cfd1ef67f46f`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 5.2 MB (5224225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee3388f0e5abab1585d0ef768f649aa1761fe059f70d4ce467e6f35ee70d3e3`  
		Last Modified: Tue, 13 Aug 2024 01:10:54 GMT  
		Size: 34.4 MB (34364059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31b7e010667719bd0131269ba63ce10ee90b1e5e03d1118479b5c7f3ecddf8`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7f2ef81baa0a30b0a3f0928fae888e1e555bd02b8528f6040cff68031682d6`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc77ee52cbf3cd485713acd95289d9bd870f6dde9bf13becffecd9c7eadd260`  
		Last Modified: Tue, 13 Aug 2024 01:10:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:37e72e4cbc0a99e856cd428f5ec6136f1fcf51e91659bb09bb09afafd4af2c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420355e28d4304daf37ecab246179c7bb0df72614e6b5a0b34dc1d08d393e5f9`

```dockerfile
```

-	Layers:
	-	`sha256:81b3df1d74554391e41ad14b60ea911767c2566e72f4b3f0cfa564665c90d5e2`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 2.9 MB (2949640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3409000ed29ff41d95fd15dc29750a00a90ad9f06769a7e3e57c77b4bbac864d`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:aae8e5af68eb2a5cce60a591d0219cbff332d27326a3913f4e9dada3e384f541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63638318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0ffd5a0a5d0a2ea0676701d90ff3386f21503160f5802f04ce7e3419bb6da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9f6a2e97ea42608bfeab22c77e01d6614f64a00a2be04ed1cff9909375d517a8 in / 
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
	-	`sha256:1a1ab1e12ebdbe1b5383067049fc746bcb9b882bd309b8befaa11c47eed5d4dd`  
		Last Modified: Tue, 13 Aug 2024 01:01:38 GMT  
		Size: 26.6 MB (26589215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a42e5baaebef08161604543d0178fada8481884bdae577deb3ca2f61dd1b74a`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 4.5 MB (4490067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a008fe5670ccbca64de527982e46593a50293d2f90f82b05885d407c7604562e`  
		Last Modified: Tue, 13 Aug 2024 06:12:18 GMT  
		Size: 32.5 MB (32534647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80731278352bd1aa487ade403bca1464eb8edd5b0c6dd8cc6e9b71844a92931f`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8192e21175861780b6a856ecee709e8ec02fb8da73addf2ce0f6cd2310961d18`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137fb33ecd585deca23c82faf8aaf67ff638f76feaa1a54134cd39fc8b0fc821`  
		Last Modified: Tue, 13 Aug 2024 06:12:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:01b142f721ca660d1adfed65c3ac1e64575460562e7b6378242e9673f28b4606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee3c84352e875938a3366938459f21632ed533a4e2394a090f75c06deaff291`

```dockerfile
```

-	Layers:
	-	`sha256:74157ea1b67ddff12d6e0684e767100001d1d6fcddbc6fca0d9832da78b79c2d`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 3.0 MB (2951910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da53ea3c6c3d880fbd25bf67e300e97d625a22617fd20969c77df31581d353e0`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:14eca5891cb4dde0228d55164de8db5513cfea38bfff018180dfa6fd9526e145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67737955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e66d5336359047ea6396bf0d4d0d7482e55bedb88b3571f01d0b1c7ddf5741b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97c21cd1bb86458c52804743230c6bcbc316e8ec413238350ae254600532714`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 5.2 MB (5207980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322c439bca740603f3dc12c3fdceba7f60d7f1ee8cd39bf0ae0d352d7dce939a`  
		Last Modified: Tue, 13 Aug 2024 06:09:13 GMT  
		Size: 32.4 MB (32429488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c332f20a194ece80813e825f107da8e618e9084a63bed07d3693de1cd8530a38`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1baf866eacca2fb0774ccc512697ddae9ac7f7ca8607a09554126f15abb2db`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9cab8f3eadeada24de206cb69cc11bd79eb1654fbf01fd997c6919d2ae6e48`  
		Last Modified: Tue, 13 Aug 2024 06:09:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:191e80fa5abad7fadf7079b003fb04b0e3dc71c61408e4afac89a8650cbf8a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8143c15632fec2db91823b36e10fad1927795763e9b372ecbc8b737a28cb0521`

```dockerfile
```

-	Layers:
	-	`sha256:1f961395096426e85e38c4f2814f6e0df2795e9b5950950cc6b8ddbd9e3cdfc2`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 2.9 MB (2949888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b5008826bfc995f89c05b59a152f29909187bb04ce758b0b3957419c74e8689`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
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
$ docker pull chronograf@sha256:685c0cff647a6befcf583f1c162cee5abe516aa6c682b8156e7a67445a49d951
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
$ docker pull chronograf@sha256:abc064f543a8a10a867493542076d386584502570a5c76318586600159712178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71688459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4baff57d50a8418e3305c0c1242b843791a0d621484858c0fd6232724fc894`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6416ee91117dd47e3a0e8097bfa64ebb114137c401dc9c5b0e70d33a47cda53f`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 5.2 MB (5224231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1069e5a2cef1788b12f887c417dd97f01f13399ac63dc20cd2a0287793cfeba`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 35.0 MB (35011555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9989395404b312a1ab6b523371e00610393c910dc3a13027ccda328892b419df`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe2a88aaa86998b8a64723e9bc260834c8fb61f9377c16d5277c323882cfba8`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf04896fecd4ddd6f1dfbf6f4fd153fe8589f51e1bab9b18452e815b426e4ea2`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:15c35fd8aea8c845165b4494163c5cb85ffb1faf28441b7147aabac400bf4359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87fbf545c9ae3bac289dd193dd1fac97abbffc84f1f7485b1cbc876a1356592`

```dockerfile
```

-	Layers:
	-	`sha256:e2cab605f0cbaf32aa1e9c65c699e815f6ca10f5be54aa06942b101c820f6c97`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 3.0 MB (2954790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528a77a18b93a95d6d83c1f10e20485168516804f841a6bca083033e2be5a47a`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 15.6 KB (15616 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:240ec03232f70106c115dc233f993abafe47f2ae6fe8e9a8f86fe66ce92f68b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64415039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3a6e5ca32d00ed64020f8f1f02c0d91bfa2876b5c501ff764393135bc02165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9f6a2e97ea42608bfeab22c77e01d6614f64a00a2be04ed1cff9909375d517a8 in / 
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
	-	`sha256:1a1ab1e12ebdbe1b5383067049fc746bcb9b882bd309b8befaa11c47eed5d4dd`  
		Last Modified: Tue, 13 Aug 2024 01:01:38 GMT  
		Size: 26.6 MB (26589215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a42e5baaebef08161604543d0178fada8481884bdae577deb3ca2f61dd1b74a`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 4.5 MB (4490067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d91368016d40b8960974bb4e3f5a3e7d71ecaad7de867592ccddabf6212e56e`  
		Last Modified: Tue, 13 Aug 2024 06:13:33 GMT  
		Size: 33.3 MB (33311364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd57178f50c07619ee3eda740318140c14eeb3949b970f1ad3a83967ba95dac6`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8735e54cdc6fe12cc369764c8babd3ebfc4c0ab483560fcaf137fb1f36a2da4`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24a0fde11ada91b92ced56f1ce737ac19aa44d6b2eb8ab2fc59dc1e35ae90d8`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:920a78f804ef46f30e3b49063ee0b9f8956ddc1000478f58db5196889c3c039a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da7ed7e333aef2e227927f5eb6b23da23db909147c2dac63340793299dff8e1`

```dockerfile
```

-	Layers:
	-	`sha256:47389970c646d141af79ddd34ad3270265b1827038fb2e91faa17e2b34c8edda`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 3.0 MB (2957060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bf40dc3934e627dbfdfb8f1a039ba7b6236421037afe810522a320c2f8064c`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6cb65d1beab74e3eec0313997c3da435ad07e00b1aaeedf19316a5c082b01e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68489894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3da9b36f4f6772c8c7ce2d85265d53ed1db9768e9dd101f356ade177b3cabc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97c21cd1bb86458c52804743230c6bcbc316e8ec413238350ae254600532714`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 5.2 MB (5207980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ac55858b6ab4f6fa50a20d011eda5c83deaba0d4be4bb3f1d1bf6b7d968344`  
		Last Modified: Tue, 13 Aug 2024 06:11:10 GMT  
		Size: 33.2 MB (33181437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d15b9159f30a7b622eb54693b7ebf077338378749120ae1f36a8604d75d30`  
		Last Modified: Tue, 13 Aug 2024 06:11:08 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608848752a9835f3358d8d0d8dd5ff027f0055f9022efe0833fa4dff8b6cda15`  
		Last Modified: Tue, 13 Aug 2024 06:11:09 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b6cd70de3dcf8a4b5b8777160ec362a5976d3009dbf7e0c26afb1779883798`  
		Last Modified: Tue, 13 Aug 2024 06:11:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:2cc83da2431317bba968e8c7b2eebc4d4abbcdb228f64dda80da37d9195862db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0960f54c95fd588344d316e8acd885ec2e8330e97012bc6fd42665a610398dd`

```dockerfile
```

-	Layers:
	-	`sha256:7f74f1d1827e48b6d4afa72e54fb5e42f9278f9b7a0ec7cc2204654b74e28dd3`  
		Last Modified: Tue, 13 Aug 2024 06:11:09 GMT  
		Size: 3.0 MB (2955038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75eceb1091fdd8a42ef4fad651021c2eff0d31873b5ca85eca4c3a4fcbf08932`  
		Last Modified: Tue, 13 Aug 2024 06:11:08 GMT  
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
$ docker pull chronograf@sha256:685c0cff647a6befcf583f1c162cee5abe516aa6c682b8156e7a67445a49d951
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
$ docker pull chronograf@sha256:abc064f543a8a10a867493542076d386584502570a5c76318586600159712178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71688459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4baff57d50a8418e3305c0c1242b843791a0d621484858c0fd6232724fc894`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6416ee91117dd47e3a0e8097bfa64ebb114137c401dc9c5b0e70d33a47cda53f`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 5.2 MB (5224231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1069e5a2cef1788b12f887c417dd97f01f13399ac63dc20cd2a0287793cfeba`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 35.0 MB (35011555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9989395404b312a1ab6b523371e00610393c910dc3a13027ccda328892b419df`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe2a88aaa86998b8a64723e9bc260834c8fb61f9377c16d5277c323882cfba8`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf04896fecd4ddd6f1dfbf6f4fd153fe8589f51e1bab9b18452e815b426e4ea2`  
		Last Modified: Tue, 13 Aug 2024 01:10:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:15c35fd8aea8c845165b4494163c5cb85ffb1faf28441b7147aabac400bf4359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87fbf545c9ae3bac289dd193dd1fac97abbffc84f1f7485b1cbc876a1356592`

```dockerfile
```

-	Layers:
	-	`sha256:e2cab605f0cbaf32aa1e9c65c699e815f6ca10f5be54aa06942b101c820f6c97`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 3.0 MB (2954790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528a77a18b93a95d6d83c1f10e20485168516804f841a6bca083033e2be5a47a`  
		Last Modified: Tue, 13 Aug 2024 01:10:52 GMT  
		Size: 15.6 KB (15616 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:240ec03232f70106c115dc233f993abafe47f2ae6fe8e9a8f86fe66ce92f68b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64415039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3a6e5ca32d00ed64020f8f1f02c0d91bfa2876b5c501ff764393135bc02165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9f6a2e97ea42608bfeab22c77e01d6614f64a00a2be04ed1cff9909375d517a8 in / 
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
	-	`sha256:1a1ab1e12ebdbe1b5383067049fc746bcb9b882bd309b8befaa11c47eed5d4dd`  
		Last Modified: Tue, 13 Aug 2024 01:01:38 GMT  
		Size: 26.6 MB (26589215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a42e5baaebef08161604543d0178fada8481884bdae577deb3ca2f61dd1b74a`  
		Last Modified: Tue, 13 Aug 2024 06:12:17 GMT  
		Size: 4.5 MB (4490067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d91368016d40b8960974bb4e3f5a3e7d71ecaad7de867592ccddabf6212e56e`  
		Last Modified: Tue, 13 Aug 2024 06:13:33 GMT  
		Size: 33.3 MB (33311364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd57178f50c07619ee3eda740318140c14eeb3949b970f1ad3a83967ba95dac6`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8735e54cdc6fe12cc369764c8babd3ebfc4c0ab483560fcaf137fb1f36a2da4`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24a0fde11ada91b92ced56f1ce737ac19aa44d6b2eb8ab2fc59dc1e35ae90d8`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:920a78f804ef46f30e3b49063ee0b9f8956ddc1000478f58db5196889c3c039a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da7ed7e333aef2e227927f5eb6b23da23db909147c2dac63340793299dff8e1`

```dockerfile
```

-	Layers:
	-	`sha256:47389970c646d141af79ddd34ad3270265b1827038fb2e91faa17e2b34c8edda`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 3.0 MB (2957060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bf40dc3934e627dbfdfb8f1a039ba7b6236421037afe810522a320c2f8064c`  
		Last Modified: Tue, 13 Aug 2024 06:13:32 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6cb65d1beab74e3eec0313997c3da435ad07e00b1aaeedf19316a5c082b01e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68489894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3da9b36f4f6772c8c7ce2d85265d53ed1db9768e9dd101f356ade177b3cabc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97c21cd1bb86458c52804743230c6bcbc316e8ec413238350ae254600532714`  
		Last Modified: Tue, 13 Aug 2024 06:09:12 GMT  
		Size: 5.2 MB (5207980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ac55858b6ab4f6fa50a20d011eda5c83deaba0d4be4bb3f1d1bf6b7d968344`  
		Last Modified: Tue, 13 Aug 2024 06:11:10 GMT  
		Size: 33.2 MB (33181437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d15b9159f30a7b622eb54693b7ebf077338378749120ae1f36a8604d75d30`  
		Last Modified: Tue, 13 Aug 2024 06:11:08 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608848752a9835f3358d8d0d8dd5ff027f0055f9022efe0833fa4dff8b6cda15`  
		Last Modified: Tue, 13 Aug 2024 06:11:09 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b6cd70de3dcf8a4b5b8777160ec362a5976d3009dbf7e0c26afb1779883798`  
		Last Modified: Tue, 13 Aug 2024 06:11:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:2cc83da2431317bba968e8c7b2eebc4d4abbcdb228f64dda80da37d9195862db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0960f54c95fd588344d316e8acd885ec2e8330e97012bc6fd42665a610398dd`

```dockerfile
```

-	Layers:
	-	`sha256:7f74f1d1827e48b6d4afa72e54fb5e42f9278f9b7a0ec7cc2204654b74e28dd3`  
		Last Modified: Tue, 13 Aug 2024 06:11:09 GMT  
		Size: 3.0 MB (2955038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75eceb1091fdd8a42ef4fad651021c2eff0d31873b5ca85eca4c3a4fcbf08932`  
		Last Modified: Tue, 13 Aug 2024 06:11:08 GMT  
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
$ docker pull chronograf@sha256:7501ef406fe9cb5edd43c702abe4de2a399ada7af5db4930c2966b8389eba7d9
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
$ docker pull chronograf@sha256:7103a0bb3d05646aac948fded55ac5201a5dc034df0aea97a3e9a497efaba292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84239467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257d3e20f92a7d73776d501432bd55abbd7e5164af3752fc8a081997f3909d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a769aefe23aebedcc5633ec6f52ebe4f5aa8eb5e942fb6ca9909454f3c5db7f4`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 7.9 MB (7871448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb49135b5a2b70e24894ece5df348bc1a45b19deb65faf4f99a30bbc92c65c8b`  
		Last Modified: Tue, 13 Aug 2024 01:11:04 GMT  
		Size: 47.2 MB (47217317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f6e528c458b87aa12af4f246a3929e0b8a17601531416271de9963650eb175`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b351d1b71edfa42cc9ddbf889b7b08d51afdba224a131837a2613690e255bc90`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30089f8784c53073e232ca2754a37eb5bfdc1e99a4c21b0b2a8303f4fd7b1ea2`  
		Last Modified: Tue, 13 Aug 2024 01:11:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:a50f53cfbec4cd00eca332ec9faab269a575a00fbd18818d189f88c076b38e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1004bd7be2d69aec9e0a3a5beedd32f3d874967b4614667db44cc32bc9fb8e8`

```dockerfile
```

-	Layers:
	-	`sha256:a577157f8d99c2f5526035aea9fcb37666a4e74dd74eb58292711f05f93839bc`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 2.7 MB (2690947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15565333f9c38d7a0464b70ad77a25b8c8c5e7b89c3976379a852393d75e3d06`  
		Last Modified: Tue, 13 Aug 2024 01:11:03 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:39319375770d59f58ba8f8cf452889082a3fe121ef1678a4b0b9d088408f317a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75514585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b275637aa1c6b1edbe24465e3a37c48bbc4e2a1de237585d38c67c2bbb2acc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
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
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e8801ac7c9368437cbe587ff1aad7e371dd42bdd6f04c05928a914df092f1`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 6.5 MB (6495882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca6877c9cb8387a29111e067ff33053781c94cfb57f5e0c6080b2a4bb8a2ac2`  
		Last Modified: Tue, 13 Aug 2024 06:14:33 GMT  
		Size: 44.3 MB (44276093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf074a2d2ee71fc778577394598994ba79defcfebcf8234714bb4403b9beff71`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2eff715fc140f8d8673333b8b3aab68990ba7d103400a9ed714554174df64f`  
		Last Modified: Tue, 13 Aug 2024 06:14:33 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c612dfb3807513faf229144dad75f2bb5af9caa5ff171426664c4d066e5de`  
		Last Modified: Tue, 13 Aug 2024 06:14:33 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d6bd28a190c6284da0493f4bf5fa1eb8436b144ba0d225566d48ae1eabf69698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e127ca5f80ddb8faab9a53351caec5483836a4a6738c368717b7f46e0030d979`

```dockerfile
```

-	Layers:
	-	`sha256:14ebf33d780e54d524ec0a4908348ea4474d4accab3dc3ad65b3e00406692a31`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 2.7 MB (2693243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5cfcf687e51c4a3124d5bd766fe1c3223794717b0e762523e87079e60613b6`  
		Last Modified: Tue, 13 Aug 2024 06:14:32 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8306fc57783667796d04956a0bc9824e5519cdc86e79404c52f451cadc33f515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81800593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3536354914de845fb9e6d00f012373ae54397a015642b573264b25a8550b88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b117a832b332535ec3b83dd4ded35fc32749ddc63215f1f9833a5c935b07c949`  
		Last Modified: Tue, 13 Aug 2024 06:13:19 GMT  
		Size: 7.6 MB (7649263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be30bd17377c5a726f876fd22fffb7968096a80be7bfca26c99ec53b524bada`  
		Last Modified: Tue, 13 Aug 2024 06:13:20 GMT  
		Size: 45.0 MB (44970331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc38e7253a66c453288470d2eeb66250ac8924124680f7c439e1fab10d84a1`  
		Last Modified: Tue, 13 Aug 2024 06:13:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e92d47cf4e44a4f24e075c908bd9ac7c41897e6f8f9a293d9b156a57e3e3a7`  
		Last Modified: Tue, 13 Aug 2024 06:13:19 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fe3e644c2ff8d6e442d809b70add3b01aae6ec1777836f0a2e651281b301db`  
		Last Modified: Tue, 13 Aug 2024 06:13:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:88687fdcc1eefed32ab2275cc83992f5a64c85187a4ea20f7d27bd99e6c1813f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe0aea431654dea6f946f5c5fe4112e3be07021c6fb56189d65276b85241406`

```dockerfile
```

-	Layers:
	-	`sha256:678d7c4634f51f7383dba93c13f2e6f0585bb1ece7dcc1de576de512a492a910`  
		Last Modified: Tue, 13 Aug 2024 06:13:18 GMT  
		Size: 2.7 MB (2691219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d54af3efccd2dba33916dc3fa3e8cfde425809f2ff3ea9d46dff8d7508855e`  
		Last Modified: Tue, 13 Aug 2024 06:13:18 GMT  
		Size: 16.2 KB (16231 bytes)  
		MIME: application/vnd.in-toto+json
