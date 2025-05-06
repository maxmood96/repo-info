## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:0f6c0611a6345f44f138108da05fa2c573b48606424e99850745a5ae4eb9b05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:645c9bfb6439247ce432fa016aa288a7c063b546dcccc1a1efbd2047ade7a000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83066472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd00bc80283e5dee38fcda1db589eb3f70d4ad664d029b857f5a315a414d7bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 20:28:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENV TELEGRAF_VERSION=1.34.3
# Mon, 05 May 2025 20:28:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 05 May 2025 20:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 05 May 2025 20:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 05 May 2025 20:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 20:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e036f026e2ca6ce0fb410d4555de5d0b0d3e8228adc8d209c04e482abbd86453`  
		Last Modified: Mon, 05 May 2025 21:43:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0861b20c0225a79f2e78e27dc922e52c78082d6a774646a4d2d8f7548508a7`  
		Last Modified: Mon, 05 May 2025 21:43:48 GMT  
		Size: 2.4 MB (2449575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d80681ba2be41917f5f0ee9aa4583465fe80682feff10dce7ac9d8787ca085`  
		Last Modified: Mon, 05 May 2025 21:43:49 GMT  
		Size: 77.0 MB (76989395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f559c698c5228b31a27032040a2e50b37d397a2bc72fe8c569fe8ae8b4d28c`  
		Last Modified: Mon, 05 May 2025 21:43:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b776a430c712f166e58d64205f9395ff4831bd55f8bf69786e3f0ed8ac68bc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1116095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000dd7750d7df88059611520d73ca93811803be83a179ce099a8a6c0ad12539a`

```dockerfile
```

-	Layers:
	-	`sha256:f7220dd330064a19390f85ae82c72a2dacdb31e562fc20818899cc094e0bd61d`  
		Last Modified: Mon, 05 May 2025 21:43:48 GMT  
		Size: 1.1 MB (1100832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0433ef5061b69291b9e8aafea4752870b788cb583117e263f986c7c56363ceae`  
		Last Modified: Mon, 05 May 2025 21:43:48 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6e8da97c1ee51411a8edceb8a9875e09026b87fccb6b4cb784d5ca2262344c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76670094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0927d5f4c68ac11638b534b35c501d05ffdf5d9c553c9826f868bdd4cf064805`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENV TELEGRAF_VERSION=1.34.2
# Mon, 14 Apr 2025 17:23:46 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 14 Apr 2025 17:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 14 Apr 2025 17:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 14 Apr 2025 17:23:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d5d995abdafd4a08c914e411233ba7edd1fd18c43edff36c7e7aeda4ed250e`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601ae3ffdf2a162bb798b5d6cd90fe82d45f9806f51408017234d7b1e575a3a6`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 2.5 MB (2535625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0ddb346a4a30c1c699ca70797d5030ab47b4bf27bc919a1a1aad8edfb15bee`  
		Last Modified: Mon, 14 Apr 2025 21:45:26 GMT  
		Size: 70.0 MB (70042697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bedfac84d629a52aaa04b5e98913b2927c261fa9950fe9d7fe5dd2721d8ca14`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:1e7dd201f0d047341155a882081e8762f241a5c05d0353ad34ac76ae74646d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1108612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19936f71adaed0f2c1a0df5618755a7f9d2856a40f4ccb94369c8cbe86707a49`

```dockerfile
```

-	Layers:
	-	`sha256:4a74a116076baec51e748e51b41ae8f8ac50b9e9858f3231e657429923b7c239`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 1.1 MB (1093227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36918405b96e57ccfe4cd94c2aa931ecc960aaa003d8649cba9cc1eb84899df`  
		Last Modified: Mon, 14 Apr 2025 21:45:24 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json
