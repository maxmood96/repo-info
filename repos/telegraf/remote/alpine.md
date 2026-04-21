## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:d96a87891f25955c267ff09c866c749ba6e5a3f00b922af7d327553c8eaaec59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9329f79e4f61821fe34e6675a45e3bc5ba490a10c29b78fa1b07fb96d7413f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89341570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e446ecec12ac9e43036b90aaf265da167e1f9a7bcd791a4f54b88a61bc77c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:01:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:01:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
ENV TELEGRAF_VERSION=1.38.3
# Mon, 20 Apr 2026 23:01:19 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 20 Apr 2026 23:01:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2026 23:01:19 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ba1ca119c95dcc4002e43d75c16e92ca9ed5da328c91b893b12b7255d7808e`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af90712c1065542090e47fc7cae5ac33079ab2ac78f365778f253d4470f006a9`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 2.6 MB (2615621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c6c96fc8127cf13a62e341546d0e33ffc6487a2d73623bba1d94c06326f1c3`  
		Last Modified: Mon, 20 Apr 2026 23:01:36 GMT  
		Size: 82.9 MB (82860856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33475f37e3f83a07cd01d957666e351be2340dc48eb31201ef97999c3a1aefaa`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:72f9b141756df474c234b4b675ad4d948bed8a7faa78fc15d82c70ee21202b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4beb1e608277e4c322525e16b08bb3c33d5459cc20f7a9d63040d627b0bdd27`

```dockerfile
```

-	Layers:
	-	`sha256:28f27aa5782d9baf2fa31f0b92fa98b22a918aa1bad41ab129608fdc4e651f0d`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 1.2 MB (1160977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd23b43aaf5b8f30b1880dc9a34d19226c9e036aab4086c52d67bf2e97f045d`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8b04ef3b191824da04c0b5874838b5821ada4a6d7b48afd86e3df6270a36db11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80731816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52511b9f42dc7b99e2458d4d1bbdafc8a021247811ad1d4c46941f8efe498987`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 20 Apr 2026 23:00:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 20 Apr 2026 23:00:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
ENV TELEGRAF_VERSION=1.38.3
# Mon, 20 Apr 2026 23:00:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 20 Apr 2026 23:00:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:00:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2026 23:00:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9b733d983622224ecddbe820bed2cb7e904ed583c6326d1fcbda67959fbc01`  
		Last Modified: Mon, 20 Apr 2026 23:01:08 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f7df98aba8c78e2e29b3b228c032880b5e8acf2e6e1cf0bed0f6363b715335`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 2.7 MB (2663564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b5d3fbd32d64ada75fc47549619be9adf0a668037fe436c3d7c3de355d6493`  
		Last Modified: Mon, 20 Apr 2026 23:01:08 GMT  
		Size: 73.9 MB (73867483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9409057d942df5ffc8f8e16a5abcc46365c47c48f909fe2ae426cdbac197930a`  
		Last Modified: Mon, 20 Apr 2026 23:01:06 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:ec76870da5c01f53a2e038528dbebb056788db16195c62c9ae5103e3b9c0510a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c287ee0afb47dc691b031e966daab08c1affe814f449dda4ed648a6b4612f6e5`

```dockerfile
```

-	Layers:
	-	`sha256:4ff1462719c9ec6f85248c19a687f2a0602683d711a5dddc76daf068ff84395e`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 1.2 MB (1155966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfcaf9bb18b8737ae93288d4b086fec056bf86622b17b184faf48cf3120545f`  
		Last Modified: Mon, 20 Apr 2026 23:01:07 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json
