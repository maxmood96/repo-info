## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:7bc2330dc3b7356df347af8c305504f340d6c5a0c0052dbfd569767c315ad061
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a2272748772d7c30648457b5031fc34f2dd85ea293749b6c0067a66d4236b8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c786416ce02274e21073bd0803d85289acdb85e3b68d9ca8647eaebcd6dd03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.31.2
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5597b23f21f5f80ed659b2fdde0ee522134e91341a885545638bf227000003`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca1d52320e512bc1ca403beaf0e87bc88071507bd255e2fd970aa0203f2266f`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 2.5 MB (2451693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f707eb959d2d03b3779c4371892513ba971036422b636ead8f0ec7988f7d6`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 66.1 MB (66074197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0decc0671675c1bb2cf6f9812c84d9dcbfe05bf41b3e0776e974bbf94f00d96`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c2aa5b78ab4b62836fb333b72446c7c0a4a50b7943748aa1ebe06ef694f14b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1078151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300cb1cb85381f511e99316f476ad6f374c4e3b0df0202891faf7a18e65b070c`

```dockerfile
```

-	Layers:
	-	`sha256:c045a5b619807d9aa31583532ace824723d8847df2285b9801929435f4a52938`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 1.1 MB (1063115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc19b6fff1ee8a85541d5112a361dce7ead509c94a0f4470f1fa4a852bb2c1f`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dc01149fac816a77ac869178a0f3c5897d197ea7f507e624326b47303aac60de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66736279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56dc490a08098a76eaf1bcfc8a235cf0e2fdf48ac4b44a693d066561eee1a69c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jul 2024 16:07:53 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENV TELEGRAF_VERSION=1.31.2
# Mon, 22 Jul 2024 16:07:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 22 Jul 2024 16:07:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jul 2024 16:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jul 2024 16:07:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0d1ffb94d496286226e500ca461ae4c84a6368b8c23b64dfd72955579f654`  
		Last Modified: Wed, 24 Jul 2024 10:08:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96666ef40bebea34c4984a3d34ddd3118468eb0087d117403688b0408735f6`  
		Last Modified: Wed, 24 Jul 2024 10:08:09 GMT  
		Size: 2.5 MB (2537424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bad44ddb0260924b2bd7f2f723028ef1a2c78b2d9f0c6b74cfecaf9bef4ecd6`  
		Last Modified: Wed, 24 Jul 2024 10:10:33 GMT  
		Size: 60.1 MB (60111314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db01da1ab0fdd4c554341294d3abd8d277b1d26011a2d10ec602dbf3021a9d8`  
		Last Modified: Wed, 24 Jul 2024 10:10:31 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8adfe7a0653d26a53b31a4518d3fd9be05fc427cb70002f7a2cf3c48f69bc3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1074912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c9b3d40486dc476f7edd70a97c71a7eae85b9930ff6e1ab94e5daa5df067cd`

```dockerfile
```

-	Layers:
	-	`sha256:364af2e9f8b4ab6c96d891f709a1ed35853f2aeb1a9eed520aadc26febf7f9f9`  
		Last Modified: Wed, 24 Jul 2024 10:10:32 GMT  
		Size: 1.1 MB (1059589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57024f9f24b9a2b2bb873b33dd87aef55005fbb99e6f446367bd746b188c597b`  
		Last Modified: Wed, 24 Jul 2024 10:10:31 GMT  
		Size: 15.3 KB (15323 bytes)  
		MIME: application/vnd.in-toto+json
