## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:f8c7e31adf71501c6008b6490729f96bd250d350da678e17ec030dd1dfefb51e
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
$ docker pull telegraf@sha256:82db004093bbbaea8c9deef8f4fc92752c2720d217391af0479c9032cf4e53bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66715791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dfde127891469f8009177857aa32bb0adf9ae21ba4fb05a7c3442b57d7f712`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENV TELEGRAF_VERSION=1.31.1
# Mon, 01 Jul 2024 19:20:29 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 01 Jul 2024 19:20:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 01 Jul 2024 19:20:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Jul 2024 19:20:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eba8dd2e5fd29bab729423d14db817b55f44940b10b1e32f92827462e6e423`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ceccb2cc5da64d07330ea2171242f64cd0bd8c1a58c50cf78d5afec75bdb08`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 2.5 MB (2539679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da2f3607c9ebd8d31adfea01b8869e3ecc164fe7711dc33994a8253da973947`  
		Last Modified: Mon, 01 Jul 2024 23:59:26 GMT  
		Size: 60.1 MB (60086705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16e1577aef80fc7823214e09bebb6fe8556f86173907f1d23e6b46d84c923b`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e3148bdad776e71b356d54317b7473aed6523aa96cc09e440d876e25e51656c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1004624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf6a5a2db81e49f9aba624d891858033ec37e2233f9c55234f71aa8c28437b0`

```dockerfile
```

-	Layers:
	-	`sha256:d24c61ecd55103603c7f91fdf5c6f18b9938562ce87de478877e3ae358d5ab6c`  
		Last Modified: Mon, 01 Jul 2024 23:59:25 GMT  
		Size: 989.3 KB (989300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5777d418d3d75900d18eba587c27585dcb2eb0b7e90c248e8890f74558e32fa2`  
		Last Modified: Mon, 01 Jul 2024 23:59:24 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json
