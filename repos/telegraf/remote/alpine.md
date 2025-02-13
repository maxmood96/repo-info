## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:9e40032cbca6098b3cfa521ecbd10413ba77e80d909b0200f08026c2a37ae8ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8eaae4bb7cbc633c9ab981a9df6e8b85e698980a9e47dddc4c7710f9eb788aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82200802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab241f084f1d9936d253e47140b85dfe5dd5c575dd7cb5b3bb567a2942bad803`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083d78968bc5956a4a06c96a8139028e36877ca2fe3c508a949b178a67fc68fd`  
		Last Modified: Tue, 11 Feb 2025 04:11:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7465b11656ffe6575003f16e24d638aac670126aa970ef1c89cd0acd988bc29b`  
		Last Modified: Tue, 11 Feb 2025 04:10:52 GMT  
		Size: 2.4 MB (2448148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a66e5f8f48a99f8518b913d81b061c700de6442da7fa0445e15c8163f7db04`  
		Last Modified: Tue, 11 Feb 2025 04:10:54 GMT  
		Size: 76.1 MB (76125790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d813ad74d5ee7cc119cd8ca406bbfcdc52ff92b2953114c412db0a27a7a311be`  
		Last Modified: Tue, 11 Feb 2025 04:12:07 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4c311b83557449b77b394a1aa0f10bbaf797bd3ff973d1aa959325e4716b0a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bf4f0d4e1a54b51815a5b66e9f730fd10f3b8cf02654bf4c569229bf104e4c`

```dockerfile
```

-	Layers:
	-	`sha256:acc9753f129c11512a1774b99b0d69c643471500e8195cb24ca4c912fa9c49d8`  
		Last Modified: Wed, 12 Feb 2025 00:53:56 GMT  
		Size: 1.1 MB (1093847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b608ba32197f9acdcd9ed066db74933eb513fb528bae611a305f1a69dd51b240`  
		Last Modified: Wed, 12 Feb 2025 00:53:56 GMT  
		Size: 15.3 KB (15262 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9287004b2b038d128f8afa0a0f08b45bcb2f145ba821a3677a795f58e0e4361b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75468967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba53ef7f9418e997738677a669bf2a09c08bb587696551897826259aea619986`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENV TELEGRAF_VERSION=1.33.2
# Mon, 10 Feb 2025 22:49:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Feb 2025 22:49:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Feb 2025 22:49:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Feb 2025 22:49:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb58607870e908afefc0f96f5d47a21d074e703f07b9545b48b883ec8954f1`  
		Last Modified: Tue, 11 Feb 2025 04:11:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022976a7a161e655c5db9e87bbf5bc24423d5444e88a97373d7db86be648a7f3`  
		Last Modified: Tue, 11 Feb 2025 04:11:13 GMT  
		Size: 2.5 MB (2534024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4cbe4424f830b2ae3a255b605a69e2775faa7d72dadf39b83a569d8c1a577e`  
		Last Modified: Tue, 11 Feb 2025 04:11:16 GMT  
		Size: 68.8 MB (68843567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6b811a0d01bbc36988dc3cf7541daddcc08d93735e4b34ddaf6acadae8005f`  
		Last Modified: Tue, 11 Feb 2025 04:11:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:009b3d81e3ec988e4fb26f3962dde2801c2f26fd4720f37022bab74d2e34826e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cc9a94b2768a06b6bda16b3bd787f008839086e32b8c11907f8261e7add120`

```dockerfile
```

-	Layers:
	-	`sha256:4b50eb27359bd01cd52bf3f842278253a07c681a6502dde0bf76448474b119bb`  
		Last Modified: Tue, 11 Feb 2025 08:59:16 GMT  
		Size: 1.1 MB (1089486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74083986b039cb586b5610dff6f34d06b86fcfa25bbd2b59bd754f4a4a76312f`  
		Last Modified: Wed, 12 Feb 2025 17:19:23 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json
