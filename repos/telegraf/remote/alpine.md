## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:8ca038c7af92a0469bd607b576e6adbde702cb5f50152e6eb14d3fc9143884e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f20bddeae4c6286ed87081a75f7c06adc88a40a547bf003959466d4c0264bb92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62521015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e8de638799c6d831fb35bfa225b6685a5987ab5a9c84ac9e280610841b9e74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 29 Sep 2023 03:25:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Tue, 03 Oct 2023 04:04:59 GMT
ENV TELEGRAF_VERSION=1.28.2
# Tue, 03 Oct 2023 04:05:06 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Tue, 03 Oct 2023 04:05:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 03 Oct 2023 04:05:06 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Tue, 03 Oct 2023 04:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 04:05:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779175f54086809f96dd5b117ed71f84dd847e86676070c520eaf459fa4e08a`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bed7c31f3b636325ae9d66bf7b4a657d3d3d16af82ee3c8aa8630eecf1003f`  
		Last Modified: Fri, 29 Sep 2023 03:26:04 GMT  
		Size: 2.6 MB (2644955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb8a6b1db1472af7a0438d286231392f78125cca60ab75196855391da99a884`  
		Last Modified: Tue, 03 Oct 2023 04:05:54 GMT  
		Size: 56.5 MB (56473489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e0e504ec2264a2c0ce471f415acbf3a0dccb30a60e4ef49d6d5a2e81bf9645`  
		Last Modified: Tue, 03 Oct 2023 04:05:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fe6aa9019fe174cfc8479e4dce06f00d35326bd23ccdb1b0ba0d5217bd7af28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57166419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fd3f5f4f563ece2615691c0d60faa41764a97406f9ed3e5928d4954b66d737`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:04:12 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 29 Sep 2023 01:04:13 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Tue, 03 Oct 2023 04:18:29 GMT
ENV TELEGRAF_VERSION=1.28.2
# Tue, 03 Oct 2023 04:18:35 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Tue, 03 Oct 2023 04:18:36 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 03 Oct 2023 04:18:36 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Tue, 03 Oct 2023 04:18:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 04:18:36 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945e94244715004b6f7ade3a66bcfa884d346f67af67149978de9ea31611ad82`  
		Last Modified: Fri, 29 Sep 2023 01:04:49 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31faafc9cbbcf6166cae9f8862e13279369c0c173349801f90034c190be5bc3`  
		Last Modified: Fri, 29 Sep 2023 01:04:50 GMT  
		Size: 2.7 MB (2673148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1cd0a910d6fea341a8f1c57ff59b3897f69c9344101ecdc18b844b827a317c`  
		Last Modified: Tue, 03 Oct 2023 04:19:22 GMT  
		Size: 51.2 MB (51160833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e384f243d4d3bc129765d090f495f3c67d451104b20ae270ce0cc1a6d38484d`  
		Last Modified: Tue, 03 Oct 2023 04:19:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
