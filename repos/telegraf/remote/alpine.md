## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:d39258b956e55d694e71c1931e851b7b1634048f3afe76474ad284109e0e69e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:e6110654779dffe3af93674173ab6ee65d98de67ba562583827498c83cd53fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72102360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690e3afff75e2915f456af71b4ef75228606e25dc91159fb154d1736d41e037c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026d2909cd521d5e52efb7fd369a9ad0fde515ce36e3e67ee6a5c4866a5b719`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686998f6bff2309f7498d422d6eba5a6c2e01c8f6aee776455d33d3f205a195`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 2.5 MB (2452606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a6d3006b5e4f58627b5b7abd8215164fde6b7f4956e8eb2bc358f1674cb28`  
		Last Modified: Mon, 01 Jul 2024 23:55:04 GMT  
		Size: 66.0 MB (66025305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad210721abc8e4b05979e6a3bb37039633ec7ed12e427c27306169fccd73973d`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:38bdf9eec17433a6514491e416d9f1a5486fb6316d156e5e7ebbdb2f04a38a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1007433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c85c73a22037ce20ce906665b70aa5e6fc880bb17cbbc40efbb1324eddda506`

```dockerfile
```

-	Layers:
	-	`sha256:53a3e95a49ad1a494a788bded03675776caadb3dec72aa6ac64e1b2c8308f33e`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 992.4 KB (992397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb7667d37c570b271319f05d4318ba936c80c6a958ae6d51a2eb199e61b2e59`  
		Last Modified: Mon, 01 Jul 2024 23:55:03 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4f1233944459215f7c7b3374f1e60a585af50d3738cc0d95eb54a60e9cd28ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65649250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c058664d0314985cc743c5e23605eb58d030b64b1d23b14c5228da8781cabf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["/bin/sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENV TELEGRAF_VERSION=1.31.0
# Mon, 10 Jun 2024 21:05:04 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 10 Jun 2024 21:05:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 10 Jun 2024 21:05:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jun 2024 21:05:04 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4d02fd6d451824a88c3da056c35af5ef536e8a634a98239ab90c650e0518e3`  
		Last Modified: Fri, 21 Jun 2024 05:12:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d4393617a41a89527ad46200950f81c7c7993bd950a78413ef7d03b012113`  
		Last Modified: Fri, 21 Jun 2024 07:01:17 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c049c93bb18ecfd2e4038ec248f1c54724ab954d9abb3fb4b1c6f919ad894c35`  
		Last Modified: Fri, 21 Jun 2024 07:02:25 GMT  
		Size: 59.0 MB (59020137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a21376323bf3755211bbbad2f03d5a2c4e633dffdee25251427c3316344992`  
		Last Modified: Fri, 21 Jun 2024 07:02:22 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:5e8aad1076c9e00e1944d5fa817289d7bb1d30bd5212bd1c09a9a44d7f8dbff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1003296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb32fe1022cc60f4eefad936aeda7da2996b2ceeddfd4cf172db84315565f55`

```dockerfile
```

-	Layers:
	-	`sha256:41745a7fa13c44c2bc34f51070e6df1487140c04b6db80fa6c06aacfdb047dac`  
		Last Modified: Fri, 21 Jun 2024 07:02:23 GMT  
		Size: 988.0 KB (987972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373261fcab240e364798582da667ac67257985292ae7d356280b55cf5fe93542`  
		Last Modified: Fri, 21 Jun 2024 07:02:22 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json
