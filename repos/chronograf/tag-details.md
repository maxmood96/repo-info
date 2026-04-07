<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.9`](#chronograf1109)
-	[`chronograf:1.10.9-alpine`](#chronograf1109-alpine)
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
$ docker pull chronograf@sha256:47c5576b66fff1426392ca99f67a29b4e7caecc6daa45cfd7a04e3c901ecd499
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
$ docker pull chronograf@sha256:cf3807fb3b6d5e1a167f2c40fc9735ce9b811b79c6f931e125dae995f9c72267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85008414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319eebf3949a35c9433ffb5568b5bcddcff17c2d10a6db22ca0231d615a4e2bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:47:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 01:47:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:47:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:47:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55699494e05bd69b9c319828f65a040b15238883abbb8aa8e051f3f9678740a5`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 7.9 MB (7879779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e811f2ebf7718e013c3b42f4380e0f8c7e092ef1894a9772fac547b69565da`  
		Last Modified: Tue, 07 Apr 2026 01:47:37 GMT  
		Size: 48.9 MB (48867850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4572cb7815b8d85f84d5779c37ffaeaa45a40205aa52600d0772c3f9b65c0e1d`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41629215bf30b7dce998c62fd19d0d4182cdeb284442222bfef4c2a748286a87`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260f04bf26e9e37a65aa5ca1e0ec1f6d2389ade77305722a0dfe0d5a50e8a161`  
		Last Modified: Tue, 07 Apr 2026 01:47:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:c64fee177752fb653bb4c67c264da76fcbd49149f138a7e24dd8136eb7249432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe8767e24afbdcc926ff9bf5b5e6f06ebb5d4e13fcd8efda4891c97d3375d76`

```dockerfile
```

-	Layers:
	-	`sha256:1ad5275ae56819a06df1f709ecc5abbce3f3b30a6576bc62577a6294661aee97`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab9ea4faa68774f8dcfdb171efa8fc2b358380d5ba61fd2d2212d9ef7eef906`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7f6ba8a05e8752787341b7fe2a6a74810b06aa9fa70a1a0228f775cc695b037a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930d1c377ac04e3da986523b9e03970d9aff20f8036670f211d374ae5e6e562c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:04:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 02:04:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:04:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:04:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde4224141eb326416434e57e6985960fa0299c171636ec51c978d7483ded221`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 6.5 MB (6512130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39644797429280d1790a41b83be262964fe685b66a13098f85a2830ef136af23`  
		Last Modified: Tue, 07 Apr 2026 02:04:51 GMT  
		Size: 46.3 MB (46320009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a038716dc519bd0d53565ee9d170bb27389cee982f799ed02c5b30bb400da63b`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2857e0024941e8431e0d2e7288ff873bb60af2b99250a6c109fb700e616232c`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac7ccabd4f0e669d232e23f27536a4797faec571f1d5b385e8d37e9543ad1d4`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:d033ac4c98bc3deb3c46315bff42913e431c32321890ec7914cd6b43bf0a4454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a769173f691e7dbe1bbac685b1b6d2cf8af5e40c11a7536386e603ca5e558e45`

```dockerfile
```

-	Layers:
	-	`sha256:dff92a3ce28b58e918bb8a1b393141f0d15f0a7436d538d1b53bafdf3cd2f3f0`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29723eb32c4a4046b83b01b8e97bd5b93cfc334f24c3dcc9145d178038a36230`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a2a43c10363a3e5414039345eec8b6f29f095b8780f535d2bf8c345ecaccc9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81846058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2139c408fd9e94f3fd3b1367a24940cb005338e161818d060b054dac34b1bfdb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 01:50:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:50:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:50:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dbac72acd22aba48e1d3ad7b9a5e1cbeb7c0aebb12c6a591e18543bc5e15cc`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 7.7 MB (7696984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c262557b34cb3bc7ec83d26805b2652f905d6b967d83f8842bf504468e0a1838`  
		Last Modified: Tue, 07 Apr 2026 01:50:52 GMT  
		Size: 46.0 MB (46008449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74498ce48e4b91d1e7d88a9e0754b61258942627ce75895df3cb7db3c1b5c15`  
		Last Modified: Tue, 07 Apr 2026 01:50:50 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65c1e63d63625f49395f0638311d1e6c4f2c7a8305b76a623caebef010c4bc9`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b076129ef9a105123d5ba844cad634c503183088bbaf98f5207dd723da7a8f3`  
		Last Modified: Tue, 07 Apr 2026 01:50:52 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:2a6ed1d948d7f96ec2f4c78bacc10dff88e412f6fe98b8dbd8b836b5a352f7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f569ab759f8a5b6b8245d0f34e87a8b99fe51d28a3fc5a72fb47d21f8bec4d7d`

```dockerfile
```

-	Layers:
	-	`sha256:d88ff8ebd731cac72703f8bd7c6c93fbe8fe1d291c78a4810ec94e4c492d84cc`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d8afa3639be4d3d75ce8e3dc27463cae0a100a14b3761dab53339f975b1fc7`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:c73bbcdde515b06b9a7c553c92cc69c63197380e32554ac70bc487978d4f93e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f43a15493dfa286ecddb2a321f543ce0782328ace5a68abdb2f0a89fce86a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b149dbf0d54466603c75f2e0a21e5810e13c38a591a4994439fd92a43c9013c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 28 Jan 2026 02:55:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:25 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cc8374b20721167e978930acc3c96665f9488132a58677f6a81dad90f698`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 29.1 MB (29136848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b20d4daed0b72a4ba10efc2998799a5aa3a7b3da28d6057aff046b6d170da1`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a44a4a5cb211d460d00144b50703689629cd5cd3151aa8d989477af9fdddc9`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1870665d6b671bf68d872d353e6f3dcf8bb876176ebe068d36ebd72cc60f1a`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:206f2990c3926bcb3257f329fb9bde8aa579b6391b11966e1c6bcf9e465730b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f49329baac7667c2c41eaab7ec9b27b1f8b819d763c6975b1c546cc58ced7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8abfdf98ab51ee4676e152235fa5a48648b67d72067e3e04c029a7c821689679`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804bbf74bc55745b883375aede79021007da8c962a7342173f0a71dc7ff369e`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9`

```console
$ docker pull chronograf@sha256:47c5576b66fff1426392ca99f67a29b4e7caecc6daa45cfd7a04e3c901ecd499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.9` - linux; amd64

```console
$ docker pull chronograf@sha256:cf3807fb3b6d5e1a167f2c40fc9735ce9b811b79c6f931e125dae995f9c72267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85008414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319eebf3949a35c9433ffb5568b5bcddcff17c2d10a6db22ca0231d615a4e2bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:47:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 01:47:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:47:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:47:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55699494e05bd69b9c319828f65a040b15238883abbb8aa8e051f3f9678740a5`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 7.9 MB (7879779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e811f2ebf7718e013c3b42f4380e0f8c7e092ef1894a9772fac547b69565da`  
		Last Modified: Tue, 07 Apr 2026 01:47:37 GMT  
		Size: 48.9 MB (48867850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4572cb7815b8d85f84d5779c37ffaeaa45a40205aa52600d0772c3f9b65c0e1d`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41629215bf30b7dce998c62fd19d0d4182cdeb284442222bfef4c2a748286a87`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260f04bf26e9e37a65aa5ca1e0ec1f6d2389ade77305722a0dfe0d5a50e8a161`  
		Last Modified: Tue, 07 Apr 2026 01:47:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:c64fee177752fb653bb4c67c264da76fcbd49149f138a7e24dd8136eb7249432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe8767e24afbdcc926ff9bf5b5e6f06ebb5d4e13fcd8efda4891c97d3375d76`

```dockerfile
```

-	Layers:
	-	`sha256:1ad5275ae56819a06df1f709ecc5abbce3f3b30a6576bc62577a6294661aee97`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab9ea4faa68774f8dcfdb171efa8fc2b358380d5ba61fd2d2212d9ef7eef906`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7f6ba8a05e8752787341b7fe2a6a74810b06aa9fa70a1a0228f775cc695b037a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930d1c377ac04e3da986523b9e03970d9aff20f8036670f211d374ae5e6e562c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:04:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 02:04:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:04:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:04:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde4224141eb326416434e57e6985960fa0299c171636ec51c978d7483ded221`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 6.5 MB (6512130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39644797429280d1790a41b83be262964fe685b66a13098f85a2830ef136af23`  
		Last Modified: Tue, 07 Apr 2026 02:04:51 GMT  
		Size: 46.3 MB (46320009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a038716dc519bd0d53565ee9d170bb27389cee982f799ed02c5b30bb400da63b`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2857e0024941e8431e0d2e7288ff873bb60af2b99250a6c109fb700e616232c`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac7ccabd4f0e669d232e23f27536a4797faec571f1d5b385e8d37e9543ad1d4`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:d033ac4c98bc3deb3c46315bff42913e431c32321890ec7914cd6b43bf0a4454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a769173f691e7dbe1bbac685b1b6d2cf8af5e40c11a7536386e603ca5e558e45`

```dockerfile
```

-	Layers:
	-	`sha256:dff92a3ce28b58e918bb8a1b393141f0d15f0a7436d538d1b53bafdf3cd2f3f0`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29723eb32c4a4046b83b01b8e97bd5b93cfc334f24c3dcc9145d178038a36230`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a2a43c10363a3e5414039345eec8b6f29f095b8780f535d2bf8c345ecaccc9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81846058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2139c408fd9e94f3fd3b1367a24940cb005338e161818d060b054dac34b1bfdb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 01:50:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:50:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:50:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dbac72acd22aba48e1d3ad7b9a5e1cbeb7c0aebb12c6a591e18543bc5e15cc`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 7.7 MB (7696984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c262557b34cb3bc7ec83d26805b2652f905d6b967d83f8842bf504468e0a1838`  
		Last Modified: Tue, 07 Apr 2026 01:50:52 GMT  
		Size: 46.0 MB (46008449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74498ce48e4b91d1e7d88a9e0754b61258942627ce75895df3cb7db3c1b5c15`  
		Last Modified: Tue, 07 Apr 2026 01:50:50 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65c1e63d63625f49395f0638311d1e6c4f2c7a8305b76a623caebef010c4bc9`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b076129ef9a105123d5ba844cad634c503183088bbaf98f5207dd723da7a8f3`  
		Last Modified: Tue, 07 Apr 2026 01:50:52 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:2a6ed1d948d7f96ec2f4c78bacc10dff88e412f6fe98b8dbd8b836b5a352f7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f569ab759f8a5b6b8245d0f34e87a8b99fe51d28a3fc5a72fb47d21f8bec4d7d`

```dockerfile
```

-	Layers:
	-	`sha256:d88ff8ebd731cac72703f8bd7c6c93fbe8fe1d291c78a4810ec94e4c492d84cc`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d8afa3639be4d3d75ce8e3dc27463cae0a100a14b3761dab53339f975b1fc7`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9-alpine`

```console
$ docker pull chronograf@sha256:c73bbcdde515b06b9a7c553c92cc69c63197380e32554ac70bc487978d4f93e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f43a15493dfa286ecddb2a321f543ce0782328ace5a68abdb2f0a89fce86a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b149dbf0d54466603c75f2e0a21e5810e13c38a591a4994439fd92a43c9013c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 28 Jan 2026 02:55:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:25 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cc8374b20721167e978930acc3c96665f9488132a58677f6a81dad90f698`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 29.1 MB (29136848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b20d4daed0b72a4ba10efc2998799a5aa3a7b3da28d6057aff046b6d170da1`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a44a4a5cb211d460d00144b50703689629cd5cd3151aa8d989477af9fdddc9`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1870665d6b671bf68d872d353e6f3dcf8bb876176ebe068d36ebd72cc60f1a`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:206f2990c3926bcb3257f329fb9bde8aa579b6391b11966e1c6bcf9e465730b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f49329baac7667c2c41eaab7ec9b27b1f8b819d763c6975b1c546cc58ced7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8abfdf98ab51ee4676e152235fa5a48648b67d72067e3e04c029a7c821689679`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804bbf74bc55745b883375aede79021007da8c962a7342173f0a71dc7ff369e`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:ae8ef9f5aed5923d2e5b6fbaf029c4ac63cf2589e044675e1c4a97bab3b7d721
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
$ docker pull chronograf@sha256:391b07e02078dedb6bcc4da6a70772427e4563028730c3418d59b9be25c4191c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69252952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6719522bf411837ce4f257448a18b9d7ef8788d8d6780b324292d5f36a656a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:47:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:47:16 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 07 Apr 2026 01:47:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:47:16 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:47:16 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:47:16 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:47:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:47:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:47:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871deb3e1f9d29842f803bbb3b57565718e03fe7d95d6727e7b9bd7ebbbcc4cf`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 4.2 MB (4209084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83f53c9fbb2e651463cc46d40e4392f1dba8d9156a783e1dfdb44f2fd22920`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 34.8 MB (34761467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab805356815147ac532172c38b82ceba10acbcd9e7499353b3bf646aae03401`  
		Last Modified: Tue, 07 Apr 2026 01:47:25 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941abd100c9a87bec00b4d60f80f216fea5bce564b92cc5f57dc577020477d45`  
		Last Modified: Tue, 07 Apr 2026 01:47:25 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0d2c6d5a7d6cc8e56b0280a0339606c28256b81ce64bcf0bcd330d88e4f021`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:e1c8ad55a5cd054daf239d72d8b9dab284f8382e209ba98b3f2b9298ccbfde73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db02dfe5d3f4bccf082159b6d150326db16a263da1f58134b625c95d9e77c1`

```dockerfile
```

-	Layers:
	-	`sha256:ac0c770fa0902929698e0e1c6c3016c72f8bdbe9c52c6d0477ac8c8cd6b78157`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 3.1 MB (3057293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3057ee95435fd9b94ada60bb4c26f66d3d9795c1e910233b1c78555dcc92f47`  
		Last Modified: Tue, 07 Apr 2026 01:47:25 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:fb8903c255c2d41ec2ab6b0251b447a52e3408517c84d223568acb6434c94cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62206865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cb49d9e215b65253617a5de74e085996e28413821c42c41557a77e12e4a277`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:02:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 07 Apr 2026 02:02:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:02:57 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:02:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:02:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e68d06981293adfea04925ae38b70c2f51ed1a5e0d6b2de60d6bdd09f147afe`  
		Last Modified: Tue, 07 Apr 2026 00:59:07 GMT  
		Size: 25.6 MB (25551488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d56cd53bdc447d79b5c39958ffdd06ac4af9b9c5727910b7d2f36b66d40564`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 3.5 MB (3511492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dba245afcb1d30d696cfc700c6f959f3e7ba9b7bca33e70563a96b824c5fe`  
		Last Modified: Tue, 07 Apr 2026 02:03:07 GMT  
		Size: 33.1 MB (33119493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185b8e2de0c7ba8551af61d2d8ab39d92f21c6057b6e7c73a812397d1023702b`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1906d9e3cdb356fd4eb6ac57e8dd0a6f646f39f14c204a34749bc88b8051ac6e`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f42a9919899da8c1fa8f035d3803101388453c9c997dd37eb23fb3e5fe2b7a`  
		Last Modified: Tue, 07 Apr 2026 02:03:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:a0cd74bc8089bc15ae5d847c7faf1ddf161fe418cc3d9410d25e0b2ec7b1c40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3075375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7235040fdeb84e6e3e5bb48b62d09f726327ea6633a529c6bab9d3c29523573d`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9fb54df074c8743e364b4616abfdc5039997706de92b717efedc34fc16edb`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 3.1 MB (3059564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8fc4d9c91d29359b4199a2a84193b25f791e49c66825aa6df59e7d7db4342af`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:864f3893dfeab633bc7b58435a0efc783613dfd8d470e19d781b895413e55467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66240771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33d7f9036965e1483aaec1c762731f354a8bccd25eb3c85694827615c0cbafe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:50:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 07 Apr 2026 01:50:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:50:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:50:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7b9dfc611c6e2d719cd53f40a4a18e9c0fa04a5ed986a17a8cbd35e2786286`  
		Last Modified: Tue, 07 Apr 2026 01:50:34 GMT  
		Size: 4.2 MB (4210441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3bc8ed829284a93c3388a1c75eca96b60c9bc0b08b809310ba22abc29f067d`  
		Last Modified: Tue, 07 Apr 2026 01:50:35 GMT  
		Size: 33.3 MB (33261244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5fc05aacb87a7d1f6f3bc89a2d95c1f8feba8abbcba347a0f4f4c4b02eecc3`  
		Last Modified: Tue, 07 Apr 2026 01:50:33 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2024ed542d93a82b76c0556c6ec9cc7f1065e1754275a4aa8e9dfae182917`  
		Last Modified: Tue, 07 Apr 2026 01:50:34 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f4bfd97ddf8094a7534c20f7b74af671f0ce06735a1922a8d068a0fd3c4b14`  
		Last Modified: Tue, 07 Apr 2026 01:50:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:c186ae9ae6652db8939f7c43975599990f03de4ab50cc2dbaf1383f02ce97904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ca749b2320e39b657106a4521338b11db03a6d8a44f42d99db06cab53dba18`

```dockerfile
```

-	Layers:
	-	`sha256:e0aeb4d525ef26c669be9462766d6b2e8150351dc4750ceb709e05b4b056b656`  
		Last Modified: Tue, 07 Apr 2026 01:50:34 GMT  
		Size: 3.1 MB (3057542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2480230331860fc51efde1aadd42e9df98fbd1ccbf75b5a67abc3b3dd3781be1`  
		Last Modified: Tue, 07 Apr 2026 01:50:34 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:64bef3719ffd40e750e40a39da4c12abaa87dfb5feb5eda538abf94e3accb618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3f189f37cc38433df9fbac676c503a10acef7c7614624600135f250066886161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bec3fa8c5026e398c27b75bfa769e7655e34f7170bcdc9037dac726934f2ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 28 Jan 2026 02:53:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:53:40 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:53:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:53:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340aae68687d2116364c9e894fd45843e9743365d10615f35ce86ed559892f63`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 19.6 MB (19556564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c53db3e00d80e1eb53e2db543c42e48bbe8cedbd46305f512e93b6a97dca45`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dcdc4fbf054e697ef5ae3221a5d4fd5e2fdd105c6d4ff0de12003ee0b27b30`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda149c9eaf485c096f2594f2e965917ccbc4373f09c74334e243c6b695c21c`  
		Last Modified: Wed, 28 Jan 2026 02:53:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c56020b83aeb19cda9433c13248182ca3b3227bdfea0e3e87429fa828fce4e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f387fa3c690e841ea63c593cf9ab0ea8833159bbd96572eb1480d58af1824f1`

```dockerfile
```

-	Layers:
	-	`sha256:3952b13f0b8499685ee3fd998a70ea826c97a65c6f328d3185fff832bf3bfd8a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7be3070420c927548a22fb90dc77dcced4eaf6f13c2cb97512b1fbff884e9e`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:ae8ef9f5aed5923d2e5b6fbaf029c4ac63cf2589e044675e1c4a97bab3b7d721
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
$ docker pull chronograf@sha256:391b07e02078dedb6bcc4da6a70772427e4563028730c3418d59b9be25c4191c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69252952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6719522bf411837ce4f257448a18b9d7ef8788d8d6780b324292d5f36a656a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:47:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:47:16 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 07 Apr 2026 01:47:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:47:16 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:47:16 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:47:16 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:47:16 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:47:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:47:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871deb3e1f9d29842f803bbb3b57565718e03fe7d95d6727e7b9bd7ebbbcc4cf`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 4.2 MB (4209084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83f53c9fbb2e651463cc46d40e4392f1dba8d9156a783e1dfdb44f2fd22920`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 34.8 MB (34761467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab805356815147ac532172c38b82ceba10acbcd9e7499353b3bf646aae03401`  
		Last Modified: Tue, 07 Apr 2026 01:47:25 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941abd100c9a87bec00b4d60f80f216fea5bce564b92cc5f57dc577020477d45`  
		Last Modified: Tue, 07 Apr 2026 01:47:25 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0d2c6d5a7d6cc8e56b0280a0339606c28256b81ce64bcf0bcd330d88e4f021`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:e1c8ad55a5cd054daf239d72d8b9dab284f8382e209ba98b3f2b9298ccbfde73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82db02dfe5d3f4bccf082159b6d150326db16a263da1f58134b625c95d9e77c1`

```dockerfile
```

-	Layers:
	-	`sha256:ac0c770fa0902929698e0e1c6c3016c72f8bdbe9c52c6d0477ac8c8cd6b78157`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 3.1 MB (3057293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3057ee95435fd9b94ada60bb4c26f66d3d9795c1e910233b1c78555dcc92f47`  
		Last Modified: Tue, 07 Apr 2026 01:47:25 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:fb8903c255c2d41ec2ab6b0251b447a52e3408517c84d223568acb6434c94cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62206865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cb49d9e215b65253617a5de74e085996e28413821c42c41557a77e12e4a277`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:02:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 07 Apr 2026 02:02:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:02:57 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:02:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:02:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e68d06981293adfea04925ae38b70c2f51ed1a5e0d6b2de60d6bdd09f147afe`  
		Last Modified: Tue, 07 Apr 2026 00:59:07 GMT  
		Size: 25.6 MB (25551488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d56cd53bdc447d79b5c39958ffdd06ac4af9b9c5727910b7d2f36b66d40564`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 3.5 MB (3511492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67dba245afcb1d30d696cfc700c6f959f3e7ba9b7bca33e70563a96b824c5fe`  
		Last Modified: Tue, 07 Apr 2026 02:03:07 GMT  
		Size: 33.1 MB (33119493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185b8e2de0c7ba8551af61d2d8ab39d92f21c6057b6e7c73a812397d1023702b`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1906d9e3cdb356fd4eb6ac57e8dd0a6f646f39f14c204a34749bc88b8051ac6e`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f42a9919899da8c1fa8f035d3803101388453c9c997dd37eb23fb3e5fe2b7a`  
		Last Modified: Tue, 07 Apr 2026 02:03:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:a0cd74bc8089bc15ae5d847c7faf1ddf161fe418cc3d9410d25e0b2ec7b1c40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3075375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7235040fdeb84e6e3e5bb48b62d09f726327ea6633a529c6bab9d3c29523573d`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9fb54df074c8743e364b4616abfdc5039997706de92b717efedc34fc16edb`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 3.1 MB (3059564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8fc4d9c91d29359b4199a2a84193b25f791e49c66825aa6df59e7d7db4342af`  
		Last Modified: Tue, 07 Apr 2026 02:03:06 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:864f3893dfeab633bc7b58435a0efc783613dfd8d470e19d781b895413e55467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66240771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33d7f9036965e1483aaec1c762731f354a8bccd25eb3c85694827615c0cbafe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:50:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 07 Apr 2026 01:50:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:50:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:50:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:50:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7b9dfc611c6e2d719cd53f40a4a18e9c0fa04a5ed986a17a8cbd35e2786286`  
		Last Modified: Tue, 07 Apr 2026 01:50:34 GMT  
		Size: 4.2 MB (4210441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3bc8ed829284a93c3388a1c75eca96b60c9bc0b08b809310ba22abc29f067d`  
		Last Modified: Tue, 07 Apr 2026 01:50:35 GMT  
		Size: 33.3 MB (33261244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5fc05aacb87a7d1f6f3bc89a2d95c1f8feba8abbcba347a0f4f4c4b02eecc3`  
		Last Modified: Tue, 07 Apr 2026 01:50:33 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2024ed542d93a82b76c0556c6ec9cc7f1065e1754275a4aa8e9dfae182917`  
		Last Modified: Tue, 07 Apr 2026 01:50:34 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f4bfd97ddf8094a7534c20f7b74af671f0ce06735a1922a8d068a0fd3c4b14`  
		Last Modified: Tue, 07 Apr 2026 01:50:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:c186ae9ae6652db8939f7c43975599990f03de4ab50cc2dbaf1383f02ce97904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ca749b2320e39b657106a4521338b11db03a6d8a44f42d99db06cab53dba18`

```dockerfile
```

-	Layers:
	-	`sha256:e0aeb4d525ef26c669be9462766d6b2e8150351dc4750ceb709e05b4b056b656`  
		Last Modified: Tue, 07 Apr 2026 01:50:34 GMT  
		Size: 3.1 MB (3057542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2480230331860fc51efde1aadd42e9df98fbd1ccbf75b5a67abc3b3dd3781be1`  
		Last Modified: Tue, 07 Apr 2026 01:50:34 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:64bef3719ffd40e750e40a39da4c12abaa87dfb5feb5eda538abf94e3accb618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3f189f37cc38433df9fbac676c503a10acef7c7614624600135f250066886161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bec3fa8c5026e398c27b75bfa769e7655e34f7170bcdc9037dac726934f2ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Wed, 28 Jan 2026 02:53:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:53:40 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:53:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:53:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:53:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340aae68687d2116364c9e894fd45843e9743365d10615f35ce86ed559892f63`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 19.6 MB (19556564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c53db3e00d80e1eb53e2db543c42e48bbe8cedbd46305f512e93b6a97dca45`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dcdc4fbf054e697ef5ae3221a5d4fd5e2fdd105c6d4ff0de12003ee0b27b30`  
		Last Modified: Wed, 28 Jan 2026 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda149c9eaf485c096f2594f2e965917ccbc4373f09c74334e243c6b695c21c`  
		Last Modified: Wed, 28 Jan 2026 02:53:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c56020b83aeb19cda9433c13248182ca3b3227bdfea0e3e87429fa828fce4e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f387fa3c690e841ea63c593cf9ab0ea8833159bbd96572eb1480d58af1824f1`

```dockerfile
```

-	Layers:
	-	`sha256:3952b13f0b8499685ee3fd998a70ea826c97a65c6f328d3185fff832bf3bfd8a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7be3070420c927548a22fb90dc77dcced4eaf6f13c2cb97512b1fbff884e9e`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:ef1a205168124ee1f6e3366a152c7a0c2498bff44fe9a799a0ef9e10b6c40875
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
$ docker pull chronograf@sha256:ebf15dc1c47a7fbf511cc108a566e170dfb7491f9ac45b8dca3e87e946752254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01997a70424752df1063806031c90ee31a1fdec42e00462b6aed8893e9bac687`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:47:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 07 Apr 2026 01:47:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:47:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:47:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ef82096a3a11dbabb1675ced3808f8da24808d1a56a1b2a43fdc78b081f06`  
		Last Modified: Tue, 07 Apr 2026 01:47:27 GMT  
		Size: 5.2 MB (5241731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ed007d97d961cf222be53168e91e0a2ca92e18a908b477a29041238882a34`  
		Last Modified: Tue, 07 Apr 2026 01:47:27 GMT  
		Size: 34.4 MB (34364324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a193596ed6e8455f326a53955438eeba9481cd427e2fef9f2a07f0a9267923b6`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec4ac30a31bcae9fc987a2429da3b2f867f7ea66041e75fb194c382da9af0b5`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db8f3707a710d3de3ac7179db9bb2adeca1a740fa3331432ee5c017c63102a9`  
		Last Modified: Tue, 07 Apr 2026 01:47:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:007b0ae7988aeba55d479e859fb7b9aacbb91a8b2c2b28cd8d02c5bd971e27fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda79e554f50d250155d1107eb3431f9cd404d1f1ccb5de06bc0a0565ec7b52c`

```dockerfile
```

-	Layers:
	-	`sha256:8d429c50b22e6a18ac15c637504b8b255ab97a00ba3c4cc7158d6dcb13626718`  
		Last Modified: Tue, 07 Apr 2026 01:47:27 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cb184502e533319580bdbc5b15faad13db611c6cd93719c724f0a0ab072dc4`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d91c66ec024d1df53eb188f2a10a148a49d072ad660203cfa30733f8ae010b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026644320adde1cd20ae029fa679953f5fa87a1df76a7285cf2e835089b75635`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:03:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 07 Apr 2026 02:03:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:03:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:03:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:03:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e68d06981293adfea04925ae38b70c2f51ed1a5e0d6b2de60d6bdd09f147afe`  
		Last Modified: Tue, 07 Apr 2026 00:59:07 GMT  
		Size: 25.6 MB (25551488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd47cf0d62602ce6360958bce3bd1e3fba112ed1c5c906bda15a06633b277e6`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 4.5 MB (4510062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958f2ff5a2882f6586ade61736106589120c3b2b7522fb0bbf665cefe6fb591c`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 32.5 MB (32534959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2148ef088edec6dc5c95379dc33749dae15a71786a8e82016d98d531d1c1a01c`  
		Last Modified: Tue, 07 Apr 2026 02:03:21 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721fd15a1cc7c612dda7365bbb0ba9343b9c0b3ae9a695fc71c55984df5e95d`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f479e93a9f877e41c4292b0114ddb0abb9292717a9745959780b834123b148c`  
		Last Modified: Tue, 07 Apr 2026 02:03:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:8966599d584fb737f0e487492378ed3cb4a3c2531a70ef6e2a140b62866a429f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce278b41217333594cb1d4f6eabbbde3075e99a1172659f9c9f1fc37efb05be`

```dockerfile
```

-	Layers:
	-	`sha256:4565dab85324c04263b921c8fc215e72ae4daae431d95f08068dc9ba7e048bd1`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2765ca1e01c86f5b3d699d78ced9a680aa7677c69e75c8ad3517a169fb3ead`  
		Last Modified: Tue, 07 Apr 2026 02:03:21 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f2906698b1d02c9200a1f9718f0ab14fd05c7d521e8d2f1638c26a675ccfd643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66428390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed0ee57daeaf623e53a336ef731ae6d0b05d5b2ff3aa421eab83683cc770e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:50:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 07 Apr 2026 01:50:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:50:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:50:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668c9ee3a5435ddd9c857db63cbf0a60ff1a26b9dfb6a0f620ccfa7d7f9d217`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 5.2 MB (5229744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dc31ba51b7d7e5d337224aeb89dd0e5bd79d29ae039480f9a454de7cedfcf5`  
		Last Modified: Tue, 07 Apr 2026 01:50:44 GMT  
		Size: 32.4 MB (32429556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6c8323e308cc6994c60fa749b29b4455a25606e4d819e9d2a57d636caf626e`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b771cb97f4d828830d21fdb47b82713f216b9b496228cee0bfd0cd97e41a68a`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55a66452a94303eae2a909c00d76f712c8cf74bb6b35f0106d963e0d89eac5`  
		Last Modified: Tue, 07 Apr 2026 01:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:a7a7537e90fa81b8e8a639f4a3b75c466742e25246083b40e617014f970d0a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9079c60736416868d23e09857a11ea23c6771318eafcb3220fd4180cfe38772`

```dockerfile
```

-	Layers:
	-	`sha256:145f5b728764f25813ffc9b2cf7e2a2cf2471136dc75c79db7c58bec1d4ad810`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f4be7877824c4081443a2b5f5d153b91ccdd4162e8ad9ecae43822d8b0cb004`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:eaa3bb3ccb8ee814154bf133b1f66211d509c29f6dd1e1526c10230e208b863c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c2bf30f869435c0b92e73e5d840baecf10b7556dee1180eab812a2e5c64ee8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f2dae78c59d8c5be31f4f138985d18bd1ba2aeb87bccc37c803d766d4dfb56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:54:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 28 Jan 2026 02:54:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:54:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:54:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11511055c1a92ee4826f4450c606b4c6fe01663551c2520901ee8904c7cc029e`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e7cced7996c2c54d3705c37d6189dd45203311e86f379e19dac56c87d79c1`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 290.8 KB (290775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85e7552262500b34023157ef8b78d59c9f8aecf673d089df4240d9c9410eaf`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 19.2 MB (19204012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f59d04c053bed8109181709b7b72268373c858113d4d325f91a61c9860fe15`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39810aef4e0fd17cd3dd3a5c3df656a78821f4433c31d84d22a70687f39fc8`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39803bc8b4320a837d54074da9cd5a373b5492fbb69ba833e15e82cb22d38c2e`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:8db07f0161f7cd63e13b7a8ec9f585002560d6c1aeb6bf3bfe117e6023c60030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f169dc8bb776368bcf6aeabb508e8f02347ed3c83e3ce9438f29a553783f718`

```dockerfile
```

-	Layers:
	-	`sha256:2a4f2a2d49e087fc0c9683afc43c5a8338ed6ca288ed80700190e6600854103b`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94417dbea42e77a238ff18ac37fde210a7fb42d1a5ba372bd1e9e6e02f0e3f2d`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:ef1a205168124ee1f6e3366a152c7a0c2498bff44fe9a799a0ef9e10b6c40875
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
$ docker pull chronograf@sha256:ebf15dc1c47a7fbf511cc108a566e170dfb7491f9ac45b8dca3e87e946752254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01997a70424752df1063806031c90ee31a1fdec42e00462b6aed8893e9bac687`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:47:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 07 Apr 2026 01:47:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:47:18 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:47:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:47:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ef82096a3a11dbabb1675ced3808f8da24808d1a56a1b2a43fdc78b081f06`  
		Last Modified: Tue, 07 Apr 2026 01:47:27 GMT  
		Size: 5.2 MB (5241731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ed007d97d961cf222be53168e91e0a2ca92e18a908b477a29041238882a34`  
		Last Modified: Tue, 07 Apr 2026 01:47:27 GMT  
		Size: 34.4 MB (34364324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a193596ed6e8455f326a53955438eeba9481cd427e2fef9f2a07f0a9267923b6`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec4ac30a31bcae9fc987a2429da3b2f867f7ea66041e75fb194c382da9af0b5`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db8f3707a710d3de3ac7179db9bb2adeca1a740fa3331432ee5c017c63102a9`  
		Last Modified: Tue, 07 Apr 2026 01:47:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:007b0ae7988aeba55d479e859fb7b9aacbb91a8b2c2b28cd8d02c5bd971e27fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda79e554f50d250155d1107eb3431f9cd404d1f1ccb5de06bc0a0565ec7b52c`

```dockerfile
```

-	Layers:
	-	`sha256:8d429c50b22e6a18ac15c637504b8b255ab97a00ba3c4cc7158d6dcb13626718`  
		Last Modified: Tue, 07 Apr 2026 01:47:27 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cb184502e533319580bdbc5b15faad13db611c6cd93719c724f0a0ab072dc4`  
		Last Modified: Tue, 07 Apr 2026 01:47:26 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d91c66ec024d1df53eb188f2a10a148a49d072ad660203cfa30733f8ae010b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026644320adde1cd20ae029fa679953f5fa87a1df76a7285cf2e835089b75635`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:03:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 07 Apr 2026 02:03:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:03:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:03:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:03:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:03:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e68d06981293adfea04925ae38b70c2f51ed1a5e0d6b2de60d6bdd09f147afe`  
		Last Modified: Tue, 07 Apr 2026 00:59:07 GMT  
		Size: 25.6 MB (25551488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd47cf0d62602ce6360958bce3bd1e3fba112ed1c5c906bda15a06633b277e6`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 4.5 MB (4510062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958f2ff5a2882f6586ade61736106589120c3b2b7522fb0bbf665cefe6fb591c`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 32.5 MB (32534959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2148ef088edec6dc5c95379dc33749dae15a71786a8e82016d98d531d1c1a01c`  
		Last Modified: Tue, 07 Apr 2026 02:03:21 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721fd15a1cc7c612dda7365bbb0ba9343b9c0b3ae9a695fc71c55984df5e95d`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f479e93a9f877e41c4292b0114ddb0abb9292717a9745959780b834123b148c`  
		Last Modified: Tue, 07 Apr 2026 02:03:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:8966599d584fb737f0e487492378ed3cb4a3c2531a70ef6e2a140b62866a429f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce278b41217333594cb1d4f6eabbbde3075e99a1172659f9c9f1fc37efb05be`

```dockerfile
```

-	Layers:
	-	`sha256:4565dab85324c04263b921c8fc215e72ae4daae431d95f08068dc9ba7e048bd1`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2765ca1e01c86f5b3d699d78ced9a680aa7677c69e75c8ad3517a169fb3ead`  
		Last Modified: Tue, 07 Apr 2026 02:03:21 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f2906698b1d02c9200a1f9718f0ab14fd05c7d521e8d2f1638c26a675ccfd643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66428390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed0ee57daeaf623e53a336ef731ae6d0b05d5b2ff3aa421eab83683cc770e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:50:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 07 Apr 2026 01:50:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:50:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:50:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:50:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668c9ee3a5435ddd9c857db63cbf0a60ff1a26b9dfb6a0f620ccfa7d7f9d217`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 5.2 MB (5229744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dc31ba51b7d7e5d337224aeb89dd0e5bd79d29ae039480f9a454de7cedfcf5`  
		Last Modified: Tue, 07 Apr 2026 01:50:44 GMT  
		Size: 32.4 MB (32429556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6c8323e308cc6994c60fa749b29b4455a25606e4d819e9d2a57d636caf626e`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b771cb97f4d828830d21fdb47b82713f216b9b496228cee0bfd0cd97e41a68a`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55a66452a94303eae2a909c00d76f712c8cf74bb6b35f0106d963e0d89eac5`  
		Last Modified: Tue, 07 Apr 2026 01:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:a7a7537e90fa81b8e8a639f4a3b75c466742e25246083b40e617014f970d0a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9079c60736416868d23e09857a11ea23c6771318eafcb3220fd4180cfe38772`

```dockerfile
```

-	Layers:
	-	`sha256:145f5b728764f25813ffc9b2cf7e2a2cf2471136dc75c79db7c58bec1d4ad810`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f4be7877824c4081443a2b5f5d153b91ccdd4162e8ad9ecae43822d8b0cb004`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:eaa3bb3ccb8ee814154bf133b1f66211d509c29f6dd1e1526c10230e208b863c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c2bf30f869435c0b92e73e5d840baecf10b7556dee1180eab812a2e5c64ee8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f2dae78c59d8c5be31f4f138985d18bd1ba2aeb87bccc37c803d766d4dfb56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:54:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 28 Jan 2026 02:54:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:54:18 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:54:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11511055c1a92ee4826f4450c606b4c6fe01663551c2520901ee8904c7cc029e`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e7cced7996c2c54d3705c37d6189dd45203311e86f379e19dac56c87d79c1`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 290.8 KB (290775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e85e7552262500b34023157ef8b78d59c9f8aecf673d089df4240d9c9410eaf`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 19.2 MB (19204012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f59d04c053bed8109181709b7b72268373c858113d4d325f91a61c9860fe15`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39810aef4e0fd17cd3dd3a5c3df656a78821f4433c31d84d22a70687f39fc8`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39803bc8b4320a837d54074da9cd5a373b5492fbb69ba833e15e82cb22d38c2e`  
		Last Modified: Wed, 28 Jan 2026 02:54:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:8db07f0161f7cd63e13b7a8ec9f585002560d6c1aeb6bf3bfe117e6023c60030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f169dc8bb776368bcf6aeabb508e8f02347ed3c83e3ce9438f29a553783f718`

```dockerfile
```

-	Layers:
	-	`sha256:2a4f2a2d49e087fc0c9683afc43c5a8338ed6ca288ed80700190e6600854103b`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94417dbea42e77a238ff18ac37fde210a7fb42d1a5ba372bd1e9e6e02f0e3f2d`  
		Last Modified: Wed, 28 Jan 2026 02:54:26 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:4f69762386637ee1e695abf8a3f1ad40a8f341128eb27bef4485f1049ec7a638
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
$ docker pull chronograf@sha256:e884383631d2475e536f3c7315f685da45dc3baaa471e918278ee81e3a3d60c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd2299e43c279f9236dc7e1dc029719d2ac4d082d231dceda5da4506640b151`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:47:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 07 Apr 2026 01:47:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:47:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:47:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80945ad94fa2bffbf5d7feb198b74305b08c511ef1e4f616756f410c6a2e4bac`  
		Last Modified: Tue, 07 Apr 2026 01:47:30 GMT  
		Size: 5.2 MB (5241691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff92eeb0a4d1c786b9b2999dadbf32283de3d4d53892212f0ca63fc94b5b2821`  
		Last Modified: Tue, 07 Apr 2026 01:47:31 GMT  
		Size: 35.0 MB (35011766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427d2a37cf387d02670c2697dde9328d47f5ece42ca96d566d10b5e04556f0ee`  
		Last Modified: Tue, 07 Apr 2026 01:47:29 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce40be3d23b38ac4748fe7d3a2ba117d02496251970121ff1473f15c835c3d27`  
		Last Modified: Tue, 07 Apr 2026 01:47:30 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d064df8b1f7034f21267bcad8f15c4ba872ce8b71261657bee28cbf2b5f34baf`  
		Last Modified: Tue, 07 Apr 2026 01:47:31 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:1eb31c6ad77c55153a8b303d996dfe53f2732cf8d80fbfe6e1a22b0c813a7f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906400df881d240fd29f3679a8d5094c48fd1e1810eeb66375ca400a4489f389`

```dockerfile
```

-	Layers:
	-	`sha256:519618fa7b0389c2701e4953d8c1feeefdbdc9cdbae784c676be3e5aa35d030f`  
		Last Modified: Tue, 07 Apr 2026 01:47:30 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51a0e8be354be28fab4a0396e29537df849a5a3089855e3c3b1d5915a0ba573`  
		Last Modified: Tue, 07 Apr 2026 01:47:29 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5be9b42d24eb10e051edc9ac1e58b9809c5f3fc0fc2a4fb023b32c364b4d816e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63397562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922484efddf50b711665b75e2678e5e51ebffc4adc76ba8527d9fa2986df3312`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:03:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 07 Apr 2026 02:03:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:03:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:03:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:03:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e68d06981293adfea04925ae38b70c2f51ed1a5e0d6b2de60d6bdd09f147afe`  
		Last Modified: Tue, 07 Apr 2026 00:59:07 GMT  
		Size: 25.6 MB (25551488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd47cf0d62602ce6360958bce3bd1e3fba112ed1c5c906bda15a06633b277e6`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 4.5 MB (4510062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d35bc51410e08b454b515ba8057d451a307007a28d18617c35f9b7de8ec37`  
		Last Modified: Tue, 07 Apr 2026 02:03:44 GMT  
		Size: 33.3 MB (33311631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a53b50e2a0674121596b70d5f7a40860db2e20f93463361dec3908d849a9e4`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9065979c58d9cf8aa69c4721c0a6f7ef810f4ae1ceafbbdf0e5536a1fc05eeb0`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03308cf9df4727cccc14addef58fb2510db67f43ec7ba8450ea758a5c30eddc`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:2d574ec8f794f2d0b33d44ff313a8c19e879a094990106e4aec0b2d91179b0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb66cab43022e04921b9fd4ab6aa7b0c6d3a6dd67d1d3c459b4d30744c21766`

```dockerfile
```

-	Layers:
	-	`sha256:f8404b68b655b82ab3d9aeb7fd7efdc63c2abcd7e603bf00b08428d196010ffb`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4808103cd6087c6c1c39538f3712ed925395a0a319201a9f3c3ce2f7705eef4d`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 15.8 KB (15843 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:03f6cd058f1c0620e2d4f4e2c754930b8133108a140f986afcb7a1d66ee97913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67181278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70023f0bdda71cbebcce64489165cfdca72282ee2bcb3270e4096261ff076869`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:50:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 07 Apr 2026 01:50:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:50:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:50:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73dbf6f566220bce016b1867f50e5f48108164353244ac579d49cb056fafe52`  
		Last Modified: Tue, 07 Apr 2026 01:50:46 GMT  
		Size: 5.2 MB (5229830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddf67bdfd00bc8962c77d403f2d039f693fa8b5648eeee38f938ea0d16aaf45`  
		Last Modified: Tue, 07 Apr 2026 01:50:46 GMT  
		Size: 33.2 MB (33182362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074e632fc5d9a1cbf23d2bfb0f30c034f4a7ecb9b528cfb5729e037ecb115f18`  
		Last Modified: Tue, 07 Apr 2026 01:50:45 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df145ff6ca5e89f312df0fac67ee8146db694ff734d9f25dbaeb35affe73f4`  
		Last Modified: Tue, 07 Apr 2026 01:50:45 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55a66452a94303eae2a909c00d76f712c8cf74bb6b35f0106d963e0d89eac5`  
		Last Modified: Tue, 07 Apr 2026 01:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:34f69751af9c037d44a78a022ca0baad6a993c4d2d3ade7d8a174b6b5457c9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c25d776f86d96510b6592e402901ad757f0482a312cc4f76ecadfe55e169205`

```dockerfile
```

-	Layers:
	-	`sha256:f59745eb7f24c46717139e4b9daeeb9542ac880039c80ef39251bf3e031e5f38`  
		Last Modified: Tue, 07 Apr 2026 01:50:46 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2689826ba0c443e39259df6f202e3d8dbf70e40596ae8a8889cd144037d6dd50`  
		Last Modified: Tue, 07 Apr 2026 01:50:45 GMT  
		Size: 15.9 KB (15861 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:fe4e3b3c10a641ad805b9ce0ec78cda2f470f49a830894c722953c8fb728fcb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:67cedab187e8fc183d786cf2258d4005ec583930cc20e74da6812a9e7ff42a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23615399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f6aa3073f13adbf88c9cccbd9ab0fbb58be572d0f96c9e48d3d49e2b1b015`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:00 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 28 Jan 2026 02:55:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:01 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49502ea6fb236afee58c16f44002da47fa15e3106a666c8b493bb26052c9274a`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 19.7 MB (19672093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21543e57ca18bdf7a24a618747db1a314a907889b35e10bf5d53278ef3419640`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feac25ca50f9519d41319a760291be5f082cfa992b201b65d9f8ce0852c6735c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579664805c4fdab94b0811a476f26cd0ce412bc8c0c5a0bab5ecbdba4b190a7d`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4b3df4976cd08554c6148388fc472cd29690db4573063bd6d7675893a2756bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af162ec484f5c5e51d9958dc581b210cf6055821574b4630fdb8d5c27c93cd1f`

```dockerfile
```

-	Layers:
	-	`sha256:e1fda32b72505ea72431129c688691bca18d6a71dfc54ac36b83c1657128e64c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8be116a02c551af1fa72b7f056c9711e39f115b000563402cba9f992d61ff`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:4f69762386637ee1e695abf8a3f1ad40a8f341128eb27bef4485f1049ec7a638
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
$ docker pull chronograf@sha256:e884383631d2475e536f3c7315f685da45dc3baaa471e918278ee81e3a3d60c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd2299e43c279f9236dc7e1dc029719d2ac4d082d231dceda5da4506640b151`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:47:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 07 Apr 2026 01:47:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:47:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:47:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80945ad94fa2bffbf5d7feb198b74305b08c511ef1e4f616756f410c6a2e4bac`  
		Last Modified: Tue, 07 Apr 2026 01:47:30 GMT  
		Size: 5.2 MB (5241691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff92eeb0a4d1c786b9b2999dadbf32283de3d4d53892212f0ca63fc94b5b2821`  
		Last Modified: Tue, 07 Apr 2026 01:47:31 GMT  
		Size: 35.0 MB (35011766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427d2a37cf387d02670c2697dde9328d47f5ece42ca96d566d10b5e04556f0ee`  
		Last Modified: Tue, 07 Apr 2026 01:47:29 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce40be3d23b38ac4748fe7d3a2ba117d02496251970121ff1473f15c835c3d27`  
		Last Modified: Tue, 07 Apr 2026 01:47:30 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d064df8b1f7034f21267bcad8f15c4ba872ce8b71261657bee28cbf2b5f34baf`  
		Last Modified: Tue, 07 Apr 2026 01:47:31 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:1eb31c6ad77c55153a8b303d996dfe53f2732cf8d80fbfe6e1a22b0c813a7f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906400df881d240fd29f3679a8d5094c48fd1e1810eeb66375ca400a4489f389`

```dockerfile
```

-	Layers:
	-	`sha256:519618fa7b0389c2701e4953d8c1feeefdbdc9cdbae784c676be3e5aa35d030f`  
		Last Modified: Tue, 07 Apr 2026 01:47:30 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51a0e8be354be28fab4a0396e29537df849a5a3089855e3c3b1d5915a0ba573`  
		Last Modified: Tue, 07 Apr 2026 01:47:29 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5be9b42d24eb10e051edc9ac1e58b9809c5f3fc0fc2a4fb023b32c364b4d816e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63397562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922484efddf50b711665b75e2678e5e51ebffc4adc76ba8527d9fa2986df3312`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:03:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 07 Apr 2026 02:03:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:03:34 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:03:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:03:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:03:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e68d06981293adfea04925ae38b70c2f51ed1a5e0d6b2de60d6bdd09f147afe`  
		Last Modified: Tue, 07 Apr 2026 00:59:07 GMT  
		Size: 25.6 MB (25551488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd47cf0d62602ce6360958bce3bd1e3fba112ed1c5c906bda15a06633b277e6`  
		Last Modified: Tue, 07 Apr 2026 02:03:22 GMT  
		Size: 4.5 MB (4510062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d35bc51410e08b454b515ba8057d451a307007a28d18617c35f9b7de8ec37`  
		Last Modified: Tue, 07 Apr 2026 02:03:44 GMT  
		Size: 33.3 MB (33311631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a53b50e2a0674121596b70d5f7a40860db2e20f93463361dec3908d849a9e4`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9065979c58d9cf8aa69c4721c0a6f7ef810f4ae1ceafbbdf0e5536a1fc05eeb0`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03308cf9df4727cccc14addef58fb2510db67f43ec7ba8450ea758a5c30eddc`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:2d574ec8f794f2d0b33d44ff313a8c19e879a094990106e4aec0b2d91179b0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb66cab43022e04921b9fd4ab6aa7b0c6d3a6dd67d1d3c459b4d30744c21766`

```dockerfile
```

-	Layers:
	-	`sha256:f8404b68b655b82ab3d9aeb7fd7efdc63c2abcd7e603bf00b08428d196010ffb`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4808103cd6087c6c1c39538f3712ed925395a0a319201a9f3c3ce2f7705eef4d`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 15.8 KB (15843 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:03f6cd058f1c0620e2d4f4e2c754930b8133108a140f986afcb7a1d66ee97913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67181278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70023f0bdda71cbebcce64489165cfdca72282ee2bcb3270e4096261ff076869`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:50:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 07 Apr 2026 01:50:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:50:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:50:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:50:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73dbf6f566220bce016b1867f50e5f48108164353244ac579d49cb056fafe52`  
		Last Modified: Tue, 07 Apr 2026 01:50:46 GMT  
		Size: 5.2 MB (5229830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddf67bdfd00bc8962c77d403f2d039f693fa8b5648eeee38f938ea0d16aaf45`  
		Last Modified: Tue, 07 Apr 2026 01:50:46 GMT  
		Size: 33.2 MB (33182362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074e632fc5d9a1cbf23d2bfb0f30c034f4a7ecb9b528cfb5729e037ecb115f18`  
		Last Modified: Tue, 07 Apr 2026 01:50:45 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df145ff6ca5e89f312df0fac67ee8146db694ff734d9f25dbaeb35affe73f4`  
		Last Modified: Tue, 07 Apr 2026 01:50:45 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55a66452a94303eae2a909c00d76f712c8cf74bb6b35f0106d963e0d89eac5`  
		Last Modified: Tue, 07 Apr 2026 01:50:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:34f69751af9c037d44a78a022ca0baad6a993c4d2d3ade7d8a174b6b5457c9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c25d776f86d96510b6592e402901ad757f0482a312cc4f76ecadfe55e169205`

```dockerfile
```

-	Layers:
	-	`sha256:f59745eb7f24c46717139e4b9daeeb9542ac880039c80ef39251bf3e031e5f38`  
		Last Modified: Tue, 07 Apr 2026 01:50:46 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2689826ba0c443e39259df6f202e3d8dbf70e40596ae8a8889cd144037d6dd50`  
		Last Modified: Tue, 07 Apr 2026 01:50:45 GMT  
		Size: 15.9 KB (15861 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:fe4e3b3c10a641ad805b9ce0ec78cda2f470f49a830894c722953c8fb728fcb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:67cedab187e8fc183d786cf2258d4005ec583930cc20e74da6812a9e7ff42a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23615399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f6aa3073f13adbf88c9cccbd9ab0fbb58be572d0f96c9e48d3d49e2b1b015`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:53:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:53:36 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:00 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 28 Jan 2026 02:55:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:01 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b2964cc34286517fc6db4e61099dfdb5bb50b2c809f99bbe92d3490150811a`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abab41c57d391adf860ba3c6dc3cf0f0d1735950f94293661caa634ed79a539`  
		Last Modified: Wed, 28 Jan 2026 02:53:47 GMT  
		Size: 290.8 KB (290786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49502ea6fb236afee58c16f44002da47fa15e3106a666c8b493bb26052c9274a`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 19.7 MB (19672093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21543e57ca18bdf7a24a618747db1a314a907889b35e10bf5d53278ef3419640`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feac25ca50f9519d41319a760291be5f082cfa992b201b65d9f8ce0852c6735c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579664805c4fdab94b0811a476f26cd0ce412bc8c0c5a0bab5ecbdba4b190a7d`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4b3df4976cd08554c6148388fc472cd29690db4573063bd6d7675893a2756bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 KB (250419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af162ec484f5c5e51d9958dc581b210cf6055821574b4630fdb8d5c27c93cd1f`

```dockerfile
```

-	Layers:
	-	`sha256:e1fda32b72505ea72431129c688691bca18d6a71dfc54ac36b83c1657128e64c`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd8be116a02c551af1fa72b7f056c9711e39f115b000563402cba9f992d61ff`  
		Last Modified: Wed, 28 Jan 2026 02:55:08 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:c73bbcdde515b06b9a7c553c92cc69c63197380e32554ac70bc487978d4f93e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f43a15493dfa286ecddb2a321f543ce0782328ace5a68abdb2f0a89fce86a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b149dbf0d54466603c75f2e0a21e5810e13c38a591a4994439fd92a43c9013c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 28 Jan 2026 02:55:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 28 Jan 2026 02:55:25 GMT
VOLUME [/var/lib/chronograf]
# Wed, 28 Jan 2026 02:55:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 02:55:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 02:55:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cc8374b20721167e978930acc3c96665f9488132a58677f6a81dad90f698`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 29.1 MB (29136848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b20d4daed0b72a4ba10efc2998799a5aa3a7b3da28d6057aff046b6d170da1`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a44a4a5cb211d460d00144b50703689629cd5cd3151aa8d989477af9fdddc9`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1870665d6b671bf68d872d353e6f3dcf8bb876176ebe068d36ebd72cc60f1a`  
		Last Modified: Wed, 28 Jan 2026 02:55:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:206f2990c3926bcb3257f329fb9bde8aa579b6391b11966e1c6bcf9e465730b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 KB (269841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f49329baac7667c2c41eaab7ec9b27b1f8b819d763c6975b1c546cc58ced7f8`

```dockerfile
```

-	Layers:
	-	`sha256:8abfdf98ab51ee4676e152235fa5a48648b67d72067e3e04c029a7c821689679`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 252.0 KB (252029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c804bbf74bc55745b883375aede79021007da8c962a7342173f0a71dc7ff369e`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 17.8 KB (17812 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:47c5576b66fff1426392ca99f67a29b4e7caecc6daa45cfd7a04e3c901ecd499
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
$ docker pull chronograf@sha256:cf3807fb3b6d5e1a167f2c40fc9735ce9b811b79c6f931e125dae995f9c72267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85008414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319eebf3949a35c9433ffb5568b5bcddcff17c2d10a6db22ca0231d615a4e2bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:47:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 01:47:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:47:25 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:47:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55699494e05bd69b9c319828f65a040b15238883abbb8aa8e051f3f9678740a5`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 7.9 MB (7879779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e811f2ebf7718e013c3b42f4380e0f8c7e092ef1894a9772fac547b69565da`  
		Last Modified: Tue, 07 Apr 2026 01:47:37 GMT  
		Size: 48.9 MB (48867850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4572cb7815b8d85f84d5779c37ffaeaa45a40205aa52600d0772c3f9b65c0e1d`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41629215bf30b7dce998c62fd19d0d4182cdeb284442222bfef4c2a748286a87`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260f04bf26e9e37a65aa5ca1e0ec1f6d2389ade77305722a0dfe0d5a50e8a161`  
		Last Modified: Tue, 07 Apr 2026 01:47:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c64fee177752fb653bb4c67c264da76fcbd49149f138a7e24dd8136eb7249432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe8767e24afbdcc926ff9bf5b5e6f06ebb5d4e13fcd8efda4891c97d3375d76`

```dockerfile
```

-	Layers:
	-	`sha256:1ad5275ae56819a06df1f709ecc5abbce3f3b30a6576bc62577a6294661aee97`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab9ea4faa68774f8dcfdb171efa8fc2b358380d5ba61fd2d2212d9ef7eef906`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7f6ba8a05e8752787341b7fe2a6a74810b06aa9fa70a1a0228f775cc695b037a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930d1c377ac04e3da986523b9e03970d9aff20f8036670f211d374ae5e6e562c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:04:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 02:04:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:04:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:04:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde4224141eb326416434e57e6985960fa0299c171636ec51c978d7483ded221`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 6.5 MB (6512130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39644797429280d1790a41b83be262964fe685b66a13098f85a2830ef136af23`  
		Last Modified: Tue, 07 Apr 2026 02:04:51 GMT  
		Size: 46.3 MB (46320009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a038716dc519bd0d53565ee9d170bb27389cee982f799ed02c5b30bb400da63b`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2857e0024941e8431e0d2e7288ff873bb60af2b99250a6c109fb700e616232c`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac7ccabd4f0e669d232e23f27536a4797faec571f1d5b385e8d37e9543ad1d4`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d033ac4c98bc3deb3c46315bff42913e431c32321890ec7914cd6b43bf0a4454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a769173f691e7dbe1bbac685b1b6d2cf8af5e40c11a7536386e603ca5e558e45`

```dockerfile
```

-	Layers:
	-	`sha256:dff92a3ce28b58e918bb8a1b393141f0d15f0a7436d538d1b53bafdf3cd2f3f0`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29723eb32c4a4046b83b01b8e97bd5b93cfc334f24c3dcc9145d178038a36230`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a2a43c10363a3e5414039345eec8b6f29f095b8780f535d2bf8c345ecaccc9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81846058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2139c408fd9e94f3fd3b1367a24940cb005338e161818d060b054dac34b1bfdb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:50:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 01:50:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 01:50:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 01:50:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:50:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dbac72acd22aba48e1d3ad7b9a5e1cbeb7c0aebb12c6a591e18543bc5e15cc`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 7.7 MB (7696984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c262557b34cb3bc7ec83d26805b2652f905d6b967d83f8842bf504468e0a1838`  
		Last Modified: Tue, 07 Apr 2026 01:50:52 GMT  
		Size: 46.0 MB (46008449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74498ce48e4b91d1e7d88a9e0754b61258942627ce75895df3cb7db3c1b5c15`  
		Last Modified: Tue, 07 Apr 2026 01:50:50 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65c1e63d63625f49395f0638311d1e6c4f2c7a8305b76a623caebef010c4bc9`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b076129ef9a105123d5ba844cad634c503183088bbaf98f5207dd723da7a8f3`  
		Last Modified: Tue, 07 Apr 2026 01:50:52 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:2a6ed1d948d7f96ec2f4c78bacc10dff88e412f6fe98b8dbd8b836b5a352f7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f569ab759f8a5b6b8245d0f34e87a8b99fe51d28a3fc5a72fb47d21f8bec4d7d`

```dockerfile
```

-	Layers:
	-	`sha256:d88ff8ebd731cac72703f8bd7c6c93fbe8fe1d291c78a4810ec94e4c492d84cc`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d8afa3639be4d3d75ce8e3dc27463cae0a100a14b3761dab53339f975b1fc7`  
		Last Modified: Tue, 07 Apr 2026 01:50:51 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
