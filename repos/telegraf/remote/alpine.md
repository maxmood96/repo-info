## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:ad364cf968e03e535da5d7862b7a9166b9a4ad2060212eb538944cf42eb1d3d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:9135d659bb330fc5958d2d5f6cb49f097f7aa4bd0ccf15765a7ad3a5e9d87dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70968917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6d9b40ffd3be9f391d78af6277cae1f42ace397007c6c60404a5f4cbceb3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 10 Jun 2024 21:05:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519e0b64014137e38d01158fb7fb21e423a93da332fd6b95b67ebbd67456db18`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c6387e3aceb95b9aa6f50902763954d64f353a43c87d05d4bec8c62f124d8`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 2.5 MB (2452624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c945a75e8792b1293770eac0ad804c8058d7334b3b64106df49f1b1b1e317bf2`  
		Last Modified: Thu, 20 Jun 2024 20:56:48 GMT  
		Size: 64.9 MB (64891840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fbde9f849ec344671f835e8c6989b67db89802c51566272f609dcdca3fe92a`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:9db694bd013b8a7a1c54e5d9355148ae5c0696975514a36bff458fd414a7b1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c5b485b76a473b4d05aded093e6d20d775fd50c855274cb2477ed798f73a99`

```dockerfile
```

-	Layers:
	-	`sha256:4d1b403a4aef78f375e034aa5179812f92ccdfc7173056daaa98da078a2990a9`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 991.1 KB (991069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95012819ef21cede26ace42a448c5d9b91240dbf5a6df58d02d40d9200362a41`  
		Last Modified: Thu, 20 Jun 2024 20:56:47 GMT  
		Size: 15.0 KB (15036 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a188fffc24ce43fb109c5a45c3ab58d5769b2463e04ca33d853cb8a7facaa8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65647168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635864417fe16787ee131f1638ad604d41e9baf2cc00cec7a24bc1a253364cd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
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
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae98a4ae3c1de8e7a286da32ecdb0266e175d5486f8c5e4d3022d080d8f905`  
		Last Modified: Fri, 07 Jun 2024 02:47:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93834036ee0adda2709e5be45d5fe77b4cb5790d5d3ceb392045a47cc615e28`  
		Last Modified: Tue, 11 Jun 2024 03:44:47 GMT  
		Size: 2.5 MB (2539706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e8867aba7abb97ac27ce75cea45b339025dc0b6608b46c31320e46e089bdd6`  
		Last Modified: Tue, 11 Jun 2024 03:47:06 GMT  
		Size: 59.0 MB (59020078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f290e7cb71287aca40b9fe4abce730593e3b0003f52ef5171abc35ed88a9bfca`  
		Last Modified: Tue, 11 Jun 2024 03:47:04 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:dafd9063fa63898f2d7d1201a25dfbdaeb2dc7fd1a8c1df5c9ce4ca4c60fa6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1003295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0438bdc71cea0b5f61036da05c5aeab2aed18d47a83809d21b7dc65e0bb25576`

```dockerfile
```

-	Layers:
	-	`sha256:c6ca588205b754231492f40f3c46495838edc2b44d6f28f4736c62abbab2677e`  
		Last Modified: Tue, 11 Jun 2024 03:47:04 GMT  
		Size: 988.0 KB (987971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c8d366cd17aab1893e05fa3f6d0b9f8027e6578c218a78b98937453b97b00ca`  
		Last Modified: Tue, 11 Jun 2024 03:47:04 GMT  
		Size: 15.3 KB (15324 bytes)  
		MIME: application/vnd.in-toto+json
