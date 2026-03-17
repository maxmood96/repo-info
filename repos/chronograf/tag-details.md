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
$ docker pull chronograf@sha256:81ae99d4b4545873d889ce321fb22f5953f31c745eefb5f3537714d63fbd91e5
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
$ docker pull chronograf@sha256:27519f63ca4898ef8ba285323e09fc616c0cb32276926d1c8869277937c677dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85008397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dba3598b178ecb4f435fa929493fcf3707c5d4a13ea918dea1cd4d813f60a44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 16 Mar 2026 22:39:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:39:09 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:39:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbf4623f75eb7fd26cd18da1dcf097bc72629733c4845e0f443afdfd02f5171`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 7.9 MB (7879797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e868813716e1ec569c7ede31f06e50226a75aef765936e5db3b98397d4b33e3`  
		Last Modified: Mon, 16 Mar 2026 22:39:22 GMT  
		Size: 48.9 MB (48867915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3769fec83e3c7d61bdd133e533add194b475101c6d0f3a7a36af85b72d47e651`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c660916672fff41690d2258d07676e84412871cbbf0f3bb7f4337bcd25987ea9`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1485265a9ac688e24a0588061f9c657800fc3c320bd65bb4c1ebb54ee267a7`  
		Last Modified: Mon, 16 Mar 2026 22:39:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:5ce28ceb177bacf5b9b70343c7ab22333b9611f321ac737af07110277902eb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc5d688036c5ce23a007e8d6ec9d580bc7068f95c38ccef8458f8deb6be9863`

```dockerfile
```

-	Layers:
	-	`sha256:1abc0e3b5f838bf9533a6ab770154a0e08494bbb5c0d6289d3b0f29287884f7f`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb21327530f8de8ab6998db7133dddd6c951c25c478d66b2f715b6153576162a`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:874cd2ce56827414451a06623a8af4a57f5499474fbdd5e3387223eb29b8b304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc61433b41ed8783b3c117c6e7d501a34350241cf76da9dd453f9df261d7bb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:23:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 16 Mar 2026 23:23:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 23:23:28 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 23:23:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:23:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f16e25d1e14be872b31f0c356cd9f2b5f0690b0c25a741a42f504fdb415d48`  
		Last Modified: Mon, 16 Mar 2026 23:23:39 GMT  
		Size: 6.5 MB (6512156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03285ac7c555d51d606190238cf48900bb66136b9c1de803f2f5cce20f4cc1e`  
		Last Modified: Mon, 16 Mar 2026 23:23:40 GMT  
		Size: 46.3 MB (46320093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1036946a7677c4d604fa0e1fdc6c290a79677545ce6545a19a49423b9875f5b`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06a045f30758384ab07fd2581a6bc48138a2ecec9a31a07813abe9220f21a30`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e812d7ae19cd5f03dca2f564f797fcb1ff6bd3bb2f2035ed91cbcb7fbbd610e6`  
		Last Modified: Mon, 16 Mar 2026 23:23:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:8d9f4a452d88dbc953693edb1585f4446fcf0c164d4bb36ffd5ceeb2c32dab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be112a84b76f0d773bcaa67194129d9eb11c187f495dee1ce4457a44c2021024`

```dockerfile
```

-	Layers:
	-	`sha256:d8d5c777df0f4b73981bf7e1cb66c1334a40b0440e990f6ac8886f56826312e5`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da9a9d56ee2fbc0f2015279a5f68ce0be788f1b0b50a47ec6cf2c41609c33e6`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0a77c7b031acad2567f14cbdf90db3cbf2a5028e14cd9979c50c183003d3be85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81845997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da2d36f8026c0c84e1c5cf8850cfd4c4d22a2cc1c2a863da1d164e0a650292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 16 Mar 2026 22:41:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:41:35 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:41:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f09ae52ddab292a199a66a53c1d8d9371a78b17fcbb59abd71bcdbbb8b942`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 7.7 MB (7697010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c62ba20fbac9591d2f8893a5ff5b0a5eee129acb796a1eb6c9d6c43f669ef30`  
		Last Modified: Mon, 16 Mar 2026 22:41:47 GMT  
		Size: 46.0 MB (46008448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821d80786e58c4f7cf23898ca6fcbecb9ce4836595c303622523620a79a548df`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9aa47cd2c2eedfbd66c9f768588fe3fb791a46e3f0f49394d85c557c60d3fbb`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3ea67f5ce87af459bfc0e2a49b81a9c9d76ef6041c02c41bf0b9eb304dee2`  
		Last Modified: Mon, 16 Mar 2026 22:41:47 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:c30aad004f940157e20dbf28485407b7c4e5d632e1192aefbe7427421ad2126a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5dd236a9182db4844b0d181db93a4d8548e75fc6d3e094f85f0f428ffc2979`

```dockerfile
```

-	Layers:
	-	`sha256:29ce36b13958c091d1aaf70efecf405baecc22341491ee6ef0af40dd5220adca`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624ea2a2909e178414bbc9d7f33e6ef39a87828ff87a45e4b5964dcc9066b654`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 16.2 KB (16191 bytes)  
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
$ docker pull chronograf@sha256:81ae99d4b4545873d889ce321fb22f5953f31c745eefb5f3537714d63fbd91e5
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
$ docker pull chronograf@sha256:27519f63ca4898ef8ba285323e09fc616c0cb32276926d1c8869277937c677dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85008397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dba3598b178ecb4f435fa929493fcf3707c5d4a13ea918dea1cd4d813f60a44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 16 Mar 2026 22:39:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:39:09 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:39:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbf4623f75eb7fd26cd18da1dcf097bc72629733c4845e0f443afdfd02f5171`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 7.9 MB (7879797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e868813716e1ec569c7ede31f06e50226a75aef765936e5db3b98397d4b33e3`  
		Last Modified: Mon, 16 Mar 2026 22:39:22 GMT  
		Size: 48.9 MB (48867915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3769fec83e3c7d61bdd133e533add194b475101c6d0f3a7a36af85b72d47e651`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c660916672fff41690d2258d07676e84412871cbbf0f3bb7f4337bcd25987ea9`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1485265a9ac688e24a0588061f9c657800fc3c320bd65bb4c1ebb54ee267a7`  
		Last Modified: Mon, 16 Mar 2026 22:39:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:5ce28ceb177bacf5b9b70343c7ab22333b9611f321ac737af07110277902eb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc5d688036c5ce23a007e8d6ec9d580bc7068f95c38ccef8458f8deb6be9863`

```dockerfile
```

-	Layers:
	-	`sha256:1abc0e3b5f838bf9533a6ab770154a0e08494bbb5c0d6289d3b0f29287884f7f`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb21327530f8de8ab6998db7133dddd6c951c25c478d66b2f715b6153576162a`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:874cd2ce56827414451a06623a8af4a57f5499474fbdd5e3387223eb29b8b304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc61433b41ed8783b3c117c6e7d501a34350241cf76da9dd453f9df261d7bb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:23:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 16 Mar 2026 23:23:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 23:23:28 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 23:23:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:23:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f16e25d1e14be872b31f0c356cd9f2b5f0690b0c25a741a42f504fdb415d48`  
		Last Modified: Mon, 16 Mar 2026 23:23:39 GMT  
		Size: 6.5 MB (6512156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03285ac7c555d51d606190238cf48900bb66136b9c1de803f2f5cce20f4cc1e`  
		Last Modified: Mon, 16 Mar 2026 23:23:40 GMT  
		Size: 46.3 MB (46320093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1036946a7677c4d604fa0e1fdc6c290a79677545ce6545a19a49423b9875f5b`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06a045f30758384ab07fd2581a6bc48138a2ecec9a31a07813abe9220f21a30`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e812d7ae19cd5f03dca2f564f797fcb1ff6bd3bb2f2035ed91cbcb7fbbd610e6`  
		Last Modified: Mon, 16 Mar 2026 23:23:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:8d9f4a452d88dbc953693edb1585f4446fcf0c164d4bb36ffd5ceeb2c32dab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be112a84b76f0d773bcaa67194129d9eb11c187f495dee1ce4457a44c2021024`

```dockerfile
```

-	Layers:
	-	`sha256:d8d5c777df0f4b73981bf7e1cb66c1334a40b0440e990f6ac8886f56826312e5`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da9a9d56ee2fbc0f2015279a5f68ce0be788f1b0b50a47ec6cf2c41609c33e6`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0a77c7b031acad2567f14cbdf90db3cbf2a5028e14cd9979c50c183003d3be85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81845997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da2d36f8026c0c84e1c5cf8850cfd4c4d22a2cc1c2a863da1d164e0a650292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 16 Mar 2026 22:41:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:41:35 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:41:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f09ae52ddab292a199a66a53c1d8d9371a78b17fcbb59abd71bcdbbb8b942`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 7.7 MB (7697010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c62ba20fbac9591d2f8893a5ff5b0a5eee129acb796a1eb6c9d6c43f669ef30`  
		Last Modified: Mon, 16 Mar 2026 22:41:47 GMT  
		Size: 46.0 MB (46008448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821d80786e58c4f7cf23898ca6fcbecb9ce4836595c303622523620a79a548df`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9aa47cd2c2eedfbd66c9f768588fe3fb791a46e3f0f49394d85c557c60d3fbb`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3ea67f5ce87af459bfc0e2a49b81a9c9d76ef6041c02c41bf0b9eb304dee2`  
		Last Modified: Mon, 16 Mar 2026 22:41:47 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:c30aad004f940157e20dbf28485407b7c4e5d632e1192aefbe7427421ad2126a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5dd236a9182db4844b0d181db93a4d8548e75fc6d3e094f85f0f428ffc2979`

```dockerfile
```

-	Layers:
	-	`sha256:29ce36b13958c091d1aaf70efecf405baecc22341491ee6ef0af40dd5220adca`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624ea2a2909e178414bbc9d7f33e6ef39a87828ff87a45e4b5964dcc9066b654`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 16.2 KB (16191 bytes)  
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
$ docker pull chronograf@sha256:25d3d87ad8923e910474ac29cd87c6df887cf7526a448e51e726a964b467093d
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
$ docker pull chronograf@sha256:a18cef2f5e7b0e862b5ef7a017e52ff378fadd1e7ea83965e02c4ed20c482b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69252759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f900eebab9479fb484a8eb09fbc8db61f5bb803cb60ba9c6b0ccedc674f3618`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 16 Mar 2026 22:38:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:38:42 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:38:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:38:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512ebecac862e87b5258b4e386aeabc40f8443091dfc132a58ce20ae076c6848`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 4.2 MB (4209086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d05584f90aec5b8f19e32caf0706a2e3338c75427c5f93793f98d819cb46c4`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 34.8 MB (34761465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061749f6feb2e03ede23bed482b0feb22a91a4f8d8ddc18eedb161d84d29b9cd`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097bb814c57ff94afb4fa32fb2c45312093e65f38301dbf9748afedabf85fc86`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8daf82e99eb9b64d8914e2e572c1a2b7bc4ee618785164d2100af7c6f9e5c`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:f80c7283661848e0c02940676a6c1e799d4ba031c0ab20a9ee0f536151c82003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f460e0aca87a3449b38aa97dd64d9a0d7259ea071d6a4dd99adedf598d15e0f3`

```dockerfile
```

-	Layers:
	-	`sha256:350c83164f7dd1f7b9df8c9c7ce94020b76d9813707664b53e1e65726391361a`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 3.1 MB (3057293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec2e97188a8b06942c1b9d37e47eb612e8330a1ce1fc2172d99a0a71aedcf744`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3d420794f204dad123e229e6aae7414a1c2cdcdd616ba014d071280b58fc37ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62206819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2962db5ac5e902d190567aa2ca3940434cd09f9f06dc5d7fe3a4c7c195e24085`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:21:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 16 Mar 2026 23:21:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 23:21:28 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 23:21:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:21:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3bc17afcb32786a635d7faf13a7aa3a4142ac1a648b659c697f5e02460592774`  
		Last Modified: Mon, 16 Mar 2026 21:52:44 GMT  
		Size: 25.6 MB (25551392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce15ce55d9d8421c3bd87262b10eb513164c1535b864b8ab4391e6db23e2655f`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 3.5 MB (3511507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521f7923b2f27566907d612b1da3685968f13f5f567fb6c1f91847a0ef54b1eb`  
		Last Modified: Mon, 16 Mar 2026 23:21:38 GMT  
		Size: 33.1 MB (33119531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21416a802d23d270b32e1fd31e3cf284700e9d4705cdeb75694ac5b5d22aeb1f`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d05fbd5096c9ef8b6f6a3a95d4e235f6d748fdc7c5e1cd0f390c5bac0395375`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3bb3bcee02ac7fad233e5ddf503a730e2fc42b67ba64f8816303a896b53b1b`  
		Last Modified: Mon, 16 Mar 2026 23:21:38 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:6dc3319e545c2b81226930c23037fb37264121851e2cf05b431b0266009ec77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3075373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a96aeaf0de38e059dcb8486b4cdb687b08223034bc2ff650220fa517a79e9`

```dockerfile
```

-	Layers:
	-	`sha256:a01471a42c2dff6db6041f7acb516352897d39819ea941e84b83792759d7d771`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 3.1 MB (3059564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9e544d99825b216d398afc5e5f971076635ce64c802a8b75868f4a59b6b793`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ac7badd202f0a9e4d2140645b4b210bdcdf49f74d9970fdc129f8d2d4e5bcff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66240622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba99032d36795b558a59ffa3fbb6c40ff97de3932f16665dd5bbb5bd18b8627e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:40:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 16 Mar 2026 22:41:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:41:00 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:41:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368aac0cc039a2c6408a7ce65e23ace4971ea372901624fefa57f1c9e903dab`  
		Last Modified: Mon, 16 Mar 2026 22:41:10 GMT  
		Size: 4.2 MB (4210429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdeae542f44e912ab1af9049fd6fe0bf6c048d3ea3ced8f94385f42266a818`  
		Last Modified: Mon, 16 Mar 2026 22:41:11 GMT  
		Size: 33.3 MB (33261285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a62a967f61f371b9c7855d9a460f2b7c0e14b4fa803f65ea7ef73ec93d8fcec`  
		Last Modified: Mon, 16 Mar 2026 22:41:09 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24a80ca0040fefe9e0367d10216db7da9378193f33aa1db64b77ba6b171f92d`  
		Last Modified: Mon, 16 Mar 2026 22:41:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021424763d0703253891ba83b6d211ff1e99f4dc0d7fb36afa64b92ca182d25`  
		Last Modified: Mon, 16 Mar 2026 22:41:11 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:3650a57b2ba957fc5f8f4934dfde2ea6456e3b6d37534319256a2cd94d76b521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1120ed1d6a810cbc542541d7c63d33e8c62957282b17df1fb38b1f22b5781384`

```dockerfile
```

-	Layers:
	-	`sha256:c34bf4d42cc4d818d48b59c1bceac71052c29e47fe447c228db3d4dd6fea707d`  
		Last Modified: Mon, 16 Mar 2026 22:41:10 GMT  
		Size: 3.1 MB (3057542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52db8dbe8dd9c2b6b954758699f524ee1ae205beec74bd23acf8a9df0436b40`  
		Last Modified: Mon, 16 Mar 2026 22:41:09 GMT  
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
$ docker pull chronograf@sha256:25d3d87ad8923e910474ac29cd87c6df887cf7526a448e51e726a964b467093d
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
$ docker pull chronograf@sha256:a18cef2f5e7b0e862b5ef7a017e52ff378fadd1e7ea83965e02c4ed20c482b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69252759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f900eebab9479fb484a8eb09fbc8db61f5bb803cb60ba9c6b0ccedc674f3618`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 16 Mar 2026 22:38:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:38:42 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:38:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:38:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:38:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512ebecac862e87b5258b4e386aeabc40f8443091dfc132a58ce20ae076c6848`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 4.2 MB (4209086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d05584f90aec5b8f19e32caf0706a2e3338c75427c5f93793f98d819cb46c4`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 34.8 MB (34761465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061749f6feb2e03ede23bed482b0feb22a91a4f8d8ddc18eedb161d84d29b9cd`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097bb814c57ff94afb4fa32fb2c45312093e65f38301dbf9748afedabf85fc86`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8daf82e99eb9b64d8914e2e572c1a2b7bc4ee618785164d2100af7c6f9e5c`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:f80c7283661848e0c02940676a6c1e799d4ba031c0ab20a9ee0f536151c82003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f460e0aca87a3449b38aa97dd64d9a0d7259ea071d6a4dd99adedf598d15e0f3`

```dockerfile
```

-	Layers:
	-	`sha256:350c83164f7dd1f7b9df8c9c7ce94020b76d9813707664b53e1e65726391361a`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 3.1 MB (3057293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec2e97188a8b06942c1b9d37e47eb612e8330a1ce1fc2172d99a0a71aedcf744`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3d420794f204dad123e229e6aae7414a1c2cdcdd616ba014d071280b58fc37ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62206819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2962db5ac5e902d190567aa2ca3940434cd09f9f06dc5d7fe3a4c7c195e24085`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:21:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 16 Mar 2026 23:21:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 23:21:28 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 23:21:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:21:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:21:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3bc17afcb32786a635d7faf13a7aa3a4142ac1a648b659c697f5e02460592774`  
		Last Modified: Mon, 16 Mar 2026 21:52:44 GMT  
		Size: 25.6 MB (25551392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce15ce55d9d8421c3bd87262b10eb513164c1535b864b8ab4391e6db23e2655f`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 3.5 MB (3511507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521f7923b2f27566907d612b1da3685968f13f5f567fb6c1f91847a0ef54b1eb`  
		Last Modified: Mon, 16 Mar 2026 23:21:38 GMT  
		Size: 33.1 MB (33119531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21416a802d23d270b32e1fd31e3cf284700e9d4705cdeb75694ac5b5d22aeb1f`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d05fbd5096c9ef8b6f6a3a95d4e235f6d748fdc7c5e1cd0f390c5bac0395375`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3bb3bcee02ac7fad233e5ddf503a730e2fc42b67ba64f8816303a896b53b1b`  
		Last Modified: Mon, 16 Mar 2026 23:21:38 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:6dc3319e545c2b81226930c23037fb37264121851e2cf05b431b0266009ec77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3075373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a96aeaf0de38e059dcb8486b4cdb687b08223034bc2ff650220fa517a79e9`

```dockerfile
```

-	Layers:
	-	`sha256:a01471a42c2dff6db6041f7acb516352897d39819ea941e84b83792759d7d771`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 3.1 MB (3059564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9e544d99825b216d398afc5e5f971076635ce64c802a8b75868f4a59b6b793`  
		Last Modified: Mon, 16 Mar 2026 23:21:37 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ac7badd202f0a9e4d2140645b4b210bdcdf49f74d9970fdc129f8d2d4e5bcff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66240622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba99032d36795b558a59ffa3fbb6c40ff97de3932f16665dd5bbb5bd18b8627e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:40:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 16 Mar 2026 22:41:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:41:00 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:41:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368aac0cc039a2c6408a7ce65e23ace4971ea372901624fefa57f1c9e903dab`  
		Last Modified: Mon, 16 Mar 2026 22:41:10 GMT  
		Size: 4.2 MB (4210429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdeae542f44e912ab1af9049fd6fe0bf6c048d3ea3ced8f94385f42266a818`  
		Last Modified: Mon, 16 Mar 2026 22:41:11 GMT  
		Size: 33.3 MB (33261285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a62a967f61f371b9c7855d9a460f2b7c0e14b4fa803f65ea7ef73ec93d8fcec`  
		Last Modified: Mon, 16 Mar 2026 22:41:09 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24a80ca0040fefe9e0367d10216db7da9378193f33aa1db64b77ba6b171f92d`  
		Last Modified: Mon, 16 Mar 2026 22:41:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021424763d0703253891ba83b6d211ff1e99f4dc0d7fb36afa64b92ca182d25`  
		Last Modified: Mon, 16 Mar 2026 22:41:11 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:3650a57b2ba957fc5f8f4934dfde2ea6456e3b6d37534319256a2cd94d76b521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1120ed1d6a810cbc542541d7c63d33e8c62957282b17df1fb38b1f22b5781384`

```dockerfile
```

-	Layers:
	-	`sha256:c34bf4d42cc4d818d48b59c1bceac71052c29e47fe447c228db3d4dd6fea707d`  
		Last Modified: Mon, 16 Mar 2026 22:41:10 GMT  
		Size: 3.1 MB (3057542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52db8dbe8dd9c2b6b954758699f524ee1ae205beec74bd23acf8a9df0436b40`  
		Last Modified: Mon, 16 Mar 2026 22:41:09 GMT  
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
$ docker pull chronograf@sha256:1beac8e9e8dbd99437266ca873605e722cf6941ddc2ecdec8f30bb71100d6b1d
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
$ docker pull chronograf@sha256:921fcedab98016c89bc39eed7ee1e6628c9810caae3f65cc054fee08b27d8190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ca4253de8f64e335cd739136c71c6b4a9f8235d63b14cda56fbf73c8a8cd1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 16 Mar 2026 22:38:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:38:41 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:38:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:38:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2e4e03a8977b2ce90dd4edefee86569487613d1f7dab5584092a24266de16`  
		Last Modified: Mon, 16 Mar 2026 22:38:50 GMT  
		Size: 5.2 MB (5241733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f749e6622cc3a58638f3094f7d124928ede3ffbdb9f957e2c845d8ddb7926`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 34.4 MB (34364355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebb2bd8c33c77c353af3d8635ab599f9b9e17ae83359466911f0472fa8241f2`  
		Last Modified: Mon, 16 Mar 2026 22:38:50 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb98feddd4c98d65a4a316621e9ee534d6cf78c6c146304e001f0b62f1092b0`  
		Last Modified: Mon, 16 Mar 2026 22:38:50 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3b7535d6fc0214a043e279a6f2b4388c6ed3a0825eeeaea052b93478e64d99`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:0281add6ac52b917aabd441c8e440e021f0eb9425c620979e5abccc4de196f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136467e1a646016e3091c77d69bb1e13d242f734c28adb9b2a4e572516a75bf6`

```dockerfile
```

-	Layers:
	-	`sha256:6ead22308341521a1b1e112f34dc83cdbcc8d56d6cd6de49732b0daf635ac42e`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbcfcd2958ba11c48610a08d26b1c2051baa9cbdc441530c79d8679a6ddb39e`  
		Last Modified: Mon, 16 Mar 2026 22:38:50 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3b9e232e64889122363967426dabc73f3e3c469b2523b95a0f27d05b44b669bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755e16486435995f11eaa19e45f38f0a4b3145bc5435c1a7eec22b7fe3018df9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:21:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 16 Mar 2026 23:21:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 23:21:58 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 23:21:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:21:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3bc17afcb32786a635d7faf13a7aa3a4142ac1a648b659c697f5e02460592774`  
		Last Modified: Mon, 16 Mar 2026 21:52:44 GMT  
		Size: 25.6 MB (25551392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86bc01684e9cd4112f6e586abd0154b4e946066b8b76e853db41f9179224b90`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 4.5 MB (4510019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3698d43e8cb5c373370b215220bbf85d4630217a71ef71fcc5f948e2861e33`  
		Last Modified: Mon, 16 Mar 2026 23:22:07 GMT  
		Size: 32.5 MB (32534953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f170f92a5763b4ecf5b8e2b3798d25ec73991f8b653d7959c37b937b4db11ce`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b53f0e7dc45a60f44e5584226a02423d3340bea51ed2ce41a9bc265d4630b1`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414b9a6ff48f9410118ade7ffea54a0d1d09de5b6562820df6d2f1b8824d4c9f`  
		Last Modified: Mon, 16 Mar 2026 23:22:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:e58d997bd2b82b7bb1c55305f2d91ce4f6eb2ef3dc0881dfcfbb5e6c942eb6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7235f6460704fcd8427380f95c7c6ff7b921b725c00b0d02492c0562fa7de40a`

```dockerfile
```

-	Layers:
	-	`sha256:442145bc1017016a312514029140041d1c42d77639590b532e84935b303df772`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb3fba3dac1eff12a5bfda7a81fce1369c3d39c323fcf76ec90839846aa0ca0`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c3c7d939961fab324e27785f132eabc1b8f8d5989efa0173e424c2d2b5200968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66428211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f7ecd0274b673f7019f4954ccaaf729d7a8131f5e2d0d2a4518a71e55adb56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:40:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 16 Mar 2026 22:41:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:41:03 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:41:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d2ed050107a8f8cf111888404e80f1875765fe7a1968ce96c4a134dd47c070`  
		Last Modified: Mon, 16 Mar 2026 22:41:13 GMT  
		Size: 5.2 MB (5229795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6749c99aa433e1e84a2b5948d8e87308ca5dcb94c9393766906207457052cc`  
		Last Modified: Mon, 16 Mar 2026 22:41:13 GMT  
		Size: 32.4 MB (32429491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de443593b0e76b5f2ad086d01ca7e72f7d4229e7f0b068b8fc7079313d16cb91`  
		Last Modified: Mon, 16 Mar 2026 22:41:12 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f62237f09156352af81c0787b7328bfe9ba378dbe8adafb92ede4761e9efb5a`  
		Last Modified: Mon, 16 Mar 2026 22:41:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729c40ed8ca7fd0530a99ce280dcb3cc77e73f26dd71cfaa593f91914d2ed92c`  
		Last Modified: Mon, 16 Mar 2026 22:41:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:81b451baf82e8fac664c92030c767e61fc14b5adfb45d0732dcdd0597eda82fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97261bd853c5c3f15cf8c6194a360f0ee1e8d606e5daefe58c9d4af20cae246`

```dockerfile
```

-	Layers:
	-	`sha256:b1107d80ba04c8b86a262f28bc01e1240dcf6433b92820356bf08d9edc7663c7`  
		Last Modified: Mon, 16 Mar 2026 22:41:13 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51767a3934610b20af84d3114d3538a8a623c7150665c0f8e33b4ab7114af8e`  
		Last Modified: Mon, 16 Mar 2026 22:41:12 GMT  
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
$ docker pull chronograf@sha256:1beac8e9e8dbd99437266ca873605e722cf6941ddc2ecdec8f30bb71100d6b1d
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
$ docker pull chronograf@sha256:921fcedab98016c89bc39eed7ee1e6628c9810caae3f65cc054fee08b27d8190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ca4253de8f64e335cd739136c71c6b4a9f8235d63b14cda56fbf73c8a8cd1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 16 Mar 2026 22:38:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:38:41 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:38:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:38:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:38:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2e4e03a8977b2ce90dd4edefee86569487613d1f7dab5584092a24266de16`  
		Last Modified: Mon, 16 Mar 2026 22:38:50 GMT  
		Size: 5.2 MB (5241733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f749e6622cc3a58638f3094f7d124928ede3ffbdb9f957e2c845d8ddb7926`  
		Last Modified: Mon, 16 Mar 2026 22:38:52 GMT  
		Size: 34.4 MB (34364355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebb2bd8c33c77c353af3d8635ab599f9b9e17ae83359466911f0472fa8241f2`  
		Last Modified: Mon, 16 Mar 2026 22:38:50 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb98feddd4c98d65a4a316621e9ee534d6cf78c6c146304e001f0b62f1092b0`  
		Last Modified: Mon, 16 Mar 2026 22:38:50 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3b7535d6fc0214a043e279a6f2b4388c6ed3a0825eeeaea052b93478e64d99`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:0281add6ac52b917aabd441c8e440e021f0eb9425c620979e5abccc4de196f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136467e1a646016e3091c77d69bb1e13d242f734c28adb9b2a4e572516a75bf6`

```dockerfile
```

-	Layers:
	-	`sha256:6ead22308341521a1b1e112f34dc83cdbcc8d56d6cd6de49732b0daf635ac42e`  
		Last Modified: Mon, 16 Mar 2026 22:38:51 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbcfcd2958ba11c48610a08d26b1c2051baa9cbdc441530c79d8679a6ddb39e`  
		Last Modified: Mon, 16 Mar 2026 22:38:50 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:3b9e232e64889122363967426dabc73f3e3c469b2523b95a0f27d05b44b669bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755e16486435995f11eaa19e45f38f0a4b3145bc5435c1a7eec22b7fe3018df9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:21:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 16 Mar 2026 23:21:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 23:21:58 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 23:21:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:21:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:21:58 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3bc17afcb32786a635d7faf13a7aa3a4142ac1a648b659c697f5e02460592774`  
		Last Modified: Mon, 16 Mar 2026 21:52:44 GMT  
		Size: 25.6 MB (25551392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86bc01684e9cd4112f6e586abd0154b4e946066b8b76e853db41f9179224b90`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 4.5 MB (4510019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3698d43e8cb5c373370b215220bbf85d4630217a71ef71fcc5f948e2861e33`  
		Last Modified: Mon, 16 Mar 2026 23:22:07 GMT  
		Size: 32.5 MB (32534953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f170f92a5763b4ecf5b8e2b3798d25ec73991f8b653d7959c37b937b4db11ce`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b53f0e7dc45a60f44e5584226a02423d3340bea51ed2ce41a9bc265d4630b1`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414b9a6ff48f9410118ade7ffea54a0d1d09de5b6562820df6d2f1b8824d4c9f`  
		Last Modified: Mon, 16 Mar 2026 23:22:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:e58d997bd2b82b7bb1c55305f2d91ce4f6eb2ef3dc0881dfcfbb5e6c942eb6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7235f6460704fcd8427380f95c7c6ff7b921b725c00b0d02492c0562fa7de40a`

```dockerfile
```

-	Layers:
	-	`sha256:442145bc1017016a312514029140041d1c42d77639590b532e84935b303df772`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb3fba3dac1eff12a5bfda7a81fce1369c3d39c323fcf76ec90839846aa0ca0`  
		Last Modified: Mon, 16 Mar 2026 23:22:06 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c3c7d939961fab324e27785f132eabc1b8f8d5989efa0173e424c2d2b5200968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66428211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f7ecd0274b673f7019f4954ccaaf729d7a8131f5e2d0d2a4518a71e55adb56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:40:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 16 Mar 2026 22:41:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:41:03 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:41:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d2ed050107a8f8cf111888404e80f1875765fe7a1968ce96c4a134dd47c070`  
		Last Modified: Mon, 16 Mar 2026 22:41:13 GMT  
		Size: 5.2 MB (5229795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6749c99aa433e1e84a2b5948d8e87308ca5dcb94c9393766906207457052cc`  
		Last Modified: Mon, 16 Mar 2026 22:41:13 GMT  
		Size: 32.4 MB (32429491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de443593b0e76b5f2ad086d01ca7e72f7d4229e7f0b068b8fc7079313d16cb91`  
		Last Modified: Mon, 16 Mar 2026 22:41:12 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f62237f09156352af81c0787b7328bfe9ba378dbe8adafb92ede4761e9efb5a`  
		Last Modified: Mon, 16 Mar 2026 22:41:12 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729c40ed8ca7fd0530a99ce280dcb3cc77e73f26dd71cfaa593f91914d2ed92c`  
		Last Modified: Mon, 16 Mar 2026 22:41:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:81b451baf82e8fac664c92030c767e61fc14b5adfb45d0732dcdd0597eda82fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97261bd853c5c3f15cf8c6194a360f0ee1e8d606e5daefe58c9d4af20cae246`

```dockerfile
```

-	Layers:
	-	`sha256:b1107d80ba04c8b86a262f28bc01e1240dcf6433b92820356bf08d9edc7663c7`  
		Last Modified: Mon, 16 Mar 2026 22:41:13 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51767a3934610b20af84d3114d3538a8a623c7150665c0f8e33b4ab7114af8e`  
		Last Modified: Mon, 16 Mar 2026 22:41:12 GMT  
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
$ docker pull chronograf@sha256:e102126a7d8736cab70b31003927745fc88026f18ab4f5a1935f3d0f60f5d1e0
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
$ docker pull chronograf@sha256:a27e274b5f466e3c563c7e5a5ee0c8e1af1107ca9cbb4fe831c680217bde511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51127482bd078da1a95560067b7bb9aab2387fabb93ba3cb217afb3473ba91df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:39:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 16 Mar 2026 22:39:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:39:15 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:39:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf694cde0b5a4c07f4ab22f56c2596af607f667ba582a2a9448e94dd4997502d`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 5.2 MB (5241789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce2fff56f6a6568500fb7786fdb86ef26b490d8ebc6d95aa9cf6275c6e955`  
		Last Modified: Mon, 16 Mar 2026 22:39:26 GMT  
		Size: 35.0 MB (35011823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb051b030b13d6e1d5fd3d25fe815f21104fee9ae16760526287797779c6ad`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27daf5564635cf55fb3c7e1ef3361c02026b063bf7b032de7126ccb8397855`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8596f2c8a950db3b6e60419744469b3c508733c7b27eafa3e3b100d55baec43`  
		Last Modified: Mon, 16 Mar 2026 22:39:26 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:9068ab093364675be9c2b6dbd858d53c9b0c59f784e2e15cd4c12325a8fdcdd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e47febbac50430a26de65675796588a4f19161a655285d538be2415edf8ba58`

```dockerfile
```

-	Layers:
	-	`sha256:5ceb61e48e83e7b7f46542bdc80e2296b163732e407fa2aa539ce727166e8161`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b9e9d73234ba10d01a80800471700aca3ee11254c0545274d6d680da14b6cd`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:231767f2a6c2a10b5b92b2aedf702c6de139d57614bbff2ccf2a21f5693afd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63397411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155f0b2f8133554ff7367a530ef9e230f4f9861d3bc3357ba2127d1914c5bccb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:22:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 16 Mar 2026 23:22:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 23:22:57 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 23:22:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:22:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3bc17afcb32786a635d7faf13a7aa3a4142ac1a648b659c697f5e02460592774`  
		Last Modified: Mon, 16 Mar 2026 21:52:44 GMT  
		Size: 25.6 MB (25551392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e182cbbd9ce751bb8b2a330f86b0acba56ce6e4b961b2fa966bc834ab8ed66`  
		Last Modified: Mon, 16 Mar 2026 23:23:06 GMT  
		Size: 4.5 MB (4510007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304ec9add4007a9a2353f44f47bac93f0137c935d50ec11f8f368137df8a3658`  
		Last Modified: Mon, 16 Mar 2026 23:23:06 GMT  
		Size: 33.3 MB (33311620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b22e647465c6b5910bd71f8f2f989074615b6bf512cc3bc8fa59c7835c081e`  
		Last Modified: Mon, 16 Mar 2026 23:23:05 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c502f7dda028fa78a15868b2a6e7f43023145b2336ac7571439862a24580c0`  
		Last Modified: Mon, 16 Mar 2026 23:23:05 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135d840a52ba2a23aaf3f30734dced78ca16fc07db649de1dbcdff02951a615`  
		Last Modified: Mon, 16 Mar 2026 23:23:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd6c5843822a3cc53dac5b8411c5473a76e90658e914c9c1b1f69ea857a7c105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abe68c638a62e94b949e8d40fd620b7c275d5a689a57eabfd3b30a7c3d75daa`

```dockerfile
```

-	Layers:
	-	`sha256:d5d022d8c0e3700bd6de60b9eb59cb4e8b44ffa78972a76c0ad12d67bca5aa2b`  
		Last Modified: Mon, 16 Mar 2026 23:23:06 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc05947686da96ccd883ed05e6e0898559cce23eecb76277a70ca40ca595f3d9`  
		Last Modified: Mon, 16 Mar 2026 23:23:05 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c946487837657a628f81a63ace8c9772d7da4b50e200156a34a1e6641cf5c95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67181112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc85fbf68d207955c3da996f1778b7ae88108339602b5714dc8bcdf2beb924b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:41:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 16 Mar 2026 22:41:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:41:07 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:41:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeec8b01f88aa125137a54b254e8437c7e832cdbeb18158be6dae84165ca160`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 5.2 MB (5229845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f75032ab63711c5c66c2c1b876e4fea7abf0d19da486dfafd11c8c9e2ad1bd`  
		Last Modified: Mon, 16 Mar 2026 22:41:18 GMT  
		Size: 33.2 MB (33182356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69527b2b87f7819c20e8bd492425a5d16feb028feb6852c288ca57e2ce368f9`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6591b229ac39b0a53e12251a2fe42a2901e678310fcf812502f322b8ebffbc`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ac77a4f775631e8a22df96df0255ca63a127b4d396c770e7047005c95e56f3`  
		Last Modified: Mon, 16 Mar 2026 22:41:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:7e999d3f6ac25d48d115afe8244aeb322471dcc47475bb82e811b1ee28d40552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a415698b38797e4fbbe438f0f527ff62b3f2f37d4b066592992f9c0a7a05b8`

```dockerfile
```

-	Layers:
	-	`sha256:f90c682a553e5ae24bd9a6cfc979cf5d79c5f2081612f7bf6ae6cb200a8aa9d0`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1bc58a2c03801c0a00fa4488665ac6091f7a6cb453d195594f7ff9a358f5810`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 15.9 KB (15862 bytes)  
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
$ docker pull chronograf@sha256:e102126a7d8736cab70b31003927745fc88026f18ab4f5a1935f3d0f60f5d1e0
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
$ docker pull chronograf@sha256:a27e274b5f466e3c563c7e5a5ee0c8e1af1107ca9cbb4fe831c680217bde511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51127482bd078da1a95560067b7bb9aab2387fabb93ba3cb217afb3473ba91df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:39:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 16 Mar 2026 22:39:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:39:15 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:39:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:39:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf694cde0b5a4c07f4ab22f56c2596af607f667ba582a2a9448e94dd4997502d`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 5.2 MB (5241789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce2fff56f6a6568500fb7786fdb86ef26b490d8ebc6d95aa9cf6275c6e955`  
		Last Modified: Mon, 16 Mar 2026 22:39:26 GMT  
		Size: 35.0 MB (35011823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb051b030b13d6e1d5fd3d25fe815f21104fee9ae16760526287797779c6ad`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27daf5564635cf55fb3c7e1ef3361c02026b063bf7b032de7126ccb8397855`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8596f2c8a950db3b6e60419744469b3c508733c7b27eafa3e3b100d55baec43`  
		Last Modified: Mon, 16 Mar 2026 22:39:26 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:9068ab093364675be9c2b6dbd858d53c9b0c59f784e2e15cd4c12325a8fdcdd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e47febbac50430a26de65675796588a4f19161a655285d538be2415edf8ba58`

```dockerfile
```

-	Layers:
	-	`sha256:5ceb61e48e83e7b7f46542bdc80e2296b163732e407fa2aa539ce727166e8161`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b9e9d73234ba10d01a80800471700aca3ee11254c0545274d6d680da14b6cd`  
		Last Modified: Mon, 16 Mar 2026 22:39:25 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:231767f2a6c2a10b5b92b2aedf702c6de139d57614bbff2ccf2a21f5693afd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63397411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155f0b2f8133554ff7367a530ef9e230f4f9861d3bc3357ba2127d1914c5bccb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:22:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 16 Mar 2026 23:22:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 23:22:57 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 23:22:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:22:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:22:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3bc17afcb32786a635d7faf13a7aa3a4142ac1a648b659c697f5e02460592774`  
		Last Modified: Mon, 16 Mar 2026 21:52:44 GMT  
		Size: 25.6 MB (25551392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e182cbbd9ce751bb8b2a330f86b0acba56ce6e4b961b2fa966bc834ab8ed66`  
		Last Modified: Mon, 16 Mar 2026 23:23:06 GMT  
		Size: 4.5 MB (4510007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304ec9add4007a9a2353f44f47bac93f0137c935d50ec11f8f368137df8a3658`  
		Last Modified: Mon, 16 Mar 2026 23:23:06 GMT  
		Size: 33.3 MB (33311620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b22e647465c6b5910bd71f8f2f989074615b6bf512cc3bc8fa59c7835c081e`  
		Last Modified: Mon, 16 Mar 2026 23:23:05 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c502f7dda028fa78a15868b2a6e7f43023145b2336ac7571439862a24580c0`  
		Last Modified: Mon, 16 Mar 2026 23:23:05 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135d840a52ba2a23aaf3f30734dced78ca16fc07db649de1dbcdff02951a615`  
		Last Modified: Mon, 16 Mar 2026 23:23:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd6c5843822a3cc53dac5b8411c5473a76e90658e914c9c1b1f69ea857a7c105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abe68c638a62e94b949e8d40fd620b7c275d5a689a57eabfd3b30a7c3d75daa`

```dockerfile
```

-	Layers:
	-	`sha256:d5d022d8c0e3700bd6de60b9eb59cb4e8b44ffa78972a76c0ad12d67bca5aa2b`  
		Last Modified: Mon, 16 Mar 2026 23:23:06 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc05947686da96ccd883ed05e6e0898559cce23eecb76277a70ca40ca595f3d9`  
		Last Modified: Mon, 16 Mar 2026 23:23:05 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c946487837657a628f81a63ace8c9772d7da4b50e200156a34a1e6641cf5c95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67181112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc85fbf68d207955c3da996f1778b7ae88108339602b5714dc8bcdf2beb924b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:41:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 16 Mar 2026 22:41:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:41:07 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:41:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeec8b01f88aa125137a54b254e8437c7e832cdbeb18158be6dae84165ca160`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 5.2 MB (5229845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f75032ab63711c5c66c2c1b876e4fea7abf0d19da486dfafd11c8c9e2ad1bd`  
		Last Modified: Mon, 16 Mar 2026 22:41:18 GMT  
		Size: 33.2 MB (33182356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69527b2b87f7819c20e8bd492425a5d16feb028feb6852c288ca57e2ce368f9`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6591b229ac39b0a53e12251a2fe42a2901e678310fcf812502f322b8ebffbc`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ac77a4f775631e8a22df96df0255ca63a127b4d396c770e7047005c95e56f3`  
		Last Modified: Mon, 16 Mar 2026 22:41:18 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:7e999d3f6ac25d48d115afe8244aeb322471dcc47475bb82e811b1ee28d40552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a415698b38797e4fbbe438f0f527ff62b3f2f37d4b066592992f9c0a7a05b8`

```dockerfile
```

-	Layers:
	-	`sha256:f90c682a553e5ae24bd9a6cfc979cf5d79c5f2081612f7bf6ae6cb200a8aa9d0`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1bc58a2c03801c0a00fa4488665ac6091f7a6cb453d195594f7ff9a358f5810`  
		Last Modified: Mon, 16 Mar 2026 22:41:17 GMT  
		Size: 15.9 KB (15862 bytes)  
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
$ docker pull chronograf@sha256:81ae99d4b4545873d889ce321fb22f5953f31c745eefb5f3537714d63fbd91e5
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
$ docker pull chronograf@sha256:27519f63ca4898ef8ba285323e09fc616c0cb32276926d1c8869277937c677dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85008397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dba3598b178ecb4f435fa929493fcf3707c5d4a13ea918dea1cd4d813f60a44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 16 Mar 2026 22:39:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:39:09 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:39:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:39:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:09 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbf4623f75eb7fd26cd18da1dcf097bc72629733c4845e0f443afdfd02f5171`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 7.9 MB (7879797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e868813716e1ec569c7ede31f06e50226a75aef765936e5db3b98397d4b33e3`  
		Last Modified: Mon, 16 Mar 2026 22:39:22 GMT  
		Size: 48.9 MB (48867915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3769fec83e3c7d61bdd133e533add194b475101c6d0f3a7a36af85b72d47e651`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c660916672fff41690d2258d07676e84412871cbbf0f3bb7f4337bcd25987ea9`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1485265a9ac688e24a0588061f9c657800fc3c320bd65bb4c1ebb54ee267a7`  
		Last Modified: Mon, 16 Mar 2026 22:39:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:5ce28ceb177bacf5b9b70343c7ab22333b9611f321ac737af07110277902eb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc5d688036c5ce23a007e8d6ec9d580bc7068f95c38ccef8458f8deb6be9863`

```dockerfile
```

-	Layers:
	-	`sha256:1abc0e3b5f838bf9533a6ab770154a0e08494bbb5c0d6289d3b0f29287884f7f`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 2.9 MB (2855730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb21327530f8de8ab6998db7133dddd6c951c25c478d66b2f715b6153576162a`  
		Last Modified: Mon, 16 Mar 2026 22:39:20 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:874cd2ce56827414451a06623a8af4a57f5499474fbdd5e3387223eb29b8b304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc61433b41ed8783b3c117c6e7d501a34350241cf76da9dd453f9df261d7bb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:23:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 16 Mar 2026 23:23:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 23:23:28 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 23:23:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:23:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:23:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f16e25d1e14be872b31f0c356cd9f2b5f0690b0c25a741a42f504fdb415d48`  
		Last Modified: Mon, 16 Mar 2026 23:23:39 GMT  
		Size: 6.5 MB (6512156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03285ac7c555d51d606190238cf48900bb66136b9c1de803f2f5cce20f4cc1e`  
		Last Modified: Mon, 16 Mar 2026 23:23:40 GMT  
		Size: 46.3 MB (46320093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1036946a7677c4d604fa0e1fdc6c290a79677545ce6545a19a49423b9875f5b`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06a045f30758384ab07fd2581a6bc48138a2ecec9a31a07813abe9220f21a30`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e812d7ae19cd5f03dca2f564f797fcb1ff6bd3bb2f2035ed91cbcb7fbbd610e6`  
		Last Modified: Mon, 16 Mar 2026 23:23:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:8d9f4a452d88dbc953693edb1585f4446fcf0c164d4bb36ffd5ceeb2c32dab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be112a84b76f0d773bcaa67194129d9eb11c187f495dee1ce4457a44c2021024`

```dockerfile
```

-	Layers:
	-	`sha256:d8d5c777df0f4b73981bf7e1cb66c1334a40b0440e990f6ac8886f56826312e5`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da9a9d56ee2fbc0f2015279a5f68ce0be788f1b0b50a47ec6cf2c41609c33e6`  
		Last Modified: Mon, 16 Mar 2026 23:23:38 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:0a77c7b031acad2567f14cbdf90db3cbf2a5028e14cd9979c50c183003d3be85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81845997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da2d36f8026c0c84e1c5cf8850cfd4c4d22a2cc1c2a863da1d164e0a650292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Mon, 16 Mar 2026 22:41:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 16 Mar 2026 22:41:35 GMT
VOLUME [/var/lib/chronograf]
# Mon, 16 Mar 2026 22:41:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f09ae52ddab292a199a66a53c1d8d9371a78b17fcbb59abd71bcdbbb8b942`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 7.7 MB (7697010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c62ba20fbac9591d2f8893a5ff5b0a5eee129acb796a1eb6c9d6c43f669ef30`  
		Last Modified: Mon, 16 Mar 2026 22:41:47 GMT  
		Size: 46.0 MB (46008448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821d80786e58c4f7cf23898ca6fcbecb9ce4836595c303622523620a79a548df`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9aa47cd2c2eedfbd66c9f768588fe3fb791a46e3f0f49394d85c557c60d3fbb`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3ea67f5ce87af459bfc0e2a49b81a9c9d76ef6041c02c41bf0b9eb304dee2`  
		Last Modified: Mon, 16 Mar 2026 22:41:47 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c30aad004f940157e20dbf28485407b7c4e5d632e1192aefbe7427421ad2126a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5dd236a9182db4844b0d181db93a4d8548e75fc6d3e094f85f0f428ffc2979`

```dockerfile
```

-	Layers:
	-	`sha256:29ce36b13958c091d1aaf70efecf405baecc22341491ee6ef0af40dd5220adca`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 2.9 MB (2856003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624ea2a2909e178414bbc9d7f33e6ef39a87828ff87a45e4b5964dcc9066b654`  
		Last Modified: Mon, 16 Mar 2026 22:41:46 GMT  
		Size: 16.2 KB (16191 bytes)  
		MIME: application/vnd.in-toto+json
