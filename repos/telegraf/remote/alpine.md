## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:52cb0c43b753b93245739035a62f6bf15159cfbf58de636cb82310554a951da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:92958ccc0fcd323ab29288eb697b72f2b776baf2eac48485faf684f99aba0099
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66507378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2fe9360c5a7de1455d44c17fffc13a143f8b3f7b045a5c5a60e3c23e6413a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 20:24:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 11 Dec 2023 20:24:48 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 08 Jan 2024 22:20:30 GMT
ENV TELEGRAF_VERSION=1.29.2
# Mon, 08 Jan 2024 22:20:37 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 08 Jan 2024 22:20:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 08 Jan 2024 22:20:37 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 08 Jan 2024 22:20:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jan 2024 22:20:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a0a804738aec5dc0fcb4fd199dcec31ce20ba35442c1faf7dabd1365e5a224`  
		Last Modified: Mon, 11 Dec 2023 20:26:02 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae898eca22470e7dd671dcd09308fe50994c32849751def459aff8c21d37515`  
		Last Modified: Mon, 11 Dec 2023 20:26:03 GMT  
		Size: 2.6 MB (2612141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1d1c51e586c61c6847fd03bcad3ff48effa73eb0118b7c4834ba4e6e5304fd`  
		Last Modified: Mon, 08 Jan 2024 22:21:30 GMT  
		Size: 60.5 MB (60486152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694db2bcef8e97354787362bf8849ac3fe0513045652eb802b8528d1f74833d4`  
		Last Modified: Mon, 08 Jan 2024 22:21:16 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:da0a767e2566e846fa68cbdf2b1438370b1073ebd9a4382c1f9ad0f75cb9f8d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60925375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457fdeee8e6374c9f7a0805a3a58d4b3cf4b4d0d62eb0bbcf4a7df3dfc9be729`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Mon, 11 Dec 2023 20:07:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 11 Dec 2023 20:07:21 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 08 Jan 2024 22:13:19 GMT
ENV TELEGRAF_VERSION=1.29.2
# Mon, 08 Jan 2024 22:13:28 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 08 Jan 2024 22:13:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 08 Jan 2024 22:13:29 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 08 Jan 2024 22:13:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Jan 2024 22:13:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f827e8bf907751a3e5b3169f3913e7b67c70b21c02477454501cd2043be3c67b`  
		Last Modified: Mon, 11 Dec 2023 20:08:04 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e495f22bdfc73e46af702cdb849f85f47df776e5075848c4a6ad77b02ec00f34`  
		Last Modified: Mon, 11 Dec 2023 20:08:05 GMT  
		Size: 2.7 MB (2694865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19281e235cd34cb27407d1ab33b1807ab6b87b6efbf03eaa58a4c3f79bf4132a`  
		Last Modified: Mon, 08 Jan 2024 22:14:14 GMT  
		Size: 54.9 MB (54882116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5bc6fc7ebd812348686f4ae5a38911cd1c10500ea3027f8f5cf869e6f4b80c`  
		Last Modified: Mon, 08 Jan 2024 22:14:07 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
