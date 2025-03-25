## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:dee2d147ad809945ee27efcd8dd792ea8624190f66ec60c6ba3704a7fa9ab422
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48bc3b417f34690563376703ac95e3b79e5f43ddaa1ede038127424889a5bc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83511692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f1971b9e03d40c7845d1f957b6409062e09422ba57f80db5fa2561ec6342d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 21:11:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENV TELEGRAF_VERSION=1.34.1
# Mon, 24 Mar 2025 21:11:50 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 24 Mar 2025 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 21:11:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373686c6905b211780de0ba5f979576bba3043c8eb39137bd9d74751e5c956ee`  
		Last Modified: Mon, 24 Mar 2025 22:16:19 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e767fff4408b53cb396fb91d0580a4f93f7cc1e3f0891e3bb5e9bf08ec6303c`  
		Last Modified: Mon, 24 Mar 2025 22:16:19 GMT  
		Size: 2.4 MB (2448008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500e93397671026cd289f85a1b420037c517d1a590f4a2c90766f5d60c165679`  
		Last Modified: Mon, 24 Mar 2025 22:16:22 GMT  
		Size: 77.4 MB (77436179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef62b6a2baf743e6d9ee9468bf9a00e161f699ed4e2881bc08fe072f1915f495`  
		Last Modified: Mon, 24 Mar 2025 22:16:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:fe3a4d28b60957c8863175a97296da064767663e9f29c4b407bf794ac5cd62a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1113832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cdfdd4dbda73d5175cf5dff31f52c402e51f216defdc27f1af52b5e70cdf1`

```dockerfile
```

-	Layers:
	-	`sha256:e2c93f3a39e003e170ff682c9f75463d7d15af634308b2634b344af8461d91a0`  
		Last Modified: Mon, 24 Mar 2025 22:16:19 GMT  
		Size: 1.1 MB (1098571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edcabd527f4346510fdb44756693934d5cbe09fb242af01666290ffb7bede0bc`  
		Last Modified: Mon, 24 Mar 2025 22:16:19 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:9847c4080ff21e95a09eb83bed62108a9c4a07234b1a2e98ee7c9e58c79d45e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76335502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d15d02aca66ad2e6c17e4b80210e40be1c2dde2e89d013a0f7aaa27f0e0bc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 24 Mar 2025 21:11:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENV TELEGRAF_VERSION=1.34.1
# Mon, 24 Mar 2025 21:11:50 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 24 Mar 2025 21:11:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 24 Mar 2025 21:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Mar 2025 21:11:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3d2c5f4fe30e9274fa0a65ad21afbbe2ecc6d66f30eda37eb288fd49dfc2d5`  
		Last Modified: Mon, 24 Mar 2025 22:16:26 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6e8f2da43adeac4af2b9fbfcd5aa5339280c8ec4eff3306fe2b04b384ccf9`  
		Last Modified: Mon, 24 Mar 2025 22:16:26 GMT  
		Size: 2.5 MB (2533917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6bcda0af26219f46c6d1f1f1f0d176e9f1ed6b32efaaa5b630bbb476da541`  
		Last Modified: Mon, 24 Mar 2025 22:16:28 GMT  
		Size: 69.7 MB (69709812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1d63bdaf9ad1bc798109cb211969945d1acca30b4a8e7231e8d44066db0a37`  
		Last Modified: Mon, 24 Mar 2025 22:16:26 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:786d11a5154e8fed03d0c5b315447e2d31245cc28f71e5c6b01f824ee596123f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1109595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36d9775c5a0d81e8e442d725013ff1a72183ef583520806dc42cb9b4333d7b6`

```dockerfile
```

-	Layers:
	-	`sha256:0e17546d955bcc4f764fd3a5f602108bb446e1ed33e6bec1b2a97f807c742df1`  
		Last Modified: Mon, 24 Mar 2025 22:16:26 GMT  
		Size: 1.1 MB (1094210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:435dc00fcfa2ff0f4349eba831385de0aae27e61910262db149511e7c7b701df`  
		Last Modified: Mon, 24 Mar 2025 22:16:26 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json
