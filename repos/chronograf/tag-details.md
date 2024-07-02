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
$ docker pull chronograf@sha256:029cbaf9f6234b7da9520f8769c6e5ca4bc9ca9bd17f292e765bbadccb5b36a6
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
$ docker pull chronograf@sha256:b9541a7c646b482265adb3c9d627378b2d83d4ef5859ed30d012d30022a69e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84239001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490904b34dc02839057ae9bbd784311b5af723278d9df8c708f1c507b715fc98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce26bc7a4c162f172c6ba2779c8e458ff17a75156594043161938df2ae44e890`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 7.9 MB (7871381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6f4fedc4074b8b78cc4fc2c448a1bb1a48b0186ec68a8e1023d4b3ee5d572`  
		Last Modified: Tue, 02 Jul 2024 03:02:27 GMT  
		Size: 47.2 MB (47216887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42720a1eb2786df8b8126407b28d597e10c985650a232048402ea700320245c2`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30b67d5c4bbc7cb1e9d9eb55ab6cba73f97e66fe0ed354db62f2c2cdecddc0`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2b163e95e68de39248cbea368139f04bd7d18059bf9d36f1ea5f6d216e6b`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:578d5793597937e1669c23efa44690d5183c3bd0a47d3b53414f6c059d640aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4dec00d335d5450ec69ddcdecc9993433b0175795b00ebc663eebae7103dd6`

```dockerfile
```

-	Layers:
	-	`sha256:467df9c611d592aa8b473bfd555940d0da4ed16b20be29e7ea9949e185113a24`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 2.7 MB (2655543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5989dafb2edf356430b4e7b198331be7faca9362e3b0ca011f097bf421c0fee`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a0435ce083bb756da6b06b35d004a6ac76fc037d1ee77edb26ad1d3abe4f331e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75514451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fc7a87206030dfffc1b51b1928616579e1fe843dc0b1cb95bef6a2b661f99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9c896caa2726afa387b9dbac529ecbb121f6e6a25d5e366c255900d9244b4d`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 6.5 MB (6495956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e0d3e9f0ae48de66aaa8921b76c9299e70974fb0ec1df0118bd4751a2655f8`  
		Last Modified: Tue, 02 Jul 2024 06:36:49 GMT  
		Size: 44.3 MB (44275865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8282e6619a76bfea913cda577cae5b5473eb0719794b3e3a62e4fdb445144a2`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd8f2f723f0513c18e767b3af2973c74e5d4c51950fc8942ae91d5bdefd884`  
		Last Modified: Tue, 02 Jul 2024 06:36:49 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877c004bdbf6a2829789712a2844bab48756799d1c46e319d425d1f6486de11`  
		Last Modified: Tue, 02 Jul 2024 06:36:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:779eacc0c1883eba90afff28b60dcdd2f1617791ce8647ab6bee762712b5b19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85635c702deafbb01bff1c75af329dce91f9a2d98f3b89c4d81c1710116844e8`

```dockerfile
```

-	Layers:
	-	`sha256:a02c71c637b3db2ebca897158751cd9dbf2b7f6a1df5e980cb035a7faa1005f9`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 2.7 MB (2657839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed70aab04800dec2c9605fc11ba5d3bd4d8b2b745a9aacbd6ad74a6b2aa7474c`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2509b79f21f8d2f01cc6fb1787c60e192cedbaa1c3a0df512f250cef530831b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81628369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0abb98411db0e43a2472ca9a04e405f3988fda0221fc73309073c33d3f1e22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c44ee98f21bfee7c5d1f4a14f776fde4841c39b3768dd1ef9237f050a1c7e`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 7.5 MB (7453190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1353d59f878028d1e53f5b9ba7ff5ffc15eba37b01f82eb05dd966d56edd38d`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 45.0 MB (44971054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf276b9e8fbbd0dcc962675f697db83c1ae8c2bddaca1cb5c11c46971d74c7`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6dd95139e23cb8a4d10dad60fa476b92f5a9145a7dd7065456fe757ca3a31`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91708736b0c8e603f3424312a2afcaa5a538aa78627f508d8c4987f3ed15b722`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:cd716da942a514ab19d44c83fa585a1630ed5119a82b7e3f88ebe30d0925a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1778fda725b4d6774f106bdc18c6d9b53fc21bdb277af9413e686b3ad5f1441`

```dockerfile
```

-	Layers:
	-	`sha256:f3e3f8f7212f21dc6670ffb3733e2c1980e6bc43ea569b9fd42cf0084277c5c9`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 2.7 MB (2655786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd3e10071bb448a595fd2dac1ecd5a65e785f3fad6449fd2bc71fbcbbe02612`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 16.2 KB (16230 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:984d3beb716dbfd933b376d3a11c8cde64589d7e5808a0539aebc245018da6de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:07c647f252815f58012c9080fb27389864deeaf76c7c87966cf06ff058212c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31809610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abdedc468f1ceb9e469bbeeaf13b3df35ad006916a805f4e88b28973f090ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca434a5221442ebfb3dbc3b9c9345f539777fcce196f9953179c35ed4c20b8`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3846ce7e00dea64b371302742d345d5d8bb344f7a56b72962a3afba74b2ee0d2`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 294.3 KB (294344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0514f13c9e2d24d9d2c294215739da77b2facca8d45dc71ce567f3d58710b`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 27.9 MB (27866719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2114a0ab5cba7eb6b946de96d6b5683da1695cdcdc11a4c871da4f27a376b`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a0dc96f976b28a9956775a14d182bc7f8632f322fbdd55ec3f90f89140148b`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db878d5004db02d508ab4fe22d6f8b1c26cebf9fb27103a529508b6c866e40`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0ca449aa846286bc7d47ab5fbd21720b9b09aba4cd9c9f446952fa94951a97c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18078ceb4ff8c5c6e5c418434c411b41e90728bc1f1692585634ee0a4370eb0d`

```dockerfile
```

-	Layers:
	-	`sha256:7ebbda34b238dac5156e27fdc39d2906e77398c4d00e55e963fd947eda6b3789`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 226.9 KB (226904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d242d1ae488c04ce12d615444f295341e10602467dfdeae021b8bb1becf01a9c`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:029cbaf9f6234b7da9520f8769c6e5ca4bc9ca9bd17f292e765bbadccb5b36a6
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
$ docker pull chronograf@sha256:b9541a7c646b482265adb3c9d627378b2d83d4ef5859ed30d012d30022a69e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84239001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490904b34dc02839057ae9bbd784311b5af723278d9df8c708f1c507b715fc98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce26bc7a4c162f172c6ba2779c8e458ff17a75156594043161938df2ae44e890`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 7.9 MB (7871381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6f4fedc4074b8b78cc4fc2c448a1bb1a48b0186ec68a8e1023d4b3ee5d572`  
		Last Modified: Tue, 02 Jul 2024 03:02:27 GMT  
		Size: 47.2 MB (47216887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42720a1eb2786df8b8126407b28d597e10c985650a232048402ea700320245c2`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30b67d5c4bbc7cb1e9d9eb55ab6cba73f97e66fe0ed354db62f2c2cdecddc0`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2b163e95e68de39248cbea368139f04bd7d18059bf9d36f1ea5f6d216e6b`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:578d5793597937e1669c23efa44690d5183c3bd0a47d3b53414f6c059d640aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4dec00d335d5450ec69ddcdecc9993433b0175795b00ebc663eebae7103dd6`

```dockerfile
```

-	Layers:
	-	`sha256:467df9c611d592aa8b473bfd555940d0da4ed16b20be29e7ea9949e185113a24`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 2.7 MB (2655543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5989dafb2edf356430b4e7b198331be7faca9362e3b0ca011f097bf421c0fee`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a0435ce083bb756da6b06b35d004a6ac76fc037d1ee77edb26ad1d3abe4f331e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75514451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fc7a87206030dfffc1b51b1928616579e1fe843dc0b1cb95bef6a2b661f99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9c896caa2726afa387b9dbac529ecbb121f6e6a25d5e366c255900d9244b4d`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 6.5 MB (6495956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e0d3e9f0ae48de66aaa8921b76c9299e70974fb0ec1df0118bd4751a2655f8`  
		Last Modified: Tue, 02 Jul 2024 06:36:49 GMT  
		Size: 44.3 MB (44275865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8282e6619a76bfea913cda577cae5b5473eb0719794b3e3a62e4fdb445144a2`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd8f2f723f0513c18e767b3af2973c74e5d4c51950fc8942ae91d5bdefd884`  
		Last Modified: Tue, 02 Jul 2024 06:36:49 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877c004bdbf6a2829789712a2844bab48756799d1c46e319d425d1f6486de11`  
		Last Modified: Tue, 02 Jul 2024 06:36:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:779eacc0c1883eba90afff28b60dcdd2f1617791ce8647ab6bee762712b5b19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85635c702deafbb01bff1c75af329dce91f9a2d98f3b89c4d81c1710116844e8`

```dockerfile
```

-	Layers:
	-	`sha256:a02c71c637b3db2ebca897158751cd9dbf2b7f6a1df5e980cb035a7faa1005f9`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 2.7 MB (2657839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed70aab04800dec2c9605fc11ba5d3bd4d8b2b745a9aacbd6ad74a6b2aa7474c`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2509b79f21f8d2f01cc6fb1787c60e192cedbaa1c3a0df512f250cef530831b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81628369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0abb98411db0e43a2472ca9a04e405f3988fda0221fc73309073c33d3f1e22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c44ee98f21bfee7c5d1f4a14f776fde4841c39b3768dd1ef9237f050a1c7e`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 7.5 MB (7453190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1353d59f878028d1e53f5b9ba7ff5ffc15eba37b01f82eb05dd966d56edd38d`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 45.0 MB (44971054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf276b9e8fbbd0dcc962675f697db83c1ae8c2bddaca1cb5c11c46971d74c7`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6dd95139e23cb8a4d10dad60fa476b92f5a9145a7dd7065456fe757ca3a31`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91708736b0c8e603f3424312a2afcaa5a538aa78627f508d8c4987f3ed15b722`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:cd716da942a514ab19d44c83fa585a1630ed5119a82b7e3f88ebe30d0925a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1778fda725b4d6774f106bdc18c6d9b53fc21bdb277af9413e686b3ad5f1441`

```dockerfile
```

-	Layers:
	-	`sha256:f3e3f8f7212f21dc6670ffb3733e2c1980e6bc43ea569b9fd42cf0084277c5c9`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 2.7 MB (2655786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd3e10071bb448a595fd2dac1ecd5a65e785f3fad6449fd2bc71fbcbbe02612`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 16.2 KB (16230 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:984d3beb716dbfd933b376d3a11c8cde64589d7e5808a0539aebc245018da6de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:07c647f252815f58012c9080fb27389864deeaf76c7c87966cf06ff058212c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31809610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abdedc468f1ceb9e469bbeeaf13b3df35ad006916a805f4e88b28973f090ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca434a5221442ebfb3dbc3b9c9345f539777fcce196f9953179c35ed4c20b8`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3846ce7e00dea64b371302742d345d5d8bb344f7a56b72962a3afba74b2ee0d2`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 294.3 KB (294344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0514f13c9e2d24d9d2c294215739da77b2facca8d45dc71ce567f3d58710b`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 27.9 MB (27866719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2114a0ab5cba7eb6b946de96d6b5683da1695cdcdc11a4c871da4f27a376b`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a0dc96f976b28a9956775a14d182bc7f8632f322fbdd55ec3f90f89140148b`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db878d5004db02d508ab4fe22d6f8b1c26cebf9fb27103a529508b6c866e40`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0ca449aa846286bc7d47ab5fbd21720b9b09aba4cd9c9f446952fa94951a97c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18078ceb4ff8c5c6e5c418434c411b41e90728bc1f1692585634ee0a4370eb0d`

```dockerfile
```

-	Layers:
	-	`sha256:7ebbda34b238dac5156e27fdc39d2906e77398c4d00e55e963fd947eda6b3789`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 226.9 KB (226904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d242d1ae488c04ce12d615444f295341e10602467dfdeae021b8bb1becf01a9c`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:cf3124dfaf6a6acffbb282d5021a3f00c530b9b993128be20c9db39613bd27dd
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
$ docker pull chronograf@sha256:18d8d86fc79758b8e42c2ea4235590dad6f36bfc9cfe3e22ef6a824f0f326068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70394254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e821e8677fbec8deff740cb40887b2f519051fb6ef1fbda3d999563ddaf45e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d03200620a85b8d68ee4ac109f6252d73a403d607e16e0f10813e7dfd3498b9`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 4.2 MB (4209319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25e716a0c082618a98a10004c870137bdbbe70351510c6b53c3c58bb7751653`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 34.7 MB (34738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e43d8bce324b27e1dd03594aa7f44d5aeeaa8a5b9aef44e427674e9f6b1fc1`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b043149ee1d2ca77e463e68d7eebcb6eb2f57e40765af889b2e4c724fc84ec25`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6113bf7e13bba7ab693b60981ed9ba4908f5cffe9776e14a13f9a6ff7385da8`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:74a5ca7627dd3dcd5e261ab399d2884656bc5f094bd753b2a77d869fe694622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4c0bbe9335b7c74a16a20a0157219e1ec72f360b791b13fd89bb2c3a05f02`

```dockerfile
```

-	Layers:
	-	`sha256:adbd682460e7313b81f708f9bef6f9ea47762121e612dfeba64db07dd6556d86`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 2.9 MB (2867288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b4fedf782965796bd1592d3af448506ec39de9d7e5d1e4d135b7e87d6aa6eb2`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:45b47e78335927082b092febfc70ed900691d5ff88659b1ffd6dae165b3c2839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63216035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c99ac4589d71b40d7b05480a1b2ece22881f64469a2db09fbeb9a7b4ac8f81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
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
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128b2e32178b1f07e23a1963898f20536abf450fc0e8ac9d8d2a046e9e744d0f`  
		Last Modified: Tue, 02 Jul 2024 04:54:57 GMT  
		Size: 3.5 MB (3511495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055666e5bee70fb6f5c58eed514a59751db6b8e7f4025b5f329ae5b64b2c554b`  
		Last Modified: Tue, 02 Jul 2024 04:54:58 GMT  
		Size: 33.1 MB (33097439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1edaae9172ae456d57d678c4abac47b0d5ba4a034db6e79d859a760d9f06f`  
		Last Modified: Tue, 02 Jul 2024 04:54:57 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3301bcd966079787fc6b883aae82f75933d52ef0fb01caea702fb0b3cd3ea9f`  
		Last Modified: Tue, 02 Jul 2024 04:54:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7a9db496495692f1ba209ad2be9139537a506a06826a7e2c2a10daaa69a0f`  
		Last Modified: Tue, 02 Jul 2024 04:54:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:9d63b50f3365eb7f56f337dba45daf2e8a87a67cecfad2368cc4eb4337b1a58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e97f5ec9ae677103f3d0a817f853a4e3900c00010bf9f20e87b1d15965fd802`

```dockerfile
```

-	Layers:
	-	`sha256:c4429774481465665716a9ccb7abf6890c78968ba953de00317e7220345a89b8`  
		Last Modified: Tue, 02 Jul 2024 04:54:57 GMT  
		Size: 2.9 MB (2869558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb2a773cf18233c85cdb13608953b052fef007d1ea19e56f893f65dbd93cd67`  
		Last Modified: Tue, 02 Jul 2024 04:54:57 GMT  
		Size: 15.7 KB (15650 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5a189457a4964185a65a2a1d6d6c3c1d2db507466c49135b1f74424a4cdaf828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67355818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9c267055303d21cdaca86881e279f2d208b80964f55576da91fdb916363886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c8db4492f9f092c550f5ffb33afd2d670d2b138f83d90b8b8a69d7e9b1fec2`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 4.2 MB (4210560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca33934a7cbc211a45559871136f7c60f01f796fb536d63dc036173814faf236`  
		Last Modified: Thu, 13 Jun 2024 08:44:33 GMT  
		Size: 33.0 MB (33033891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96932bde717aa7cebd87911175141b352c136580456aa23dcb72516623588ed1`  
		Last Modified: Thu, 13 Jun 2024 08:44:31 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01523c2ad47ed495e4192d57a1f4f25cf64b250f9b173a87a4e8d378c62f22a1`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4792d4db8a65302c0b0963b8e8559d7e6ef32bad62d4610f037aac8e0edd38b2`  
		Last Modified: Thu, 13 Jun 2024 08:44:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:d6b789e80c41b570391981557b35d3c0ee8b386b24274358088320b71ccaf6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b75d0f914bf542c53e473755fa81ae9ce94b8ffd80eedfd68549562c9dd16b`

```dockerfile
```

-	Layers:
	-	`sha256:6564687ae3dc3ab0d1ae7e9828d8f6a9e8c1fb7cd2462b5d3b3b6388e95d075f`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 2.9 MB (2867497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcbcad728ed505b86f2a4428c05f3c6531b9b9a0afd66eca17a99300ee8f19e`  
		Last Modified: Thu, 13 Jun 2024 08:44:31 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:dc2b77860c0d9abfddd4258d195e6dd8c6f57a0060ae4647d9d87f6937896948
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c36158fd878791c4d6864fa6b2e2277dcf1844b101f7f4283f89d736ff83a9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23497563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6b49bfc7612e66500d912d8017a01ef224a5be1cb4f7ded6adc4d0b7ce2158`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f32acfd72a12dc339f5b67752df209abba35968e2f6767bb155cc38c863e80`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc85f7f1b607ca59d6e9b0110ccb2be09486e02421a92e2c39a476d8b1745856`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 292.4 KB (292421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5d7db5d6ddfd0cd4fbda7af34544cd04c79cea81bd0af193b5db7fbcc9e5f1`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 19.6 MB (19556647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4223beda7e146770a4515e659b5b8a8bd3d7f8a5bbaf860e16a31929e6dc37ac`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d37efecd7efe3732d8c20b4b35a0e25feaa735ad23c89d13a4986a044dab79`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef57d29558f1c9c7d0680de713565169dbd0126ad21cda447b8d601be9a6585`  
		Last Modified: Thu, 20 Jun 2024 20:54:51 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:9a53967224df07b8a0d0e21be398099bc414c300176c72388d5f6f75017b6b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 KB (185257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9823cb0b1245d5d5c8ac0c017d9ea0e9f911d66cb070fd49fc62ff8ae236ea79`

```dockerfile
```

-	Layers:
	-	`sha256:d451d0df30ae1f6a59569670946d7f2c26fec3122e3a18af7c6af6510d2959fc`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 168.6 KB (168560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34aa34bbd0423b5929e99546a0dc42aab460d59d888514532fa2ff925b726ed6`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:cf3124dfaf6a6acffbb282d5021a3f00c530b9b993128be20c9db39613bd27dd
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
$ docker pull chronograf@sha256:18d8d86fc79758b8e42c2ea4235590dad6f36bfc9cfe3e22ef6a824f0f326068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70394254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e821e8677fbec8deff740cb40887b2f519051fb6ef1fbda3d999563ddaf45e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d03200620a85b8d68ee4ac109f6252d73a403d607e16e0f10813e7dfd3498b9`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 4.2 MB (4209319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25e716a0c082618a98a10004c870137bdbbe70351510c6b53c3c58bb7751653`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 34.7 MB (34738263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e43d8bce324b27e1dd03594aa7f44d5aeeaa8a5b9aef44e427674e9f6b1fc1`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b043149ee1d2ca77e463e68d7eebcb6eb2f57e40765af889b2e4c724fc84ec25`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6113bf7e13bba7ab693b60981ed9ba4908f5cffe9776e14a13f9a6ff7385da8`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:74a5ca7627dd3dcd5e261ab399d2884656bc5f094bd753b2a77d869fe694622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b4c0bbe9335b7c74a16a20a0157219e1ec72f360b791b13fd89bb2c3a05f02`

```dockerfile
```

-	Layers:
	-	`sha256:adbd682460e7313b81f708f9bef6f9ea47762121e612dfeba64db07dd6556d86`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 2.9 MB (2867288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b4fedf782965796bd1592d3af448506ec39de9d7e5d1e4d135b7e87d6aa6eb2`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:45b47e78335927082b092febfc70ed900691d5ff88659b1ffd6dae165b3c2839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63216035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c99ac4589d71b40d7b05480a1b2ece22881f64469a2db09fbeb9a7b4ac8f81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
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
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128b2e32178b1f07e23a1963898f20536abf450fc0e8ac9d8d2a046e9e744d0f`  
		Last Modified: Tue, 02 Jul 2024 04:54:57 GMT  
		Size: 3.5 MB (3511495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055666e5bee70fb6f5c58eed514a59751db6b8e7f4025b5f329ae5b64b2c554b`  
		Last Modified: Tue, 02 Jul 2024 04:54:58 GMT  
		Size: 33.1 MB (33097439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1edaae9172ae456d57d678c4abac47b0d5ba4a034db6e79d859a760d9f06f`  
		Last Modified: Tue, 02 Jul 2024 04:54:57 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3301bcd966079787fc6b883aae82f75933d52ef0fb01caea702fb0b3cd3ea9f`  
		Last Modified: Tue, 02 Jul 2024 04:54:58 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7a9db496495692f1ba209ad2be9139537a506a06826a7e2c2a10daaa69a0f`  
		Last Modified: Tue, 02 Jul 2024 04:54:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:9d63b50f3365eb7f56f337dba45daf2e8a87a67cecfad2368cc4eb4337b1a58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2885208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e97f5ec9ae677103f3d0a817f853a4e3900c00010bf9f20e87b1d15965fd802`

```dockerfile
```

-	Layers:
	-	`sha256:c4429774481465665716a9ccb7abf6890c78968ba953de00317e7220345a89b8`  
		Last Modified: Tue, 02 Jul 2024 04:54:57 GMT  
		Size: 2.9 MB (2869558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb2a773cf18233c85cdb13608953b052fef007d1ea19e56f893f65dbd93cd67`  
		Last Modified: Tue, 02 Jul 2024 04:54:57 GMT  
		Size: 15.7 KB (15650 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5a189457a4964185a65a2a1d6d6c3c1d2db507466c49135b1f74424a4cdaf828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67355818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9c267055303d21cdaca86881e279f2d208b80964f55576da91fdb916363886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c8db4492f9f092c550f5ffb33afd2d670d2b138f83d90b8b8a69d7e9b1fec2`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 4.2 MB (4210560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca33934a7cbc211a45559871136f7c60f01f796fb536d63dc036173814faf236`  
		Last Modified: Thu, 13 Jun 2024 08:44:33 GMT  
		Size: 33.0 MB (33033891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96932bde717aa7cebd87911175141b352c136580456aa23dcb72516623588ed1`  
		Last Modified: Thu, 13 Jun 2024 08:44:31 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01523c2ad47ed495e4192d57a1f4f25cf64b250f9b173a87a4e8d378c62f22a1`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4792d4db8a65302c0b0963b8e8559d7e6ef32bad62d4610f037aac8e0edd38b2`  
		Last Modified: Thu, 13 Jun 2024 08:44:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:d6b789e80c41b570391981557b35d3c0ee8b386b24274358088320b71ccaf6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b75d0f914bf542c53e473755fa81ae9ce94b8ffd80eedfd68549562c9dd16b`

```dockerfile
```

-	Layers:
	-	`sha256:6564687ae3dc3ab0d1ae7e9828d8f6a9e8c1fb7cd2462b5d3b3b6388e95d075f`  
		Last Modified: Thu, 13 Jun 2024 08:44:32 GMT  
		Size: 2.9 MB (2867497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcbcad728ed505b86f2a4428c05f3c6531b9b9a0afd66eca17a99300ee8f19e`  
		Last Modified: Thu, 13 Jun 2024 08:44:31 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:dc2b77860c0d9abfddd4258d195e6dd8c6f57a0060ae4647d9d87f6937896948
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c36158fd878791c4d6864fa6b2e2277dcf1844b101f7f4283f89d736ff83a9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23497563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6b49bfc7612e66500d912d8017a01ef224a5be1cb4f7ded6adc4d0b7ce2158`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f32acfd72a12dc339f5b67752df209abba35968e2f6767bb155cc38c863e80`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc85f7f1b607ca59d6e9b0110ccb2be09486e02421a92e2c39a476d8b1745856`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 292.4 KB (292421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5d7db5d6ddfd0cd4fbda7af34544cd04c79cea81bd0af193b5db7fbcc9e5f1`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 19.6 MB (19556647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4223beda7e146770a4515e659b5b8a8bd3d7f8a5bbaf860e16a31929e6dc37ac`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d37efecd7efe3732d8c20b4b35a0e25feaa735ad23c89d13a4986a044dab79`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef57d29558f1c9c7d0680de713565169dbd0126ad21cda447b8d601be9a6585`  
		Last Modified: Thu, 20 Jun 2024 20:54:51 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:9a53967224df07b8a0d0e21be398099bc414c300176c72388d5f6f75017b6b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 KB (185257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9823cb0b1245d5d5c8ac0c017d9ea0e9f911d66cb070fd49fc62ff8ae236ea79`

```dockerfile
```

-	Layers:
	-	`sha256:d451d0df30ae1f6a59569670946d7f2c26fec3122e3a18af7c6af6510d2959fc`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 168.6 KB (168560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34aa34bbd0423b5929e99546a0dc42aab460d59d888514532fa2ff925b726ed6`  
		Last Modified: Thu, 20 Jun 2024 20:54:49 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:4262782455e235e75ae234ec5bb0da9494c85c9a761084c6b2c6add43356655d
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
$ docker pull chronograf@sha256:8532cd6f5153f19f7ec2e6e1d002043260f7c0a3f080c08a7ac417a2f2a69dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71034955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a0bde67d71ac2fa0fef0fcd040b82494bb9c371564de8b88dde63c1a46a7a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012bdf303913935004591df45c854454fe1e9a2ba553e02b4d6015cce53b74`  
		Last Modified: Tue, 02 Jul 2024 03:02:35 GMT  
		Size: 5.2 MB (5224233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcac90ce2ea280e46dca89a8aa1707a35121e57ae389e7e9e48c3ba4b99cbd74`  
		Last Modified: Tue, 02 Jul 2024 03:02:35 GMT  
		Size: 34.4 MB (34364063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54e3415265306b81f205c11865271d0f970636e75a9b33e8df5e6b8628b299`  
		Last Modified: Tue, 02 Jul 2024 03:02:34 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2640547b6be962ebd6cbc3d5b8e18c4ab913a4d7e939caad797b7eceb6d866a`  
		Last Modified: Tue, 02 Jul 2024 03:02:35 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555e4c087192ab363950406027e8aba27d605cf6ebec05af5becd32fd132171e`  
		Last Modified: Tue, 02 Jul 2024 03:02:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:4dfc092838886f55aa3d5babd7ea886ddd9684de0b2266665bdc5efbc33b90f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2930572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727c5af4b25d15450727a94db4453348c36531012887cde2a2724f5b9bcf1e9c`

```dockerfile
```

-	Layers:
	-	`sha256:adde2282f702164f380368499b3140efdfa5f349fab02616bf3158cb686bd4b9`  
		Last Modified: Tue, 02 Jul 2024 03:02:35 GMT  
		Size: 2.9 MB (2914949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b891e622bde4bb7170fc1ea573cf82c68594d19063e8086e1709566f2e1d48e`  
		Last Modified: Tue, 02 Jul 2024 03:02:34 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:202ed5f085aa9da810ec55188f16d3c61db5382ae75df227e5d412a75e47bb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63631867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3891e77c1ee2d58bd9175daa7554cc58a2d043d82a08b1296b94647c8862f126`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
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
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa53d5c68a74e2caa2b0922c6ce751b2f1fe854e1362fef70dfcf8bfbb64faa`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 4.5 MB (4490082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c02d0fc8ef39125e674e952387787d9eec6c850603939ac380cd6782f5430e8`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 32.5 MB (32534681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d840977935ecebd0985c3f4ef3742a5cf3c65b802a42504f788efea8c48bc104`  
		Last Modified: Tue, 02 Jul 2024 06:34:38 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b71d5559830267ab7a408e21e4149cdeed4686bf0120cf044d63a2e334f8c6e`  
		Last Modified: Tue, 02 Jul 2024 06:34:38 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f304ef9271c9bd27d5c9b043d158d87075f5bb33ba0654f6c7195545d1dad`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:71ea812af862ccc9c78521c339dc9e73a166e62d643fbdfd16e244c5b8919365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61b0ad7f5d3d7bb4389ee918c6b2e50667fa91dd46e0a41ef48b42994492e2`

```dockerfile
```

-	Layers:
	-	`sha256:929f8b827d70059daf7ee56fd0a3872a79b0337af28be75ebe9bb43c347693fb`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 2.9 MB (2917219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8b4b9dc5e3924bb8b3a0c548554be57e181428c027bb449dbc128573b2ca2b`  
		Last Modified: Tue, 02 Jul 2024 06:34:38 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:91aae5d8912885c88287b065515265162286007c187c648361ed8b47cc99f3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67544910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d7a5d74734ac0e44525de668af66d1c8a820511af4d2e35028e5d5de72473b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198db4c78d05a7fae6481f1f23e9abd0f4bd589e25e5b4afa53b8cb416bbfc7`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 5.0 MB (5004108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0299cfd86fa3f79a7004d1cce8b56dde224addfbd665488e4ca70acc75d20470`  
		Last Modified: Thu, 13 Jun 2024 10:39:05 GMT  
		Size: 32.4 MB (32429432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352c9608ddcf2ce9b44f0b0aaf9a71dbf0a7d9d83dd4c946e20c4bb07a21ce7c`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebdc4ba22b8ea39106433506e2f36daae588229d50644f58ff2347feaa7bdc3`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e98413252a072b47934a947e3ff659675761a772b2098a242888f8876feaf`  
		Last Modified: Thu, 13 Jun 2024 10:39:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:f84cd02a12ebfbf384a8f5228f5a9bb7e90f0d010b65917008dc506c8d61e53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6c2de8e3269574d9287fcc9e73e6428b5b977210e3fa490bbc7b86f5c033be`

```dockerfile
```

-	Layers:
	-	`sha256:6d9f8b4d656f1021b4fc951ad5021fd727a0f2d9868dc178776008ea2e8d2588`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 2.9 MB (2915158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:669b39bb1e5a6a4645a76705f6123148de76ad978dc395af0a5542509ae8f98f`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:74741dcda03510261b292d954dc23d09506056013bc25465d72f3a16f5f06dd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ac477289528eeac0d6192db0f553a5e6d587f0b93363cf4349663ef9d70fa207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23144946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8fb9b8769e568db43512e64bb05ceb44bdbd0aa0b617a0dd344d1c2f24b757`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca434a5221442ebfb3dbc3b9c9345f539777fcce196f9953179c35ed4c20b8`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec692b23ce3f06736c77304d50d358747add2ed9d109a0798a58ce8e6aa20e02`  
		Last Modified: Thu, 20 Jun 2024 20:55:40 GMT  
		Size: 292.4 KB (292418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac37fcb0b27a6d29519d90fd44133c2ad7b7c2a1fdbdd1264a36008669d8e05`  
		Last Modified: Thu, 20 Jun 2024 20:56:56 GMT  
		Size: 19.2 MB (19204032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd663a9d259dd1d14d41e02fe24cf0224b441e1e3ce4b2978e8ccd2483436a15`  
		Last Modified: Thu, 20 Jun 2024 20:56:55 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3446f4edde6d8d89b416064a9e722690ac3e294bc434b4d8b0b784825f119744`  
		Last Modified: Thu, 20 Jun 2024 20:56:55 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ce9d83f97f733ed27f9c9b3a01f5d62b680add1852cf5737d0078d15322cf`  
		Last Modified: Thu, 20 Jun 2024 20:56:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:5cb763be9da459e5ed7e0505b0073241c8e3a0ae37e0d3ea2ad0050c3980a991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 KB (233579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7795127d92bef4efc1d41bc689a1330bba955f9dc387cc021f6ccca60f4af512`

```dockerfile
```

-	Layers:
	-	`sha256:b1fe8b7ea701a68a0a6b773a59e2faa0804ed3032832fdcca03bb3eaa8ffda23`  
		Last Modified: Thu, 20 Jun 2024 20:56:55 GMT  
		Size: 216.9 KB (216882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eece67b5983a18ad16e61a01996f46de33cdb81d0062ae19b6e8f6de48ee473e`  
		Last Modified: Thu, 20 Jun 2024 20:56:55 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:4262782455e235e75ae234ec5bb0da9494c85c9a761084c6b2c6add43356655d
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
$ docker pull chronograf@sha256:8532cd6f5153f19f7ec2e6e1d002043260f7c0a3f080c08a7ac417a2f2a69dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71034955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a0bde67d71ac2fa0fef0fcd040b82494bb9c371564de8b88dde63c1a46a7a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd012bdf303913935004591df45c854454fe1e9a2ba553e02b4d6015cce53b74`  
		Last Modified: Tue, 02 Jul 2024 03:02:35 GMT  
		Size: 5.2 MB (5224233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcac90ce2ea280e46dca89a8aa1707a35121e57ae389e7e9e48c3ba4b99cbd74`  
		Last Modified: Tue, 02 Jul 2024 03:02:35 GMT  
		Size: 34.4 MB (34364063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d54e3415265306b81f205c11865271d0f970636e75a9b33e8df5e6b8628b299`  
		Last Modified: Tue, 02 Jul 2024 03:02:34 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2640547b6be962ebd6cbc3d5b8e18c4ab913a4d7e939caad797b7eceb6d866a`  
		Last Modified: Tue, 02 Jul 2024 03:02:35 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555e4c087192ab363950406027e8aba27d605cf6ebec05af5becd32fd132171e`  
		Last Modified: Tue, 02 Jul 2024 03:02:36 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:4dfc092838886f55aa3d5babd7ea886ddd9684de0b2266665bdc5efbc33b90f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2930572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727c5af4b25d15450727a94db4453348c36531012887cde2a2724f5b9bcf1e9c`

```dockerfile
```

-	Layers:
	-	`sha256:adde2282f702164f380368499b3140efdfa5f349fab02616bf3158cb686bd4b9`  
		Last Modified: Tue, 02 Jul 2024 03:02:35 GMT  
		Size: 2.9 MB (2914949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b891e622bde4bb7170fc1ea573cf82c68594d19063e8086e1709566f2e1d48e`  
		Last Modified: Tue, 02 Jul 2024 03:02:34 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:202ed5f085aa9da810ec55188f16d3c61db5382ae75df227e5d412a75e47bb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63631867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3891e77c1ee2d58bd9175daa7554cc58a2d043d82a08b1296b94647c8862f126`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
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
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa53d5c68a74e2caa2b0922c6ce751b2f1fe854e1362fef70dfcf8bfbb64faa`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 4.5 MB (4490082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c02d0fc8ef39125e674e952387787d9eec6c850603939ac380cd6782f5430e8`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 32.5 MB (32534681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d840977935ecebd0985c3f4ef3742a5cf3c65b802a42504f788efea8c48bc104`  
		Last Modified: Tue, 02 Jul 2024 06:34:38 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b71d5559830267ab7a408e21e4149cdeed4686bf0120cf044d63a2e334f8c6e`  
		Last Modified: Tue, 02 Jul 2024 06:34:38 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f304ef9271c9bd27d5c9b043d158d87075f5bb33ba0654f6c7195545d1dad`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:71ea812af862ccc9c78521c339dc9e73a166e62d643fbdfd16e244c5b8919365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61b0ad7f5d3d7bb4389ee918c6b2e50667fa91dd46e0a41ef48b42994492e2`

```dockerfile
```

-	Layers:
	-	`sha256:929f8b827d70059daf7ee56fd0a3872a79b0337af28be75ebe9bb43c347693fb`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 2.9 MB (2917219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8b4b9dc5e3924bb8b3a0c548554be57e181428c027bb449dbc128573b2ca2b`  
		Last Modified: Tue, 02 Jul 2024 06:34:38 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:91aae5d8912885c88287b065515265162286007c187c648361ed8b47cc99f3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67544910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d7a5d74734ac0e44525de668af66d1c8a820511af4d2e35028e5d5de72473b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198db4c78d05a7fae6481f1f23e9abd0f4bd589e25e5b4afa53b8cb416bbfc7`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 5.0 MB (5004108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0299cfd86fa3f79a7004d1cce8b56dde224addfbd665488e4ca70acc75d20470`  
		Last Modified: Thu, 13 Jun 2024 10:39:05 GMT  
		Size: 32.4 MB (32429432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352c9608ddcf2ce9b44f0b0aaf9a71dbf0a7d9d83dd4c946e20c4bb07a21ce7c`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebdc4ba22b8ea39106433506e2f36daae588229d50644f58ff2347feaa7bdc3`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e98413252a072b47934a947e3ff659675761a772b2098a242888f8876feaf`  
		Last Modified: Thu, 13 Jun 2024 10:39:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:f84cd02a12ebfbf384a8f5228f5a9bb7e90f0d010b65917008dc506c8d61e53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6c2de8e3269574d9287fcc9e73e6428b5b977210e3fa490bbc7b86f5c033be`

```dockerfile
```

-	Layers:
	-	`sha256:6d9f8b4d656f1021b4fc951ad5021fd727a0f2d9868dc178776008ea2e8d2588`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 2.9 MB (2915158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:669b39bb1e5a6a4645a76705f6123148de76ad978dc395af0a5542509ae8f98f`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:74741dcda03510261b292d954dc23d09506056013bc25465d72f3a16f5f06dd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ac477289528eeac0d6192db0f553a5e6d587f0b93363cf4349663ef9d70fa207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23144946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8fb9b8769e568db43512e64bb05ceb44bdbd0aa0b617a0dd344d1c2f24b757`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca434a5221442ebfb3dbc3b9c9345f539777fcce196f9953179c35ed4c20b8`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec692b23ce3f06736c77304d50d358747add2ed9d109a0798a58ce8e6aa20e02`  
		Last Modified: Thu, 20 Jun 2024 20:55:40 GMT  
		Size: 292.4 KB (292418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac37fcb0b27a6d29519d90fd44133c2ad7b7c2a1fdbdd1264a36008669d8e05`  
		Last Modified: Thu, 20 Jun 2024 20:56:56 GMT  
		Size: 19.2 MB (19204032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd663a9d259dd1d14d41e02fe24cf0224b441e1e3ce4b2978e8ccd2483436a15`  
		Last Modified: Thu, 20 Jun 2024 20:56:55 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3446f4edde6d8d89b416064a9e722690ac3e294bc434b4d8b0b784825f119744`  
		Last Modified: Thu, 20 Jun 2024 20:56:55 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ce9d83f97f733ed27f9c9b3a01f5d62b680add1852cf5737d0078d15322cf`  
		Last Modified: Thu, 20 Jun 2024 20:56:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:5cb763be9da459e5ed7e0505b0073241c8e3a0ae37e0d3ea2ad0050c3980a991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 KB (233579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7795127d92bef4efc1d41bc689a1330bba955f9dc387cc021f6ccca60f4af512`

```dockerfile
```

-	Layers:
	-	`sha256:b1fe8b7ea701a68a0a6b773a59e2faa0804ed3032832fdcca03bb3eaa8ffda23`  
		Last Modified: Thu, 20 Jun 2024 20:56:55 GMT  
		Size: 216.9 KB (216882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eece67b5983a18ad16e61a01996f46de33cdb81d0062ae19b6e8f6de48ee473e`  
		Last Modified: Thu, 20 Jun 2024 20:56:55 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:c78da5527919125de76f4dce0020511b5959b54ac698c30c9462706981d9f254
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
$ docker pull chronograf@sha256:60ac65e44d3465d9a21254be4fb46cc606089f90e70b631587994e8c1ff0f32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71682443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227cb01b7bd3a5808b5b59aeac6849442b89923501b58aa21d185fb5950f8e8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ea3f488d2b3e3be13ec1474956f5dfac75e58348e02ec8e0d2d26e3ddc9517`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 5.2 MB (5224193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fadd7c3a1d55e8a5c4e8c950a7e256fd94363e7a6cb8951b96c89511b47118`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 35.0 MB (35011587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42720a1eb2786df8b8126407b28d597e10c985650a232048402ea700320245c2`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30b67d5c4bbc7cb1e9d9eb55ab6cba73f97e66fe0ed354db62f2c2cdecddc0`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0740228b25ace4c4f7210d8944291c08bac7f7738c75e4a8fe46d367e0f090a7`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:8a790635ed9d64d82857d3e45b3c0535dcd303811d6b3f2cd6348c3254555ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2934857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53dbe4b74dfd5e78a779e03d0b7ab4a3bc44bd3033d278f968e150df97cd65d`

```dockerfile
```

-	Layers:
	-	`sha256:559b226415d9a1316d108aff1073270d879bc8cf1ed66d6d3974f1ddcde9b047`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 2.9 MB (2919241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e02314bf0463e57ef21264398ccf47d418f5d19a0fe1184e3d6966ee27293c7a`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 15.6 KB (15616 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:434e8e18a112a2c6b56740fbd0c1a26cdcbdb713b966379b43b2f38c2be694bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64408538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7416ef1f7941343285afe1ee26ed594bed8863de714e6b47382004715ca7d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
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
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa53d5c68a74e2caa2b0922c6ce751b2f1fe854e1362fef70dfcf8bfbb64faa`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 4.5 MB (4490082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180115af1b5da40472752b80c72ac7b9275589f2d0b71570ba7d04392075ea4a`  
		Last Modified: Tue, 02 Jul 2024 06:35:54 GMT  
		Size: 33.3 MB (33311369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70810fa78d97a8f2d09d4d20e45887d1e81866234bae7b5d688d998872e1847`  
		Last Modified: Tue, 02 Jul 2024 06:35:53 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81f4c6d286593b7c4bd5fc50e3b695b7b3f9d890780fb7f2255f1e49bbd37d`  
		Last Modified: Tue, 02 Jul 2024 06:35:53 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf2cee1ae8e9a1323c64af11dcb7faf4194443821d1a709a699eed78ad827a`  
		Last Modified: Tue, 02 Jul 2024 06:35:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:244957977610291976606612319f7465d586832726bfb73d7a4956e0acc5baa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b106b06f6fddc3c9e7349cd2bb9578e9d34a60f6c6868928a7054abb33ea2e`

```dockerfile
```

-	Layers:
	-	`sha256:9857f3965c874fe0339f71b75769a6668d464e6ea642957726e3549df5556d57`  
		Last Modified: Tue, 02 Jul 2024 06:35:53 GMT  
		Size: 2.9 MB (2921511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea1ba5b8ea2574135b387fdd0d338c2fb2d8ad09e673148e005ddc9901165da`  
		Last Modified: Tue, 02 Jul 2024 06:35:52 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6e8c68703b2c32c0caa49fca9a178c1b1570fc83f02d4983afda43ef05187cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68296970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2383c1504df2d6569fca6055e53ec08b06e23f454c5b375c7ebed93ac65d7c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198db4c78d05a7fae6481f1f23e9abd0f4bd589e25e5b4afa53b8cb416bbfc7`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 5.0 MB (5004108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ad92281f32fe70c0311ce7ed3f7acd1741c8032fde27cbc16f94a5c38d565f`  
		Last Modified: Thu, 13 Jun 2024 10:55:38 GMT  
		Size: 33.2 MB (33181496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da50fde1cce334f6a1ad1711bb3d87397a8080057f40cf3f96350391baf652ca`  
		Last Modified: Thu, 13 Jun 2024 10:55:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3509692559eedcda3f2b71b87c4c102ab3f01cb0cace7bf32e1a47a4eef43a2`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac4d965d75fd56f4d880446b398e9a6070d38f4b50bbd1e7407d4967eeb618`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:f51c3c268b6054fba5a9c1d7b5f3b873174ec5faae2d43bc933de2f8139a39ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5af6a49938dd2a8df3b0af59b7ce70e798dd386349119c683868194949f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f2d7394ca425fefa0fc2285f002417e4488e41a44e6be35d3d56e63eede1491d`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 2.9 MB (2919450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417534c734d87b40b3a2af7e2151653dad429ec2863595e87e5230bdb8e55eea`  
		Last Modified: Thu, 13 Jun 2024 10:55:36 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:d9a2179d92fb88cd0af7308bf7a5cbce583a5172dc6b2adce5ae1afff2acee51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b0ce1dfe716aee9383ea0f939bc50557fccace39bbdc27e1f0a84497a8370c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23613003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8c628503a2cd601120b0ba224dab36c9e92153b3a4287da55478946b7d09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2feade0b56ab73e43d466d80ae5f8520e6980f8be9faa76cfeb2469940ee24`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dfc7feaeda5eebc8e8eff57fbc7a172cc9456841cfbfcbe16305df9fc80587`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 292.4 KB (292418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01e086d0e1216edc62a7964c649375ed8c53fcfcbb8ce03ae236f0a90aeea9d`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 19.7 MB (19672086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1270fe3d86e2549b6730a41e5f045736ca9dbe0acb1aebd66e19fca9f8496325`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1d0a5f8c48334aaf813231c16b2bb688cf8f397bae19f90f3ed5cb435567f1`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403e3e9d757b928cccef98d9366c1af31db28328f420bbbd1ffacd18b7484f1`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:19abcd63ce90b3f5fcd48d17f443bc38208e4e12f0e1b3633f67342326257488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 KB (237869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d61b50c7fa691eb226bc4795a8a5deeb01d1e3f6fd472becee1ef4b8db3cec4`

```dockerfile
```

-	Layers:
	-	`sha256:593444f07193cedb98c95112a22a0f6cde9d869302e31c8ab9bb87942a0e2b49`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 221.2 KB (221176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703f8ac08838d1847c70ca780cc70619aa43656a9e551cd81e8eb0648a55113a`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:c78da5527919125de76f4dce0020511b5959b54ac698c30c9462706981d9f254
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
$ docker pull chronograf@sha256:60ac65e44d3465d9a21254be4fb46cc606089f90e70b631587994e8c1ff0f32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71682443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227cb01b7bd3a5808b5b59aeac6849442b89923501b58aa21d185fb5950f8e8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ea3f488d2b3e3be13ec1474956f5dfac75e58348e02ec8e0d2d26e3ddc9517`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 5.2 MB (5224193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fadd7c3a1d55e8a5c4e8c950a7e256fd94363e7a6cb8951b96c89511b47118`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 35.0 MB (35011587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42720a1eb2786df8b8126407b28d597e10c985650a232048402ea700320245c2`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30b67d5c4bbc7cb1e9d9eb55ab6cba73f97e66fe0ed354db62f2c2cdecddc0`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0740228b25ace4c4f7210d8944291c08bac7f7738c75e4a8fe46d367e0f090a7`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:8a790635ed9d64d82857d3e45b3c0535dcd303811d6b3f2cd6348c3254555ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2934857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53dbe4b74dfd5e78a779e03d0b7ab4a3bc44bd3033d278f968e150df97cd65d`

```dockerfile
```

-	Layers:
	-	`sha256:559b226415d9a1316d108aff1073270d879bc8cf1ed66d6d3974f1ddcde9b047`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 2.9 MB (2919241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e02314bf0463e57ef21264398ccf47d418f5d19a0fe1184e3d6966ee27293c7a`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 15.6 KB (15616 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:434e8e18a112a2c6b56740fbd0c1a26cdcbdb713b966379b43b2f38c2be694bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64408538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7416ef1f7941343285afe1ee26ed594bed8863de714e6b47382004715ca7d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
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
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa53d5c68a74e2caa2b0922c6ce751b2f1fe854e1362fef70dfcf8bfbb64faa`  
		Last Modified: Tue, 02 Jul 2024 06:34:39 GMT  
		Size: 4.5 MB (4490082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180115af1b5da40472752b80c72ac7b9275589f2d0b71570ba7d04392075ea4a`  
		Last Modified: Tue, 02 Jul 2024 06:35:54 GMT  
		Size: 33.3 MB (33311369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70810fa78d97a8f2d09d4d20e45887d1e81866234bae7b5d688d998872e1847`  
		Last Modified: Tue, 02 Jul 2024 06:35:53 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81f4c6d286593b7c4bd5fc50e3b695b7b3f9d890780fb7f2255f1e49bbd37d`  
		Last Modified: Tue, 02 Jul 2024 06:35:53 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf2cee1ae8e9a1323c64af11dcb7faf4194443821d1a709a699eed78ad827a`  
		Last Modified: Tue, 02 Jul 2024 06:35:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:244957977610291976606612319f7465d586832726bfb73d7a4956e0acc5baa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b106b06f6fddc3c9e7349cd2bb9578e9d34a60f6c6868928a7054abb33ea2e`

```dockerfile
```

-	Layers:
	-	`sha256:9857f3965c874fe0339f71b75769a6668d464e6ea642957726e3549df5556d57`  
		Last Modified: Tue, 02 Jul 2024 06:35:53 GMT  
		Size: 2.9 MB (2921511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea1ba5b8ea2574135b387fdd0d338c2fb2d8ad09e673148e005ddc9901165da`  
		Last Modified: Tue, 02 Jul 2024 06:35:52 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:6e8c68703b2c32c0caa49fca9a178c1b1570fc83f02d4983afda43ef05187cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68296970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2383c1504df2d6569fca6055e53ec08b06e23f454c5b375c7ebed93ac65d7c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e198db4c78d05a7fae6481f1f23e9abd0f4bd589e25e5b4afa53b8cb416bbfc7`  
		Last Modified: Thu, 13 Jun 2024 10:39:04 GMT  
		Size: 5.0 MB (5004108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ad92281f32fe70c0311ce7ed3f7acd1741c8032fde27cbc16f94a5c38d565f`  
		Last Modified: Thu, 13 Jun 2024 10:55:38 GMT  
		Size: 33.2 MB (33181496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da50fde1cce334f6a1ad1711bb3d87397a8080057f40cf3f96350391baf652ca`  
		Last Modified: Thu, 13 Jun 2024 10:55:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3509692559eedcda3f2b71b87c4c102ab3f01cb0cace7bf32e1a47a4eef43a2`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac4d965d75fd56f4d880446b398e9a6070d38f4b50bbd1e7407d4967eeb618`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:f51c3c268b6054fba5a9c1d7b5f3b873174ec5faae2d43bc933de2f8139a39ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2935351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5af6a49938dd2a8df3b0af59b7ce70e798dd386349119c683868194949f96c`

```dockerfile
```

-	Layers:
	-	`sha256:f2d7394ca425fefa0fc2285f002417e4488e41a44e6be35d3d56e63eede1491d`  
		Last Modified: Thu, 13 Jun 2024 10:55:37 GMT  
		Size: 2.9 MB (2919450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417534c734d87b40b3a2af7e2151653dad429ec2863595e87e5230bdb8e55eea`  
		Last Modified: Thu, 13 Jun 2024 10:55:36 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:d9a2179d92fb88cd0af7308bf7a5cbce583a5172dc6b2adce5ae1afff2acee51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:b0ce1dfe716aee9383ea0f939bc50557fccace39bbdc27e1f0a84497a8370c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23613003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8c628503a2cd601120b0ba224dab36c9e92153b3a4287da55478946b7d09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2feade0b56ab73e43d466d80ae5f8520e6980f8be9faa76cfeb2469940ee24`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dfc7feaeda5eebc8e8eff57fbc7a172cc9456841cfbfcbe16305df9fc80587`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 292.4 KB (292418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01e086d0e1216edc62a7964c649375ed8c53fcfcbb8ce03ae236f0a90aeea9d`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 19.7 MB (19672086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1270fe3d86e2549b6730a41e5f045736ca9dbe0acb1aebd66e19fca9f8496325`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 12.2 KB (12236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1d0a5f8c48334aaf813231c16b2bb688cf8f397bae19f90f3ed5cb435567f1`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403e3e9d757b928cccef98d9366c1af31db28328f420bbbd1ffacd18b7484f1`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:19abcd63ce90b3f5fcd48d17f443bc38208e4e12f0e1b3633f67342326257488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 KB (237869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d61b50c7fa691eb226bc4795a8a5deeb01d1e3f6fd472becee1ef4b8db3cec4`

```dockerfile
```

-	Layers:
	-	`sha256:593444f07193cedb98c95112a22a0f6cde9d869302e31c8ab9bb87942a0e2b49`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 221.2 KB (221176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703f8ac08838d1847c70ca780cc70619aa43656a9e551cd81e8eb0648a55113a`  
		Last Modified: Thu, 20 Jun 2024 20:54:44 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:984d3beb716dbfd933b376d3a11c8cde64589d7e5808a0539aebc245018da6de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:07c647f252815f58012c9080fb27389864deeaf76c7c87966cf06ff058212c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31809610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abdedc468f1ceb9e469bbeeaf13b3df35ad006916a805f4e88b28973f090ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca434a5221442ebfb3dbc3b9c9345f539777fcce196f9953179c35ed4c20b8`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3846ce7e00dea64b371302742d345d5d8bb344f7a56b72962a3afba74b2ee0d2`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 294.3 KB (294344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d0514f13c9e2d24d9d2c294215739da77b2facca8d45dc71ce567f3d58710b`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 27.9 MB (27866719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb2114a0ab5cba7eb6b946de96d6b5683da1695cdcdc11a4c871da4f27a376b`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a0dc96f976b28a9956775a14d182bc7f8632f322fbdd55ec3f90f89140148b`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db878d5004db02d508ab4fe22d6f8b1c26cebf9fb27103a529508b6c866e40`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0ca449aa846286bc7d47ab5fbd21720b9b09aba4cd9c9f446952fa94951a97c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18078ceb4ff8c5c6e5c418434c411b41e90728bc1f1692585634ee0a4370eb0d`

```dockerfile
```

-	Layers:
	-	`sha256:7ebbda34b238dac5156e27fdc39d2906e77398c4d00e55e963fd947eda6b3789`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 226.9 KB (226904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d242d1ae488c04ce12d615444f295341e10602467dfdeae021b8bb1becf01a9c`  
		Last Modified: Thu, 20 Jun 2024 20:54:45 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:029cbaf9f6234b7da9520f8769c6e5ca4bc9ca9bd17f292e765bbadccb5b36a6
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
$ docker pull chronograf@sha256:b9541a7c646b482265adb3c9d627378b2d83d4ef5859ed30d012d30022a69e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84239001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490904b34dc02839057ae9bbd784311b5af723278d9df8c708f1c507b715fc98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce26bc7a4c162f172c6ba2779c8e458ff17a75156594043161938df2ae44e890`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 7.9 MB (7871381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6f4fedc4074b8b78cc4fc2c448a1bb1a48b0186ec68a8e1023d4b3ee5d572`  
		Last Modified: Tue, 02 Jul 2024 03:02:27 GMT  
		Size: 47.2 MB (47216887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42720a1eb2786df8b8126407b28d597e10c985650a232048402ea700320245c2`  
		Last Modified: Tue, 02 Jul 2024 03:02:24 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30b67d5c4bbc7cb1e9d9eb55ab6cba73f97e66fe0ed354db62f2c2cdecddc0`  
		Last Modified: Tue, 02 Jul 2024 03:02:25 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2b163e95e68de39248cbea368139f04bd7d18059bf9d36f1ea5f6d216e6b`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:578d5793597937e1669c23efa44690d5183c3bd0a47d3b53414f6c059d640aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2671477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4dec00d335d5450ec69ddcdecc9993433b0175795b00ebc663eebae7103dd6`

```dockerfile
```

-	Layers:
	-	`sha256:467df9c611d592aa8b473bfd555940d0da4ed16b20be29e7ea9949e185113a24`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 2.7 MB (2655543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5989dafb2edf356430b4e7b198331be7faca9362e3b0ca011f097bf421c0fee`  
		Last Modified: Tue, 02 Jul 2024 03:02:26 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a0435ce083bb756da6b06b35d004a6ac76fc037d1ee77edb26ad1d3abe4f331e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75514451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709fc7a87206030dfffc1b51b1928616579e1fe843dc0b1cb95bef6a2b661f99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9c896caa2726afa387b9dbac529ecbb121f6e6a25d5e366c255900d9244b4d`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 6.5 MB (6495956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e0d3e9f0ae48de66aaa8921b76c9299e70974fb0ec1df0118bd4751a2655f8`  
		Last Modified: Tue, 02 Jul 2024 06:36:49 GMT  
		Size: 44.3 MB (44275865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8282e6619a76bfea913cda577cae5b5473eb0719794b3e3a62e4fdb445144a2`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd8f2f723f0513c18e767b3af2973c74e5d4c51950fc8942ae91d5bdefd884`  
		Last Modified: Tue, 02 Jul 2024 06:36:49 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877c004bdbf6a2829789712a2844bab48756799d1c46e319d425d1f6486de11`  
		Last Modified: Tue, 02 Jul 2024 06:36:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:779eacc0c1883eba90afff28b60dcdd2f1617791ce8647ab6bee762712b5b19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2673848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85635c702deafbb01bff1c75af329dce91f9a2d98f3b89c4d81c1710116844e8`

```dockerfile
```

-	Layers:
	-	`sha256:a02c71c637b3db2ebca897158751cd9dbf2b7f6a1df5e980cb035a7faa1005f9`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 2.7 MB (2657839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed70aab04800dec2c9605fc11ba5d3bd4d8b2b745a9aacbd6ad74a6b2aa7474c`  
		Last Modified: Tue, 02 Jul 2024 06:36:48 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2509b79f21f8d2f01cc6fb1787c60e192cedbaa1c3a0df512f250cef530831b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81628369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0abb98411db0e43a2472ca9a04e405f3988fda0221fc73309073c33d3f1e22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c44ee98f21bfee7c5d1f4a14f776fde4841c39b3768dd1ef9237f050a1c7e`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 7.5 MB (7453190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1353d59f878028d1e53f5b9ba7ff5ffc15eba37b01f82eb05dd966d56edd38d`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 45.0 MB (44971054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acf276b9e8fbbd0dcc962675f697db83c1ae8c2bddaca1cb5c11c46971d74c7`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6dd95139e23cb8a4d10dad60fa476b92f5a9145a7dd7065456fe757ca3a31`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91708736b0c8e603f3424312a2afcaa5a538aa78627f508d8c4987f3ed15b722`  
		Last Modified: Thu, 13 Jun 2024 11:07:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:cd716da942a514ab19d44c83fa585a1630ed5119a82b7e3f88ebe30d0925a055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1778fda725b4d6774f106bdc18c6d9b53fc21bdb277af9413e686b3ad5f1441`

```dockerfile
```

-	Layers:
	-	`sha256:f3e3f8f7212f21dc6670ffb3733e2c1980e6bc43ea569b9fd42cf0084277c5c9`  
		Last Modified: Thu, 13 Jun 2024 11:07:26 GMT  
		Size: 2.7 MB (2655786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd3e10071bb448a595fd2dac1ecd5a65e785f3fad6449fd2bc71fbcbbe02612`  
		Last Modified: Thu, 13 Jun 2024 11:07:25 GMT  
		Size: 16.2 KB (16230 bytes)  
		MIME: application/vnd.in-toto+json
