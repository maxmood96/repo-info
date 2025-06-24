## `telegraf:latest`

```console
$ docker pull telegraf@sha256:1b4dbebb724c61726c1c44edc15067a176020c35207620e06212c2e72339435e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:25cf4d910e75c1631c60242fd0fb777697de7287538a6390f22f5ec3f28b3479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169929889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7745ba6757add3cd32dbe5b328c7d6e30a54721b41f87744ada181c4dfe6a0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04f894c9e9144c5a44b547f93fa55733fc6b7d2ddc31d5b9c13ff2307a74fb7`  
		Last Modified: Mon, 23 Jun 2025 21:51:45 GMT  
		Size: 18.9 MB (18946572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a701658913f63bea75a9c425ccf195a5ab83307bdfb9c2b391e2b8af81642`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f8bb75caf60e34009e2b31b54126f6ba87c97ab1a061ca78d41d41ca67a86`  
		Last Modified: Tue, 24 Jun 2025 00:10:41 GMT  
		Size: 78.5 MB (78470943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a89198acf78f2e74f68400a5555343b3301e654b6eb77b85f9670d463fac329`  
		Last Modified: Mon, 23 Jun 2025 21:51:42 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:bbeb16248fca8e87a79da0088556d9f67d89591bde1f3f5398ec33426f995c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07064035e41321f35dca453d90152bfd2bd683036ae7f0fd1e7975bd50f84c70`

```dockerfile
```

-	Layers:
	-	`sha256:836585210c55cda93ccb51298f721a3d39e79b9c3a16e1ed5030c7e28e184432`  
		Last Modified: Tue, 24 Jun 2025 00:10:30 GMT  
		Size: 6.6 MB (6637089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bcc5c93c20fc60dcaf0b42c95872afc8a517d122dcfc8d8ea437cbd2e4bc0d8`  
		Last Modified: Tue, 24 Jun 2025 00:10:31 GMT  
		Size: 14.8 KB (14772 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:234efe5eca43c454934e2ab1443c098888827e15935897ddf5591b415b6822d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156370914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1668d1e3bbea6c1e6c184f99a888bc2e379791ddd259275c5c2504b3f23e4c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449907dadb3e534574a2fbaebc996906a8ec5bbb4a2b536a5bf81fd8b82f603`  
		Last Modified: Wed, 11 Jun 2025 15:11:55 GMT  
		Size: 17.7 MB (17725142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9378665d1fbace5ff58281c8769d5dd7956ae34dd48f5981527d5a253dc35f35`  
		Last Modified: Tue, 17 Jun 2025 22:02:03 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeb49456c542ce43f24e8fe7a7b61aa78e8c5125a9b22659ee1d54a727a32bd`  
		Last Modified: Mon, 23 Jun 2025 21:51:28 GMT  
		Size: 72.5 MB (72510527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf28e68a60f2fe7286b78b3f256881fca4a85d6f547c8ccf235ec90abe89252`  
		Last Modified: Mon, 23 Jun 2025 21:51:09 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:d9058e4d487567b1b879300724f7c0b4f974a336c228ebd46288a7ea0f4b4c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dd0fa53f237d51a161e634a1fca2cc256807bea0853ad0ed5ac32326aad5ae`

```dockerfile
```

-	Layers:
	-	`sha256:041b7a1c87fa324981c03e424373940afbcb8646e951d117c217d7a0c8e6caef`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 6.6 MB (6631692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab0e104532ca127ca2198d21eb07e54f1f2981be5ad22e1d91a71218f5b4578`  
		Last Modified: Tue, 24 Jun 2025 00:10:37 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:07c7b62be9ff3af75017a2ec363c86c8f532566666984ec7fe3e9b5d725bf02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161914465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1e713e42839bebab87906ae3f79b1436f086b39a2128676ead6bf9e8958234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENV TELEGRAF_VERSION=1.35.1
# Mon, 23 Jun 2025 21:43:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Jun 2025 21:43:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Jun 2025 21:43:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Jun 2025 21:43:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f54a5ba270c8c951d04c03b722b8248bd8f3e41dc8c3ab443d6aedcae4165f7`  
		Last Modified: Tue, 17 Jun 2025 22:07:58 GMT  
		Size: 18.9 MB (18872028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99487c7a328ad568d7b219d1ba0ac111561192b88793fd96629fa10378b2712b`  
		Last Modified: Tue, 17 Jun 2025 22:05:52 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e599e5d86c57376b30aa8f44334f650e9144a7fa02612ea4f92f62cf9ae12`  
		Last Modified: Mon, 23 Jun 2025 21:51:20 GMT  
		Size: 71.1 MB (71149623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34431be71109f4ab0dae3e9e3138dbc83aa025cc99e6a77b8f79ba679a5e452`  
		Last Modified: Mon, 23 Jun 2025 21:51:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2e7923997956104d616cc6492446b03d043ecc1cc2c49259535fb5368a079c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6652671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bfd7e3c2de91c77e6ab9a7ea0f55c3a2ab4df0548cd0b06ead4f2473362318`

```dockerfile
```

-	Layers:
	-	`sha256:a50db35ca596919f9dbd929efc85dbee4d4333c84158f8495ffa05494acccbd9`  
		Last Modified: Tue, 24 Jun 2025 00:10:43 GMT  
		Size: 6.6 MB (6637777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26123943db9a6853d77aadaecb866e8273c121d5a8814e9eb0dc363e0bf63a45`  
		Last Modified: Tue, 24 Jun 2025 00:10:44 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json
