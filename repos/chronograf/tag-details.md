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
$ docker pull chronograf@sha256:577141d452b5a3cccbd1db19145202a297d49c663bb79bbf779a8f34c6408f44
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
$ docker pull chronograf@sha256:bfca8025f4d68b495da72e098376d1fe63b9ae77c9a61aafda046b2ff18c83c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84242775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e22bd1094cc8989f1be4b77b98d19d05d4c8b87eb06a287102835d8d17f5dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931ce04a30de7c6159357982f3d2483c8c2e16e134f40bbe80649bee7c12da9b`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 7.9 MB (7874758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf564a41eef26bac0ce210e52a60894f64d25f1e817cc4a642e2f42a74365e70`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 47.2 MB (47217280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658b8c5e294f51d814ca552029bd6010582dac5ea08dbe1d40e0bec9f1139a1`  
		Last Modified: Fri, 27 Sep 2024 06:00:47 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73977342bb8e5122e366042f7d946ff6e9c68632cc5a9379401c22c50db6da8e`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ba1a31ceeaae1e5b7461840d0c8154abc898a3acb106b2453e99ab502b73ef`  
		Last Modified: Fri, 27 Sep 2024 06:00:49 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:10cad40c1cff2b4dd3bcf21fd31b5755c86469928cd837976ce396b39338595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d968b3d22adb6a6263cd5616772258f6d5b40f6fae2dd9db77e9c34091d1b5`

```dockerfile
```

-	Layers:
	-	`sha256:26882e00fc721d89c0a6ab2ae2b6ad7b447fb645c183a2a67a1567a038fb36d9`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 2.7 MB (2690960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b147ce9a37e84ca85751772d5af43e4bbca08b527b0ec053c8b73856045b4746`  
		Last Modified: Fri, 27 Sep 2024 06:00:47 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f4e397fb399f64fcf07bc43bab529323cdb22432f4b823604d4c55060acc973c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75516183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a78871ba44f021ee17c3b85942764da865fff0d9b4664f97a8adb15c31af624`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93075f5189215242875cbd3d5e513405ee4b4d1b4e8297d1c0d2e4465465568f`  
		Last Modified: Fri, 27 Sep 2024 10:21:03 GMT  
		Size: 6.5 MB (6497563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b57e864f3a4f39835c3705faaf75356ce8308b7033d8a18f5245e4cc695152`  
		Last Modified: Fri, 27 Sep 2024 10:21:04 GMT  
		Size: 44.3 MB (44276006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa51aa34c540038eb1c3c1f16872ece2f1da8f732de20f7cd25317d28a2af4`  
		Last Modified: Fri, 27 Sep 2024 10:21:02 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba15c11dcf19bd71b5605fb06ceec46dc294d94cf41b8c71adcd15c3273649ba`  
		Last Modified: Fri, 27 Sep 2024 10:21:03 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9106328ba6ab3f511e9697a68f801fbd8cf7e837fad34c78fe682682ecc03e`  
		Last Modified: Fri, 27 Sep 2024 10:21:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:56b9a7f2c2e93cb638a90d8f7a10b78f01482e174ad0d46d778dcdcf7ac7d956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1b21096c93a71510558b4645364e5cfcaab5c9516d9893db2d2318b5373efb`

```dockerfile
```

-	Layers:
	-	`sha256:14e202c2801d21db907ade88851037fdaa7e6c044e4d8b627466c3c848fd7d85`  
		Last Modified: Fri, 27 Sep 2024 10:21:03 GMT  
		Size: 2.7 MB (2693256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bf294098e564cb51d47ce92f9687e5bb12c4627afcc4418083b6250c982704`  
		Last Modified: Fri, 27 Sep 2024 10:21:02 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:23cbe7b62f6dd8d267f7b5fdac8d27523ab31c0fcaa72f75b201b6c922a865af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81802521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4d47528283cee27d646e2bb2c4b4e80911fd53583bcd1a464c4695d7f016cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6bbfdabfa81c2097fa252bb22668759ae42a543d8438e950c1b358320e23ab`  
		Last Modified: Fri, 27 Sep 2024 10:12:53 GMT  
		Size: 7.7 MB (7651311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c32089a726eece93219d436dcc8f441e6dfbfa42e37aa693973505516817066`  
		Last Modified: Fri, 27 Sep 2024 10:12:54 GMT  
		Size: 45.0 MB (44970387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3840bf77bfc5b8546225f8aac0852984537b572a5ca7b5f00beecc05e16c974`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219ac5eb808868491929c75e1e79af7b42478c21e319330ff2f5141f8e832bf5`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef5af92adc6445bde61b8c40e72f420c99bba684a6825e3fff3bec5fee1cede`  
		Last Modified: Fri, 27 Sep 2024 10:12:53 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:61b9b5f3b618e8d621b54d8dcd486f17985c03fbb7f92820e1dc7ecc76de5325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3f533ec676d7191bff30fb070d29396bdb3320a2ea4bae035b413417c748fc`

```dockerfile
```

-	Layers:
	-	`sha256:d7a87eb439c233b417a4aab085b83c9f11594153953278e14254670ebaeefb1e`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 2.7 MB (2691232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0978d3b28c381c6ce79f8c21fdfd756db72e9f46602c40e3419b00fb2df771`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 16.2 KB (16231 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:5c0ef984976bfefd20fa4c75f0c6a875561bbe792fbc3a8dd1562d9f58bfe74d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9db740a90a3f57dec9ee0694c4c0ca7108726332a5fcaabba6f511ef2d950a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31807854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721c7b0fb14defda16bb4c97e7b7973eba1357cb1f911ed888bf8de5ca1f2be4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08d447a64db49fbab2349074af3b28b29fc9f9e21d220e5ef3c257757c4dc74`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c1bf89f79d5659365e90141c4b9d64ac53a7d3fa453daec6c91390c55db6b`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 292.6 KB (292597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2fdc8712d053d3be5a3eac36d2ab85885a94a8420b9e1c618b83faba44cb0`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 27.9 MB (27866745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582c813a3de53aaf6186a47b93b9b94f71b222359ee33a8a6c852a2958d94a4`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b650264875e0bb719fef5c24879775972e4ffa43ffceaa93b671be1bf3888`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020946a0bc65717d96d8dcea5b6ff1b5cfe797c14fea294199a0d20f75399744`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:805e972c1bb52dfc739c6298925601f6f43a3d3fc6ad154c942f138f34608910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 KB (257225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7796174809f7169d510b6c15dc3f9706d25fa63b88bae8d42cd72c6b5132604`

```dockerfile
```

-	Layers:
	-	`sha256:98e0e20b09ed16648a357232ac7fdf95371f498fda9265df1d848b41f11a678e`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 239.6 KB (239585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79b51922071e3d180fdebf5a7cbb5b9d23c8ad6154951adff660268d34e7618`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:577141d452b5a3cccbd1db19145202a297d49c663bb79bbf779a8f34c6408f44
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
$ docker pull chronograf@sha256:bfca8025f4d68b495da72e098376d1fe63b9ae77c9a61aafda046b2ff18c83c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84242775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e22bd1094cc8989f1be4b77b98d19d05d4c8b87eb06a287102835d8d17f5dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931ce04a30de7c6159357982f3d2483c8c2e16e134f40bbe80649bee7c12da9b`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 7.9 MB (7874758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf564a41eef26bac0ce210e52a60894f64d25f1e817cc4a642e2f42a74365e70`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 47.2 MB (47217280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658b8c5e294f51d814ca552029bd6010582dac5ea08dbe1d40e0bec9f1139a1`  
		Last Modified: Fri, 27 Sep 2024 06:00:47 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73977342bb8e5122e366042f7d946ff6e9c68632cc5a9379401c22c50db6da8e`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ba1a31ceeaae1e5b7461840d0c8154abc898a3acb106b2453e99ab502b73ef`  
		Last Modified: Fri, 27 Sep 2024 06:00:49 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:10cad40c1cff2b4dd3bcf21fd31b5755c86469928cd837976ce396b39338595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d968b3d22adb6a6263cd5616772258f6d5b40f6fae2dd9db77e9c34091d1b5`

```dockerfile
```

-	Layers:
	-	`sha256:26882e00fc721d89c0a6ab2ae2b6ad7b447fb645c183a2a67a1567a038fb36d9`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 2.7 MB (2690960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b147ce9a37e84ca85751772d5af43e4bbca08b527b0ec053c8b73856045b4746`  
		Last Modified: Fri, 27 Sep 2024 06:00:47 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f4e397fb399f64fcf07bc43bab529323cdb22432f4b823604d4c55060acc973c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75516183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a78871ba44f021ee17c3b85942764da865fff0d9b4664f97a8adb15c31af624`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93075f5189215242875cbd3d5e513405ee4b4d1b4e8297d1c0d2e4465465568f`  
		Last Modified: Fri, 27 Sep 2024 10:21:03 GMT  
		Size: 6.5 MB (6497563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b57e864f3a4f39835c3705faaf75356ce8308b7033d8a18f5245e4cc695152`  
		Last Modified: Fri, 27 Sep 2024 10:21:04 GMT  
		Size: 44.3 MB (44276006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa51aa34c540038eb1c3c1f16872ece2f1da8f732de20f7cd25317d28a2af4`  
		Last Modified: Fri, 27 Sep 2024 10:21:02 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba15c11dcf19bd71b5605fb06ceec46dc294d94cf41b8c71adcd15c3273649ba`  
		Last Modified: Fri, 27 Sep 2024 10:21:03 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9106328ba6ab3f511e9697a68f801fbd8cf7e837fad34c78fe682682ecc03e`  
		Last Modified: Fri, 27 Sep 2024 10:21:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:56b9a7f2c2e93cb638a90d8f7a10b78f01482e174ad0d46d778dcdcf7ac7d956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1b21096c93a71510558b4645364e5cfcaab5c9516d9893db2d2318b5373efb`

```dockerfile
```

-	Layers:
	-	`sha256:14e202c2801d21db907ade88851037fdaa7e6c044e4d8b627466c3c848fd7d85`  
		Last Modified: Fri, 27 Sep 2024 10:21:03 GMT  
		Size: 2.7 MB (2693256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bf294098e564cb51d47ce92f9687e5bb12c4627afcc4418083b6250c982704`  
		Last Modified: Fri, 27 Sep 2024 10:21:02 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:23cbe7b62f6dd8d267f7b5fdac8d27523ab31c0fcaa72f75b201b6c922a865af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81802521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4d47528283cee27d646e2bb2c4b4e80911fd53583bcd1a464c4695d7f016cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6bbfdabfa81c2097fa252bb22668759ae42a543d8438e950c1b358320e23ab`  
		Last Modified: Fri, 27 Sep 2024 10:12:53 GMT  
		Size: 7.7 MB (7651311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c32089a726eece93219d436dcc8f441e6dfbfa42e37aa693973505516817066`  
		Last Modified: Fri, 27 Sep 2024 10:12:54 GMT  
		Size: 45.0 MB (44970387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3840bf77bfc5b8546225f8aac0852984537b572a5ca7b5f00beecc05e16c974`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219ac5eb808868491929c75e1e79af7b42478c21e319330ff2f5141f8e832bf5`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef5af92adc6445bde61b8c40e72f420c99bba684a6825e3fff3bec5fee1cede`  
		Last Modified: Fri, 27 Sep 2024 10:12:53 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:61b9b5f3b618e8d621b54d8dcd486f17985c03fbb7f92820e1dc7ecc76de5325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3f533ec676d7191bff30fb070d29396bdb3320a2ea4bae035b413417c748fc`

```dockerfile
```

-	Layers:
	-	`sha256:d7a87eb439c233b417a4aab085b83c9f11594153953278e14254670ebaeefb1e`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 2.7 MB (2691232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0978d3b28c381c6ce79f8c21fdfd756db72e9f46602c40e3419b00fb2df771`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 16.2 KB (16231 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:5c0ef984976bfefd20fa4c75f0c6a875561bbe792fbc3a8dd1562d9f58bfe74d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9db740a90a3f57dec9ee0694c4c0ca7108726332a5fcaabba6f511ef2d950a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31807854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721c7b0fb14defda16bb4c97e7b7973eba1357cb1f911ed888bf8de5ca1f2be4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08d447a64db49fbab2349074af3b28b29fc9f9e21d220e5ef3c257757c4dc74`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c1bf89f79d5659365e90141c4b9d64ac53a7d3fa453daec6c91390c55db6b`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 292.6 KB (292597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2fdc8712d053d3be5a3eac36d2ab85885a94a8420b9e1c618b83faba44cb0`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 27.9 MB (27866745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582c813a3de53aaf6186a47b93b9b94f71b222359ee33a8a6c852a2958d94a4`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b650264875e0bb719fef5c24879775972e4ffa43ffceaa93b671be1bf3888`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020946a0bc65717d96d8dcea5b6ff1b5cfe797c14fea294199a0d20f75399744`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:805e972c1bb52dfc739c6298925601f6f43a3d3fc6ad154c942f138f34608910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 KB (257225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7796174809f7169d510b6c15dc3f9706d25fa63b88bae8d42cd72c6b5132604`

```dockerfile
```

-	Layers:
	-	`sha256:98e0e20b09ed16648a357232ac7fdf95371f498fda9265df1d848b41f11a678e`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 239.6 KB (239585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79b51922071e3d180fdebf5a7cbb5b9d23c8ad6154951adff660268d34e7618`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:87e3860b4c7f8ae3889b773e60b03066accc24a84d1f33df3a9e84b88667e1a2
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
$ docker pull chronograf@sha256:a16688f6dab80c3e69e3f98a1773ab9e9047af104f56e6a36f6f57e0d3e4a112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70400590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6269eaf60a39bbb03b3ab1aa08d04babdfc90abd696909d9b08fa3b20b63ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666aed9bac86ceb0bc41e0a9d171f1160e447062928d33ba7f981b0868e81167`  
		Last Modified: Fri, 27 Sep 2024 06:00:52 GMT  
		Size: 4.2 MB (4209310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da746ea98382f062ac1d8ab5ad6ed7a23ef8e634ff1a7d6302f540029cc63fda`  
		Last Modified: Fri, 27 Sep 2024 06:00:54 GMT  
		Size: 34.7 MB (34738292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bec0790be1012f2c399d0734154fd0651a589dadb94eae3f992c6166247bd7`  
		Last Modified: Fri, 27 Sep 2024 06:00:51 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb80f58342ee1b10a7fed03bce92e55eb24ff69ba8439b143caedc002531b381`  
		Last Modified: Fri, 27 Sep 2024 06:00:51 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26571979d1a5cb4e4219c007b549fa9fa8aed4d67ff9ec7aa1b2227f5f6cfbb4`  
		Last Modified: Fri, 27 Sep 2024 06:00:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:62f87b112d8b8c2b58f4239fbe1ef0630ef847204c496e7a5daf97fe22264b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883833a3bb6ec34616e595ee2f2dd25ad14c2660c9d49d6f0009c5b449cb4f6`

```dockerfile
```

-	Layers:
	-	`sha256:fb391cef629ac97bc6f529d4de67682db92b6d431abb3a5c0d681578aee3198a`  
		Last Modified: Fri, 27 Sep 2024 06:00:52 GMT  
		Size: 2.9 MB (2893555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6187767858e82d9128b9370c9fc31af89c1c1c0f042a9d2721f96ff8642cb2a`  
		Last Modified: Fri, 27 Sep 2024 06:00:51 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2fa1cdb073e6c2b5ac541eb2c0d3d981e29bc5cb9d2fb640d715bd8779aef09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde5536cd4bb8b42ba9e7711e010085741afdaa1d6f17175ffbc69a1226b0e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb2c98667dee735f1184796fa2cee79af730bd211287192474ebecde128ed4`  
		Last Modified: Fri, 27 Sep 2024 10:12:35 GMT  
		Size: 3.5 MB (3511606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7026d41bcad318f20a2cf0a6c7679b52f1c7176c9646801dbfca9c07669dbf2`  
		Last Modified: Fri, 27 Sep 2024 10:12:36 GMT  
		Size: 33.1 MB (33097463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d45a573dc26738f0af754ac64243410e4adeebb9dc6f7f002370c29ea1e1aa`  
		Last Modified: Fri, 27 Sep 2024 10:12:34 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc754763ecf15ebb623c62bc2a084c789581cefb7d96eea02804274abf00db38`  
		Last Modified: Fri, 27 Sep 2024 10:12:35 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fdb5ad12a4c871e29f9d49a8c0010defdaf002b21830c10e839cc4aa3057b9`  
		Last Modified: Fri, 27 Sep 2024 10:12:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:e171ebb3860e6ee6899651fec3eaaa81176dcc73c4c525a5064ca20e0cf0559c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2911475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0038ed29e64b73bfaf60424b017688bca0f7db78e142805ab2e628c0c314a529`

```dockerfile
```

-	Layers:
	-	`sha256:4628f597e16dd52368fd08014bc7f535407230f5106a14ca9ea0f14d1988b19a`  
		Last Modified: Fri, 27 Sep 2024 10:12:35 GMT  
		Size: 2.9 MB (2895825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc4447c0e04489c7b97731e1db286ef8bd0a2a0eaecbe8f5938ccdade78d0589`  
		Last Modified: Fri, 27 Sep 2024 10:12:34 GMT  
		Size: 15.7 KB (15650 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:044a5aa39f98e9eb8ecff5bb77946a2cf093ba3c4ac81a8cbab42e97c474a08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67547922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd5e28df840f0d2adfb4ccb8fc9aa4978fc7a9b4ff97f79843eda7e1515f154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bf811df6e4ba63716a64a12e52b203a40468f362a32ac642d07681fbe558a4`  
		Last Modified: Fri, 27 Sep 2024 10:11:03 GMT  
		Size: 4.2 MB (4210528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e80a2da2fac7d87da01503971ab846718f08f95f15dd648924294f2ebb4ad1a`  
		Last Modified: Fri, 27 Sep 2024 10:11:04 GMT  
		Size: 33.2 MB (33237852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c82b1eabf3ea8883f10a126efe11d73fd93b97e8ac20cfac18898f2225e9f5`  
		Last Modified: Fri, 27 Sep 2024 10:11:05 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1732cfddd11c8fd5a433875b4be169385a62af0e6e27c40986fd8f8cbacd5f`  
		Last Modified: Fri, 27 Sep 2024 10:11:05 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8ed549128e39c863dde59a2ba252c9de623a4d4e75605415c36edcf83e3d31`  
		Last Modified: Fri, 27 Sep 2024 10:11:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:05da5b711eb735cb3d0fb947c62127e14d64b11ad4322bd04fba2dce406b014e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0668c85f96255553a733201536aadd950ad4509d20ae8daca817681a3cb107`

```dockerfile
```

-	Layers:
	-	`sha256:ee6801b6f33e0c92f8f7830eb556c273c1e7f7b18a14c9cec0fe0e4d1ada9f6c`  
		Last Modified: Fri, 27 Sep 2024 10:11:03 GMT  
		Size: 2.9 MB (2893803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22e2ff99363b3d97d640a7562bebfc56cea1eb5d4d0a14cd34bcfc1e8f90d99`  
		Last Modified: Fri, 27 Sep 2024 10:11:03 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:ae9cdafc242e5e8ff9c96f3c65f39bb1538f574e7535c67c8e52cdaee219960c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3de004b9b3957e329028c27dcaff35a81dadbe9556d127936b2043b86a6ccad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23496029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2243834b7dedb55ce7db37bb4e12aefe047628ff2f64cceb06de3ea38d017317`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a7812599bc616e92d0320eee1b26625969a25c2baf338377a45df6a273462a`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbda816b9a9bb7d03cfdc8c20a70fff0ed2202c45165aa32b72aa1bcbb3f58e`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 290.9 KB (290878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1337904852ed7215c8444d37ac8a60f15b3ea3bb2ce3924481133855f8cba084`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 19.6 MB (19556694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb06d3817271be3db0822ecbdab86b22d1d27a7bbcd6f1bc8994721f6a344e8`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035c2e170be0d5bf3fea36f813f3597cf73ba164b6b0f5b74ab151864f240aa`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b893641d880dc991a0eca24cd715a5ca5af8cc8e76071cf2e9e3364c3583f43e`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:2133fc0b1ad6a027dabea4a4f2fbc4b29d56f78b39b3c1068e7c28a4f7e10395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 KB (187930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add13fc4dea2f5873c47db87b3dd3a2942ef4f998ae767feb6275f3f7d7613a4`

```dockerfile
```

-	Layers:
	-	`sha256:6574187e3c4c7411c29152486d4f632fe493db3a6ff86647f2d0a22bb510d869`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 171.2 KB (171233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b76905e92df9073ef3893754f50d651a7d1b63f960464dddfe8e3635613cfa`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:87e3860b4c7f8ae3889b773e60b03066accc24a84d1f33df3a9e84b88667e1a2
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
$ docker pull chronograf@sha256:a16688f6dab80c3e69e3f98a1773ab9e9047af104f56e6a36f6f57e0d3e4a112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70400590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6269eaf60a39bbb03b3ab1aa08d04babdfc90abd696909d9b08fa3b20b63ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666aed9bac86ceb0bc41e0a9d171f1160e447062928d33ba7f981b0868e81167`  
		Last Modified: Fri, 27 Sep 2024 06:00:52 GMT  
		Size: 4.2 MB (4209310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da746ea98382f062ac1d8ab5ad6ed7a23ef8e634ff1a7d6302f540029cc63fda`  
		Last Modified: Fri, 27 Sep 2024 06:00:54 GMT  
		Size: 34.7 MB (34738292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bec0790be1012f2c399d0734154fd0651a589dadb94eae3f992c6166247bd7`  
		Last Modified: Fri, 27 Sep 2024 06:00:51 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb80f58342ee1b10a7fed03bce92e55eb24ff69ba8439b143caedc002531b381`  
		Last Modified: Fri, 27 Sep 2024 06:00:51 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26571979d1a5cb4e4219c007b549fa9fa8aed4d67ff9ec7aa1b2227f5f6cfbb4`  
		Last Modified: Fri, 27 Sep 2024 06:00:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:62f87b112d8b8c2b58f4239fbe1ef0630ef847204c496e7a5daf97fe22264b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883833a3bb6ec34616e595ee2f2dd25ad14c2660c9d49d6f0009c5b449cb4f6`

```dockerfile
```

-	Layers:
	-	`sha256:fb391cef629ac97bc6f529d4de67682db92b6d431abb3a5c0d681578aee3198a`  
		Last Modified: Fri, 27 Sep 2024 06:00:52 GMT  
		Size: 2.9 MB (2893555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6187767858e82d9128b9370c9fc31af89c1c1c0f042a9d2721f96ff8642cb2a`  
		Last Modified: Fri, 27 Sep 2024 06:00:51 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:2fa1cdb073e6c2b5ac541eb2c0d3d981e29bc5cb9d2fb640d715bd8779aef09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63222773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde5536cd4bb8b42ba9e7711e010085741afdaa1d6f17175ffbc69a1226b0e5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bb2c98667dee735f1184796fa2cee79af730bd211287192474ebecde128ed4`  
		Last Modified: Fri, 27 Sep 2024 10:12:35 GMT  
		Size: 3.5 MB (3511606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7026d41bcad318f20a2cf0a6c7679b52f1c7176c9646801dbfca9c07669dbf2`  
		Last Modified: Fri, 27 Sep 2024 10:12:36 GMT  
		Size: 33.1 MB (33097463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d45a573dc26738f0af754ac64243410e4adeebb9dc6f7f002370c29ea1e1aa`  
		Last Modified: Fri, 27 Sep 2024 10:12:34 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc754763ecf15ebb623c62bc2a084c789581cefb7d96eea02804274abf00db38`  
		Last Modified: Fri, 27 Sep 2024 10:12:35 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fdb5ad12a4c871e29f9d49a8c0010defdaf002b21830c10e839cc4aa3057b9`  
		Last Modified: Fri, 27 Sep 2024 10:12:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:e171ebb3860e6ee6899651fec3eaaa81176dcc73c4c525a5064ca20e0cf0559c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2911475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0038ed29e64b73bfaf60424b017688bca0f7db78e142805ab2e628c0c314a529`

```dockerfile
```

-	Layers:
	-	`sha256:4628f597e16dd52368fd08014bc7f535407230f5106a14ca9ea0f14d1988b19a`  
		Last Modified: Fri, 27 Sep 2024 10:12:35 GMT  
		Size: 2.9 MB (2895825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc4447c0e04489c7b97731e1db286ef8bd0a2a0eaecbe8f5938ccdade78d0589`  
		Last Modified: Fri, 27 Sep 2024 10:12:34 GMT  
		Size: 15.7 KB (15650 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:044a5aa39f98e9eb8ecff5bb77946a2cf093ba3c4ac81a8cbab42e97c474a08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67547922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd5e28df840f0d2adfb4ccb8fc9aa4978fc7a9b4ff97f79843eda7e1515f154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bf811df6e4ba63716a64a12e52b203a40468f362a32ac642d07681fbe558a4`  
		Last Modified: Fri, 27 Sep 2024 10:11:03 GMT  
		Size: 4.2 MB (4210528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e80a2da2fac7d87da01503971ab846718f08f95f15dd648924294f2ebb4ad1a`  
		Last Modified: Fri, 27 Sep 2024 10:11:04 GMT  
		Size: 33.2 MB (33237852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c82b1eabf3ea8883f10a126efe11d73fd93b97e8ac20cfac18898f2225e9f5`  
		Last Modified: Fri, 27 Sep 2024 10:11:05 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1732cfddd11c8fd5a433875b4be169385a62af0e6e27c40986fd8f8cbacd5f`  
		Last Modified: Fri, 27 Sep 2024 10:11:05 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8ed549128e39c863dde59a2ba252c9de623a4d4e75605415c36edcf83e3d31`  
		Last Modified: Fri, 27 Sep 2024 10:11:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:05da5b711eb735cb3d0fb947c62127e14d64b11ad4322bd04fba2dce406b014e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2909671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0668c85f96255553a733201536aadd950ad4509d20ae8daca817681a3cb107`

```dockerfile
```

-	Layers:
	-	`sha256:ee6801b6f33e0c92f8f7830eb556c273c1e7f7b18a14c9cec0fe0e4d1ada9f6c`  
		Last Modified: Fri, 27 Sep 2024 10:11:03 GMT  
		Size: 2.9 MB (2893803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22e2ff99363b3d97d640a7562bebfc56cea1eb5d4d0a14cd34bcfc1e8f90d99`  
		Last Modified: Fri, 27 Sep 2024 10:11:03 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:ae9cdafc242e5e8ff9c96f3c65f39bb1538f574e7535c67c8e52cdaee219960c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:3de004b9b3957e329028c27dcaff35a81dadbe9556d127936b2043b86a6ccad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23496029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2243834b7dedb55ce7db37bb4e12aefe047628ff2f64cceb06de3ea38d017317`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a7812599bc616e92d0320eee1b26625969a25c2baf338377a45df6a273462a`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbda816b9a9bb7d03cfdc8c20a70fff0ed2202c45165aa32b72aa1bcbb3f58e`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 290.9 KB (290878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1337904852ed7215c8444d37ac8a60f15b3ea3bb2ce3924481133855f8cba084`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 19.6 MB (19556694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb06d3817271be3db0822ecbdab86b22d1d27a7bbcd6f1bc8994721f6a344e8`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035c2e170be0d5bf3fea36f813f3597cf73ba164b6b0f5b74ab151864f240aa`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b893641d880dc991a0eca24cd715a5ca5af8cc8e76071cf2e9e3364c3583f43e`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:2133fc0b1ad6a027dabea4a4f2fbc4b29d56f78b39b3c1068e7c28a4f7e10395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 KB (187930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add13fc4dea2f5873c47db87b3dd3a2942ef4f998ae767feb6275f3f7d7613a4`

```dockerfile
```

-	Layers:
	-	`sha256:6574187e3c4c7411c29152486d4f632fe493db3a6ff86647f2d0a22bb510d869`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 171.2 KB (171233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b76905e92df9073ef3893754f50d651a7d1b63f960464dddfe8e3635613cfa`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 16.7 KB (16697 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:7daa8dbd0bfc1ab6c94401866a4a8b641bd2c7f6b6b5a33543813202d9447c5c
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
$ docker pull chronograf@sha256:125187625990efd6a48fce14c01752d4b4407f2a1224295b09805761aa255f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71041287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f751997300e21848c12df346fa12fd4aafa45833ad21af285f9842ebe752633c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d07d5da88661f93c0c50fad9b4276eaee84bacd38bb8b75995998e0b4a6cf6`  
		Last Modified: Fri, 27 Sep 2024 06:00:42 GMT  
		Size: 5.2 MB (5224234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8208159551a726059130c71105a067336b831b7bd6f5cb26e71191f7baaa5cee`  
		Last Modified: Fri, 27 Sep 2024 06:00:43 GMT  
		Size: 34.4 MB (34364053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6bce6e9922c1406ce0fc228ba3981429ef21e655888bde790732b3d2f5c9e`  
		Last Modified: Fri, 27 Sep 2024 06:00:42 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb0828e7907a2b62d2aff7cd1dbd0e7144140632462ff42032298fc08849639`  
		Last Modified: Fri, 27 Sep 2024 06:00:43 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633ae64a48ff6892c1c033f2ca92aca49d59a89c557e2bd966ff835afd5cea1a`  
		Last Modified: Fri, 27 Sep 2024 06:00:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:caa27c5b45ebdc303e982753ff25faa0c640bfca4e3f38f899348c23ea768837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07123d17dbd33356aefeb52b31f9ee2a865c63512343629a06fb70636e7cf250`

```dockerfile
```

-	Layers:
	-	`sha256:92d5b73a4f57a884acaa52788a8ed24971dd16e79e78fa9a75d3db62508567b4`  
		Last Modified: Fri, 27 Sep 2024 06:00:42 GMT  
		Size: 2.9 MB (2949653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc23dd26cefe17f7db525a6c2898ff12feffe17ab057d7618b74765ecaded55`  
		Last Modified: Fri, 27 Sep 2024 06:00:42 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ee4a6c0dbb8c765783145746246a81c494a2a47b9b93e9ef158a85d8224c46fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63638365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5a65d7a1885a6fb45017d737ec3ef79ce39d55a1f1589ca04a47fad0b48d20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d94a61c847b8be9fb9dd892187d08b7c8f26954e1de0c4cfd3bb738830d63`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 4.5 MB (4489968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f429d46f365318663ed60dea354a6219e33aafff48742cddbedcc2a7884c5fa5`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 32.5 MB (32534689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab8a60b9d18febae55974da5ae855fc8b56e1e4d73154ce4ba7f646a7233a2a`  
		Last Modified: Fri, 27 Sep 2024 10:19:14 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ff7a1d180afb6169b87a0f93219f56c9ff239c5a774c719a9b54227cd05df`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4a44d1b395c1dadaa217cd595346cd571bc142eb5d9865534fa677d6f8bd65`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:5f3f340cfe74cd75c0a73ddc3456a856903c2d1cdf62aab6ee088afa047456f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e32b6d60a6ab119f68ffb49d76297b6dbba980c736529714f09dd7f5c8ed186`

```dockerfile
```

-	Layers:
	-	`sha256:35a2fe87e6d127d79a86c41dbed8d180b467df090c4a5650840129cfa88212b0`  
		Last Modified: Fri, 27 Sep 2024 10:19:14 GMT  
		Size: 3.0 MB (2951923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25dd2e26ed6ea66237abdca841ea97e6df0e88250afbdbb52e69a77f6b8bf5e0`  
		Last Modified: Fri, 27 Sep 2024 10:19:14 GMT  
		Size: 15.7 KB (15689 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b09d260c827c7125c4083e298ce081c374552b28a10812e8dcbe06ea47e4af11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67737090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c1c694d8c9f7ae6afc228633ca01ddbf320bb1a8b9ac6c977b78308c3f956`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160426fa618a05e6485fd0c9c9bc120a9f5ab4552eccff26fb855450aec759ac`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 5.2 MB (5208021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45620acd55388e99ee7fdff3a207c6e532a574b94690c66a5b0ec2917395d2be`  
		Last Modified: Fri, 27 Sep 2024 10:11:42 GMT  
		Size: 32.4 MB (32429517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ca9a425b5a28eefd429b0a393b090cac840a19e36c5062fff4aa66ca296cf8`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e07d0a45a746fba3158d8a330bd57181bc3fe353965e2a3e38328694be0b9b`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1413ae46bfb034d849ef0b2c8b253abd552784b6c6fb67ba47ab1ced19f252c2`  
		Last Modified: Fri, 27 Sep 2024 10:11:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:4a73b710325771c958f15d439ff04d7e6c618201c90546ba00877cb79e462b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c592fe3a3bf7d6246598e0ca2cb08d0cb3859875da19986da8657743f7f3bcb7`

```dockerfile
```

-	Layers:
	-	`sha256:839b0eb260285076b0bcf40be4605ec0156950acf48c0e6625eab7f82a1c3ea0`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 2.9 MB (2949901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b9f364151c45fbfa83b8f467696f8985f1c1574a3236f2fdf11e2059f8d1de5`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:37b5c7e1584b976325a4cf47765b8fda42450322140848b6a9866f81be4ccc23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:09656ce94b48203dd5d9ee02169abdb65d2cf11b17e7d333bb16b42b23984500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e33195e032fc8825dfaa92b5477faac60ffe62b14caadcffbad9a349378ea7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0a5f03bb2b35cfa73aedf1de5ba53534434400ac8d9f4c41d46551700c185e`  
		Last Modified: Fri, 06 Sep 2024 23:15:09 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7420049ffba52c598c5dbdd90979b04a7e8462288123c107bbfd4c1b86dc950`  
		Last Modified: Fri, 06 Sep 2024 23:15:09 GMT  
		Size: 290.9 KB (290894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bece9777b9b6d5916892108a0a05af3ddbf71f95d6ca308c169aa35569d2ff9`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 19.2 MB (19204060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9690baeefdae3fd111f1d9bd43f36642b058ab774a0f344ecf27e85d4dfcec91`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15057704d098d4902add4771b2d61fd63fdf0a81b26075cf461fa749d393459a`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4c97aa470a57cab7bef378d5046c463db4437ea362755715eb50375e8278bd`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0d658efcb4a3b108ec1547dabf5251317db019cdce531cc0008da925e94fcfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 KB (244688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d215f84514110511a5f92fd707815e2b953e9b5cffc6a8c1a7e975f6d1d4198`

```dockerfile
```

-	Layers:
	-	`sha256:bce9e4a677ac08eec4ea7090bde3467df9d30afe267db2cdf5ac3b9483260b07`  
		Last Modified: Fri, 06 Sep 2024 23:15:09 GMT  
		Size: 228.0 KB (227992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868055598088efb7dfc7be2a41356a1d13b6a506d683238878dc5e069bf03eac`  
		Last Modified: Fri, 06 Sep 2024 23:15:09 GMT  
		Size: 16.7 KB (16696 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:7daa8dbd0bfc1ab6c94401866a4a8b641bd2c7f6b6b5a33543813202d9447c5c
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
$ docker pull chronograf@sha256:125187625990efd6a48fce14c01752d4b4407f2a1224295b09805761aa255f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71041287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f751997300e21848c12df346fa12fd4aafa45833ad21af285f9842ebe752633c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d07d5da88661f93c0c50fad9b4276eaee84bacd38bb8b75995998e0b4a6cf6`  
		Last Modified: Fri, 27 Sep 2024 06:00:42 GMT  
		Size: 5.2 MB (5224234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8208159551a726059130c71105a067336b831b7bd6f5cb26e71191f7baaa5cee`  
		Last Modified: Fri, 27 Sep 2024 06:00:43 GMT  
		Size: 34.4 MB (34364053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6bce6e9922c1406ce0fc228ba3981429ef21e655888bde790732b3d2f5c9e`  
		Last Modified: Fri, 27 Sep 2024 06:00:42 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb0828e7907a2b62d2aff7cd1dbd0e7144140632462ff42032298fc08849639`  
		Last Modified: Fri, 27 Sep 2024 06:00:43 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633ae64a48ff6892c1c033f2ca92aca49d59a89c557e2bd966ff835afd5cea1a`  
		Last Modified: Fri, 27 Sep 2024 06:00:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:caa27c5b45ebdc303e982753ff25faa0c640bfca4e3f38f899348c23ea768837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07123d17dbd33356aefeb52b31f9ee2a865c63512343629a06fb70636e7cf250`

```dockerfile
```

-	Layers:
	-	`sha256:92d5b73a4f57a884acaa52788a8ed24971dd16e79e78fa9a75d3db62508567b4`  
		Last Modified: Fri, 27 Sep 2024 06:00:42 GMT  
		Size: 2.9 MB (2949653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dc23dd26cefe17f7db525a6c2898ff12feffe17ab057d7618b74765ecaded55`  
		Last Modified: Fri, 27 Sep 2024 06:00:42 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ee4a6c0dbb8c765783145746246a81c494a2a47b9b93e9ef158a85d8224c46fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63638365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5a65d7a1885a6fb45017d737ec3ef79ce39d55a1f1589ca04a47fad0b48d20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d94a61c847b8be9fb9dd892187d08b7c8f26954e1de0c4cfd3bb738830d63`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 4.5 MB (4489968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f429d46f365318663ed60dea354a6219e33aafff48742cddbedcc2a7884c5fa5`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 32.5 MB (32534689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab8a60b9d18febae55974da5ae855fc8b56e1e4d73154ce4ba7f646a7233a2a`  
		Last Modified: Fri, 27 Sep 2024 10:19:14 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ff7a1d180afb6169b87a0f93219f56c9ff239c5a774c719a9b54227cd05df`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4a44d1b395c1dadaa217cd595346cd571bc142eb5d9865534fa677d6f8bd65`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:5f3f340cfe74cd75c0a73ddc3456a856903c2d1cdf62aab6ee088afa047456f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e32b6d60a6ab119f68ffb49d76297b6dbba980c736529714f09dd7f5c8ed186`

```dockerfile
```

-	Layers:
	-	`sha256:35a2fe87e6d127d79a86c41dbed8d180b467df090c4a5650840129cfa88212b0`  
		Last Modified: Fri, 27 Sep 2024 10:19:14 GMT  
		Size: 3.0 MB (2951923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25dd2e26ed6ea66237abdca841ea97e6df0e88250afbdbb52e69a77f6b8bf5e0`  
		Last Modified: Fri, 27 Sep 2024 10:19:14 GMT  
		Size: 15.7 KB (15689 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b09d260c827c7125c4083e298ce081c374552b28a10812e8dcbe06ea47e4af11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67737090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c1c694d8c9f7ae6afc228633ca01ddbf320bb1a8b9ac6c977b78308c3f956`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160426fa618a05e6485fd0c9c9bc120a9f5ab4552eccff26fb855450aec759ac`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 5.2 MB (5208021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45620acd55388e99ee7fdff3a207c6e532a574b94690c66a5b0ec2917395d2be`  
		Last Modified: Fri, 27 Sep 2024 10:11:42 GMT  
		Size: 32.4 MB (32429517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ca9a425b5a28eefd429b0a393b090cac840a19e36c5062fff4aa66ca296cf8`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e07d0a45a746fba3158d8a330bd57181bc3fe353965e2a3e38328694be0b9b`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1413ae46bfb034d849ef0b2c8b253abd552784b6c6fb67ba47ab1ced19f252c2`  
		Last Modified: Fri, 27 Sep 2024 10:11:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:4a73b710325771c958f15d439ff04d7e6c618201c90546ba00877cb79e462b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2965809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c592fe3a3bf7d6246598e0ca2cb08d0cb3859875da19986da8657743f7f3bcb7`

```dockerfile
```

-	Layers:
	-	`sha256:839b0eb260285076b0bcf40be4605ec0156950acf48c0e6625eab7f82a1c3ea0`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 2.9 MB (2949901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b9f364151c45fbfa83b8f467696f8985f1c1574a3236f2fdf11e2059f8d1de5`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:37b5c7e1584b976325a4cf47765b8fda42450322140848b6a9866f81be4ccc23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:09656ce94b48203dd5d9ee02169abdb65d2cf11b17e7d333bb16b42b23984500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23143411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e33195e032fc8825dfaa92b5477faac60ffe62b14caadcffbad9a349378ea7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0a5f03bb2b35cfa73aedf1de5ba53534434400ac8d9f4c41d46551700c185e`  
		Last Modified: Fri, 06 Sep 2024 23:15:09 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7420049ffba52c598c5dbdd90979b04a7e8462288123c107bbfd4c1b86dc950`  
		Last Modified: Fri, 06 Sep 2024 23:15:09 GMT  
		Size: 290.9 KB (290894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bece9777b9b6d5916892108a0a05af3ddbf71f95d6ca308c169aa35569d2ff9`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 19.2 MB (19204060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9690baeefdae3fd111f1d9bd43f36642b058ab774a0f344ecf27e85d4dfcec91`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15057704d098d4902add4771b2d61fd63fdf0a81b26075cf461fa749d393459a`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4c97aa470a57cab7bef378d5046c463db4437ea362755715eb50375e8278bd`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0d658efcb4a3b108ec1547dabf5251317db019cdce531cc0008da925e94fcfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 KB (244688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d215f84514110511a5f92fd707815e2b953e9b5cffc6a8c1a7e975f6d1d4198`

```dockerfile
```

-	Layers:
	-	`sha256:bce9e4a677ac08eec4ea7090bde3467df9d30afe267db2cdf5ac3b9483260b07`  
		Last Modified: Fri, 06 Sep 2024 23:15:09 GMT  
		Size: 228.0 KB (227992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868055598088efb7dfc7be2a41356a1d13b6a506d683238878dc5e069bf03eac`  
		Last Modified: Fri, 06 Sep 2024 23:15:09 GMT  
		Size: 16.7 KB (16696 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:1cc6da0054d46b39d7f76476a4cab14573984f45f819b1a5c6c27cb08e49f10f
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
$ docker pull chronograf@sha256:df5e48dfb6888475185baa267c9eb28e61150b13ab47e9785880075140e6d706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71688777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791dcf50f0e8c6e537ec335b41b83954c4e55ed6b098b1c390b797ad54e9ba1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeea43404181c2ec602bab3fef62e49eb5efa9120387b6d0c761a5c99948d6b`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 5.2 MB (5224246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a770cd7d02dc0f5de3fc8b9db9e0a0f156e438b9c97fbe04594e95bf8c70c57`  
		Last Modified: Fri, 27 Sep 2024 06:00:54 GMT  
		Size: 35.0 MB (35011536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254d3fc74d1ae19bae9ab39d554695c919dadca8e112dcad6ff3699c313089b3`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58fd467626acadb92ad2565d2a612bf6e3f94606a869f2e719e929f520dd384`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f751054a33d3df228fc5e2e7991595d23dc537c20cb2e4fe1cc29d07881aaf2`  
		Last Modified: Fri, 27 Sep 2024 06:00:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:43af0cba892225b2200a651c602b8873a0530fff0408682de2bd6828b5032aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0927277c6ff59abd885bb7318236a6d58427a32f42dcf3ae3556e32bca6ef94d`

```dockerfile
```

-	Layers:
	-	`sha256:1eb30498173c68e592bc2dabcc8dbf6cf802f4c38bef8980d03d243d296f09a5`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 3.0 MB (2954803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c192348caa321be65b53dac38586e03f13e96931a35b293365001c78d40474a1`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 15.6 KB (15616 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bdf592919ffca0bf1ddaad09fe4c5d978fa5eaa9597c37b0c2a4541e7db8e780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64415016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3008372f3bd4d939e9701900fffb9ac47faafbbbb9021fa9a3f6766585d0cea3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d94a61c847b8be9fb9dd892187d08b7c8f26954e1de0c4cfd3bb738830d63`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 4.5 MB (4489968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12bf13944c580a885957d6bfd139a47f4d35846f130eb8f67736d15a619a095`  
		Last Modified: Fri, 27 Sep 2024 10:19:55 GMT  
		Size: 33.3 MB (33311342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af1991a83ff91d4aaeced69e1c4557eeaca144f6a12a1c7c7ec18924a57bae7`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96693920a689bc78013642fbf78eb6bec6b0bd59cbf545be178edeadce94e22f`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2305d41187863d38cbb97051eb1e86e1f30bdafbab5be50f042ec640ac99d`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:b4ebe3c4ce9cf0b97b9d22ff15866fe7332c7229f0d6e5e9eace035279c63f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d746261b5b16622135a4063a068eb673ce0b8a281167b9c84daafdc12bb315`

```dockerfile
```

-	Layers:
	-	`sha256:9c0d650e28722cca97477d0c10741c1d28c485305bac0b7caacb8ab44796a6ae`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 3.0 MB (2957073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1207c895792fc3398fcc184bc06f1db7804f60a12c99db263c25c01dfe46007c`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:33d5a94116d86521df24d6128533a9670346355e484f525c9e87d8700c4f217e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68489052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2114c5fa99f5e5373113faeed5b1c893b05e37d20a8870b5b4405258e636d047`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160426fa618a05e6485fd0c9c9bc120a9f5ab4552eccff26fb855450aec759ac`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 5.2 MB (5208021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e20edb9e73c5f071da2460f956d57464a97a08260fbe1b5becbcbc61f5dc9`  
		Last Modified: Fri, 27 Sep 2024 10:12:14 GMT  
		Size: 33.2 MB (33181479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f971dc54a1eef724ba7e373892a37fd828ca0bc8692f4a134502eabfe6d4b3`  
		Last Modified: Fri, 27 Sep 2024 10:12:12 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53782dc1b2172250e020591e6fa3ee544d1811543fde9632f3c22799f3d1bdb`  
		Last Modified: Fri, 27 Sep 2024 10:12:12 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bbfee2f1501b2b3b053bd1b6e7cbc6e9daf6438226295ae4a66dd53bcf3195`  
		Last Modified: Fri, 27 Sep 2024 10:12:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:4e3d281d89f3a2ef2fe98ad9d6e988f11363b3893e1138ec4ce999874c1e6a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355f01792199c7a9435e5e1a04b07ea6ef43bc57362bf3dfc239da4286b4d0e`

```dockerfile
```

-	Layers:
	-	`sha256:cb7e4c5db3e4b2386930569fc32a9c4d58dd84c526e13dc3012ce4d768eb40ea`  
		Last Modified: Fri, 27 Sep 2024 10:12:13 GMT  
		Size: 3.0 MB (2955051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2f5b47c17ed4fcfee5bcd143d80b97d231bfdf90e8c305b3296f52c2b93586`  
		Last Modified: Fri, 27 Sep 2024 10:12:12 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:6c2ad7aaa8cdee1d8af460a24e35c5219725c0ea0b1817060c1d79e72c3865bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:812949c3f257502553f5397c0bef4bba6d6533e458f3801acedc4b39f68a09ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9642d9bb422ce0ee1b4e48a3eab755e1bbc0ff4817cf09d90a0949b8b9e8dcbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4375f8599b9554a4c1c57fb6f5f7b616065458689f5f38657a13dc538e3468f8`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a1a1b72afc5dd4017f0f6f8feaa02fc6e9e1d7dce7ec870eae50247ebdbeb2`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 290.9 KB (290883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb79892634e836ff308cdf956c3e4f73608095d213dbe8d6d03f27fb9f4bff6`  
		Last Modified: Fri, 06 Sep 2024 23:15:11 GMT  
		Size: 19.7 MB (19672075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b94e0dd7f1c1a13ffb1e301a0f36b2432f8e52523b391643fc442caf4ac8276`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d120905fa82ff7b7e5dabadabdc1bda01b552eba23ded0cf06ac003f4bf940a`  
		Last Modified: Fri, 06 Sep 2024 23:15:11 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee32ab24cdcf70289ca8c386566836aa86c8b01b5929c728f7f1f9c4ffc1d97c`  
		Last Modified: Fri, 06 Sep 2024 23:15:11 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d8e7cd618c4d7b3bbd2750e3bd5288fec920b3e5bfd231110569ac6cdafdb557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 KB (249838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1327988e3866f1914bfb7ff2867b1e033304f617859345d8611c1d7eaefcc13e`

```dockerfile
```

-	Layers:
	-	`sha256:88c4c593588252baf2ef3424a50b0e4e7f963626f992e977e9f0636afeb2d1e9`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 233.1 KB (233144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ced52ac661bb9f31584750249bc99f5a39af0fc76f4ce42192643cc36c53041b`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 16.7 KB (16694 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:1cc6da0054d46b39d7f76476a4cab14573984f45f819b1a5c6c27cb08e49f10f
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
$ docker pull chronograf@sha256:df5e48dfb6888475185baa267c9eb28e61150b13ab47e9785880075140e6d706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71688777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791dcf50f0e8c6e537ec335b41b83954c4e55ed6b098b1c390b797ad54e9ba1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeea43404181c2ec602bab3fef62e49eb5efa9120387b6d0c761a5c99948d6b`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 5.2 MB (5224246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a770cd7d02dc0f5de3fc8b9db9e0a0f156e438b9c97fbe04594e95bf8c70c57`  
		Last Modified: Fri, 27 Sep 2024 06:00:54 GMT  
		Size: 35.0 MB (35011536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254d3fc74d1ae19bae9ab39d554695c919dadca8e112dcad6ff3699c313089b3`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58fd467626acadb92ad2565d2a612bf6e3f94606a869f2e719e929f520dd384`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f751054a33d3df228fc5e2e7991595d23dc537c20cb2e4fe1cc29d07881aaf2`  
		Last Modified: Fri, 27 Sep 2024 06:00:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:43af0cba892225b2200a651c602b8873a0530fff0408682de2bd6828b5032aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0927277c6ff59abd885bb7318236a6d58427a32f42dcf3ae3556e32bca6ef94d`

```dockerfile
```

-	Layers:
	-	`sha256:1eb30498173c68e592bc2dabcc8dbf6cf802f4c38bef8980d03d243d296f09a5`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 3.0 MB (2954803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c192348caa321be65b53dac38586e03f13e96931a35b293365001c78d40474a1`  
		Last Modified: Fri, 27 Sep 2024 06:00:53 GMT  
		Size: 15.6 KB (15616 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:bdf592919ffca0bf1ddaad09fe4c5d978fa5eaa9597c37b0c2a4541e7db8e780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64415016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3008372f3bd4d939e9701900fffb9ac47faafbbbb9021fa9a3f6766585d0cea3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d94a61c847b8be9fb9dd892187d08b7c8f26954e1de0c4cfd3bb738830d63`  
		Last Modified: Fri, 27 Sep 2024 10:19:15 GMT  
		Size: 4.5 MB (4489968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12bf13944c580a885957d6bfd139a47f4d35846f130eb8f67736d15a619a095`  
		Last Modified: Fri, 27 Sep 2024 10:19:55 GMT  
		Size: 33.3 MB (33311342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af1991a83ff91d4aaeced69e1c4557eeaca144f6a12a1c7c7ec18924a57bae7`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96693920a689bc78013642fbf78eb6bec6b0bd59cbf545be178edeadce94e22f`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2305d41187863d38cbb97051eb1e86e1f30bdafbab5be50f042ec640ac99d`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:b4ebe3c4ce9cf0b97b9d22ff15866fe7332c7229f0d6e5e9eace035279c63f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d746261b5b16622135a4063a068eb673ce0b8a281167b9c84daafdc12bb315`

```dockerfile
```

-	Layers:
	-	`sha256:9c0d650e28722cca97477d0c10741c1d28c485305bac0b7caacb8ab44796a6ae`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 3.0 MB (2957073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1207c895792fc3398fcc184bc06f1db7804f60a12c99db263c25c01dfe46007c`  
		Last Modified: Fri, 27 Sep 2024 10:19:54 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:33d5a94116d86521df24d6128533a9670346355e484f525c9e87d8700c4f217e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68489052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2114c5fa99f5e5373113faeed5b1c893b05e37d20a8870b5b4405258e636d047`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160426fa618a05e6485fd0c9c9bc120a9f5ab4552eccff26fb855450aec759ac`  
		Last Modified: Fri, 27 Sep 2024 10:11:41 GMT  
		Size: 5.2 MB (5208021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008e20edb9e73c5f071da2460f956d57464a97a08260fbe1b5becbcbc61f5dc9`  
		Last Modified: Fri, 27 Sep 2024 10:12:14 GMT  
		Size: 33.2 MB (33181479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f971dc54a1eef724ba7e373892a37fd828ca0bc8692f4a134502eabfe6d4b3`  
		Last Modified: Fri, 27 Sep 2024 10:12:12 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53782dc1b2172250e020591e6fa3ee544d1811543fde9632f3c22799f3d1bdb`  
		Last Modified: Fri, 27 Sep 2024 10:12:12 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bbfee2f1501b2b3b053bd1b6e7cbc6e9daf6438226295ae4a66dd53bcf3195`  
		Last Modified: Fri, 27 Sep 2024 10:12:13 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:4e3d281d89f3a2ef2fe98ad9d6e988f11363b3893e1138ec4ce999874c1e6a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4355f01792199c7a9435e5e1a04b07ea6ef43bc57362bf3dfc239da4286b4d0e`

```dockerfile
```

-	Layers:
	-	`sha256:cb7e4c5db3e4b2386930569fc32a9c4d58dd84c526e13dc3012ce4d768eb40ea`  
		Last Modified: Fri, 27 Sep 2024 10:12:13 GMT  
		Size: 3.0 MB (2955051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2f5b47c17ed4fcfee5bcd143d80b97d231bfdf90e8c305b3296f52c2b93586`  
		Last Modified: Fri, 27 Sep 2024 10:12:12 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:6c2ad7aaa8cdee1d8af460a24e35c5219725c0ea0b1817060c1d79e72c3865bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:812949c3f257502553f5397c0bef4bba6d6533e458f3801acedc4b39f68a09ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9642d9bb422ce0ee1b4e48a3eab755e1bbc0ff4817cf09d90a0949b8b9e8dcbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4375f8599b9554a4c1c57fb6f5f7b616065458689f5f38657a13dc538e3468f8`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a1a1b72afc5dd4017f0f6f8feaa02fc6e9e1d7dce7ec870eae50247ebdbeb2`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 290.9 KB (290883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb79892634e836ff308cdf956c3e4f73608095d213dbe8d6d03f27fb9f4bff6`  
		Last Modified: Fri, 06 Sep 2024 23:15:11 GMT  
		Size: 19.7 MB (19672075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b94e0dd7f1c1a13ffb1e301a0f36b2432f8e52523b391643fc442caf4ac8276`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 12.2 KB (12234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d120905fa82ff7b7e5dabadabdc1bda01b552eba23ded0cf06ac003f4bf940a`  
		Last Modified: Fri, 06 Sep 2024 23:15:11 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee32ab24cdcf70289ca8c386566836aa86c8b01b5929c728f7f1f9c4ffc1d97c`  
		Last Modified: Fri, 06 Sep 2024 23:15:11 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d8e7cd618c4d7b3bbd2750e3bd5288fec920b3e5bfd231110569ac6cdafdb557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 KB (249838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1327988e3866f1914bfb7ff2867b1e033304f617859345d8611c1d7eaefcc13e`

```dockerfile
```

-	Layers:
	-	`sha256:88c4c593588252baf2ef3424a50b0e4e7f963626f992e977e9f0636afeb2d1e9`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 233.1 KB (233144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ced52ac661bb9f31584750249bc99f5a39af0fc76f4ce42192643cc36c53041b`  
		Last Modified: Fri, 06 Sep 2024 23:15:10 GMT  
		Size: 16.7 KB (16694 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:5c0ef984976bfefd20fa4c75f0c6a875561bbe792fbc3a8dd1562d9f58bfe74d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:9db740a90a3f57dec9ee0694c4c0ca7108726332a5fcaabba6f511ef2d950a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31807854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721c7b0fb14defda16bb4c97e7b7973eba1357cb1f911ed888bf8de5ca1f2be4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08d447a64db49fbab2349074af3b28b29fc9f9e21d220e5ef3c257757c4dc74`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c1bf89f79d5659365e90141c4b9d64ac53a7d3fa453daec6c91390c55db6b`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 292.6 KB (292597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2fdc8712d053d3be5a3eac36d2ab85885a94a8420b9e1c618b83faba44cb0`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 27.9 MB (27866745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582c813a3de53aaf6186a47b93b9b94f71b222359ee33a8a6c852a2958d94a4`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b650264875e0bb719fef5c24879775972e4ffa43ffceaa93b671be1bf3888`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020946a0bc65717d96d8dcea5b6ff1b5cfe797c14fea294199a0d20f75399744`  
		Last Modified: Fri, 06 Sep 2024 23:15:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:805e972c1bb52dfc739c6298925601f6f43a3d3fc6ad154c942f138f34608910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 KB (257225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7796174809f7169d510b6c15dc3f9706d25fa63b88bae8d42cd72c6b5132604`

```dockerfile
```

-	Layers:
	-	`sha256:98e0e20b09ed16648a357232ac7fdf95371f498fda9265df1d848b41f11a678e`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 239.6 KB (239585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79b51922071e3d180fdebf5a7cbb5b9d23c8ad6154951adff660268d34e7618`  
		Last Modified: Fri, 06 Sep 2024 23:15:13 GMT  
		Size: 17.6 KB (17640 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:577141d452b5a3cccbd1db19145202a297d49c663bb79bbf779a8f34c6408f44
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
$ docker pull chronograf@sha256:bfca8025f4d68b495da72e098376d1fe63b9ae77c9a61aafda046b2ff18c83c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84242775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e22bd1094cc8989f1be4b77b98d19d05d4c8b87eb06a287102835d8d17f5dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931ce04a30de7c6159357982f3d2483c8c2e16e134f40bbe80649bee7c12da9b`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 7.9 MB (7874758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf564a41eef26bac0ce210e52a60894f64d25f1e817cc4a642e2f42a74365e70`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 47.2 MB (47217280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658b8c5e294f51d814ca552029bd6010582dac5ea08dbe1d40e0bec9f1139a1`  
		Last Modified: Fri, 27 Sep 2024 06:00:47 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73977342bb8e5122e366042f7d946ff6e9c68632cc5a9379401c22c50db6da8e`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ba1a31ceeaae1e5b7461840d0c8154abc898a3acb106b2453e99ab502b73ef`  
		Last Modified: Fri, 27 Sep 2024 06:00:49 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:10cad40c1cff2b4dd3bcf21fd31b5755c86469928cd837976ce396b39338595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d968b3d22adb6a6263cd5616772258f6d5b40f6fae2dd9db77e9c34091d1b5`

```dockerfile
```

-	Layers:
	-	`sha256:26882e00fc721d89c0a6ab2ae2b6ad7b447fb645c183a2a67a1567a038fb36d9`  
		Last Modified: Fri, 27 Sep 2024 06:00:48 GMT  
		Size: 2.7 MB (2690960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b147ce9a37e84ca85751772d5af43e4bbca08b527b0ec053c8b73856045b4746`  
		Last Modified: Fri, 27 Sep 2024 06:00:47 GMT  
		Size: 15.9 KB (15934 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:f4e397fb399f64fcf07bc43bab529323cdb22432f4b823604d4c55060acc973c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75516183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a78871ba44f021ee17c3b85942764da865fff0d9b4664f97a8adb15c31af624`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93075f5189215242875cbd3d5e513405ee4b4d1b4e8297d1c0d2e4465465568f`  
		Last Modified: Fri, 27 Sep 2024 10:21:03 GMT  
		Size: 6.5 MB (6497563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b57e864f3a4f39835c3705faaf75356ce8308b7033d8a18f5245e4cc695152`  
		Last Modified: Fri, 27 Sep 2024 10:21:04 GMT  
		Size: 44.3 MB (44276006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfa51aa34c540038eb1c3c1f16872ece2f1da8f732de20f7cd25317d28a2af4`  
		Last Modified: Fri, 27 Sep 2024 10:21:02 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba15c11dcf19bd71b5605fb06ceec46dc294d94cf41b8c71adcd15c3273649ba`  
		Last Modified: Fri, 27 Sep 2024 10:21:03 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9106328ba6ab3f511e9697a68f801fbd8cf7e837fad34c78fe682682ecc03e`  
		Last Modified: Fri, 27 Sep 2024 10:21:04 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:56b9a7f2c2e93cb638a90d8f7a10b78f01482e174ad0d46d778dcdcf7ac7d956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1b21096c93a71510558b4645364e5cfcaab5c9516d9893db2d2318b5373efb`

```dockerfile
```

-	Layers:
	-	`sha256:14e202c2801d21db907ade88851037fdaa7e6c044e4d8b627466c3c848fd7d85`  
		Last Modified: Fri, 27 Sep 2024 10:21:03 GMT  
		Size: 2.7 MB (2693256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bf294098e564cb51d47ce92f9687e5bb12c4627afcc4418083b6250c982704`  
		Last Modified: Fri, 27 Sep 2024 10:21:02 GMT  
		Size: 16.0 KB (16009 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:23cbe7b62f6dd8d267f7b5fdac8d27523ab31c0fcaa72f75b201b6c922a865af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81802521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4d47528283cee27d646e2bb2c4b4e80911fd53583bcd1a464c4695d7f016cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6bbfdabfa81c2097fa252bb22668759ae42a543d8438e950c1b358320e23ab`  
		Last Modified: Fri, 27 Sep 2024 10:12:53 GMT  
		Size: 7.7 MB (7651311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c32089a726eece93219d436dcc8f441e6dfbfa42e37aa693973505516817066`  
		Last Modified: Fri, 27 Sep 2024 10:12:54 GMT  
		Size: 45.0 MB (44970387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3840bf77bfc5b8546225f8aac0852984537b572a5ca7b5f00beecc05e16c974`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219ac5eb808868491929c75e1e79af7b42478c21e319330ff2f5141f8e832bf5`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef5af92adc6445bde61b8c40e72f420c99bba684a6825e3fff3bec5fee1cede`  
		Last Modified: Fri, 27 Sep 2024 10:12:53 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:61b9b5f3b618e8d621b54d8dcd486f17985c03fbb7f92820e1dc7ecc76de5325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2707463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3f533ec676d7191bff30fb070d29396bdb3320a2ea4bae035b413417c748fc`

```dockerfile
```

-	Layers:
	-	`sha256:d7a87eb439c233b417a4aab085b83c9f11594153953278e14254670ebaeefb1e`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 2.7 MB (2691232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0978d3b28c381c6ce79f8c21fdfd756db72e9f46602c40e3419b00fb2df771`  
		Last Modified: Fri, 27 Sep 2024 10:12:52 GMT  
		Size: 16.2 KB (16231 bytes)  
		MIME: application/vnd.in-toto+json
