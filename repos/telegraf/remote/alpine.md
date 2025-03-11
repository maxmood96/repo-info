## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:54bb44420c2bad6e4dbc017a140107ef0f2fd66192d22e4297228e6657257517
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:307dff9d25edf62e990b02f7427799852b411acf9defbe0a746da41334fc2280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83181342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a2f2610a65d4727686a80d149dec5e8eabc84964f8672c121ae59bf5129b0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENV TELEGRAF_VERSION=1.33.3
# Tue, 25 Feb 2025 19:20:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 25 Feb 2025 19:20:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 25 Feb 2025 19:20:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2025 19:20:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38049afbf35aebc48750aa922431b39f2fc798c04bdbe76bd6ae3b281fed2ba5`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073bd82841c579643840dc44375728fdc6290a0b75a5c7c7a9f475e2fd33df5c`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 2.4 MB (2448010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804d0c3c2f1304b11b15aa3615c2ae951b7aa267345cd8caebf2534c09f432c4`  
		Last Modified: Tue, 25 Feb 2025 23:27:38 GMT  
		Size: 77.1 MB (77105828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecb0ae4356bd231d8a07dbc4b04fad1e156e8bcf1f303290303cee493817e28`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7da2eb2660beb59ed82ea1425fe6e4bb730c61f69a7197c2ed08ebc3cdc021d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028284213fd46027a1ced219a906753338d9c763850718d8f063be618ea2b50f`

```dockerfile
```

-	Layers:
	-	`sha256:f43b03bb1a8042cca6df1e56fbc4d2705ce1afa316953c6a42fa05d0dd301ff3`  
		Last Modified: Tue, 25 Feb 2025 23:27:37 GMT  
		Size: 1.1 MB (1094776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b15e5bf904084afce0335a323cb7a49eb0e277254fb8c1ce8618e0518df0650`  
		Last Modified: Tue, 25 Feb 2025 23:27:36 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:66f341f3d9c3a9ed063f589d97031bfcbb352b0b7bbcacc1566df33672e8d468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76308949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf5fed543e27d83c18311052a57b5fb1d3326d209325a28a1f9c6b4233bc6ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENV TELEGRAF_VERSION=1.34.0
# Mon, 10 Mar 2025 21:51:36 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Mar 2025 21:51:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Mar 2025 21:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Mar 2025 21:51:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762a8644aed736cbf4c123385c72d805586043830867b764844d918e74198748`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb2ac6e1bddedd29dec17c8c60b881e71180e9057717b8bedd88a5ddf29dff`  
		Last Modified: Mon, 10 Mar 2025 23:11:02 GMT  
		Size: 2.5 MB (2533888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20701fd7f7a969a1bb9baed0533147a4628e6b1e40e06cc6766a8c24bbb4d7ed`  
		Last Modified: Mon, 10 Mar 2025 23:11:04 GMT  
		Size: 69.7 MB (69683288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a78f405bde17beaef6b5427477777ec46ef79f448a34a5696059ea9640d53`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d28fc275fc1644b0c1ced6d75ab3a8cc29421bcdc61078be517d7f594dd623f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b056bb10daf2d2da12f3331ed098a4815715ac4bd65fbae4b8dcd59ee35d37`

```dockerfile
```

-	Layers:
	-	`sha256:c4e80edcb5ee8ddfb281a98ae137fdbbfd549dd05f4446a03756b9153a9cd647`  
		Last Modified: Mon, 10 Mar 2025 23:11:02 GMT  
		Size: 1.1 MB (1095009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e30c7e59efcf50a5d390853fa8e19f748b27cede182f74e6748210d6a8f5d49`  
		Last Modified: Mon, 10 Mar 2025 23:11:01 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json
