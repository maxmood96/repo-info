## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:c2f97b178be0d6da47934693aab5f12968d4c357067466b00750d7c883c7ca5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:b9f1dad8bfc6e2e0a071ec3708f69b608314a1638df1a27dbee6c8d9c201157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85721229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898bfc2837a825d9ca57c11162f841378cca6e17895db8ff8007425b40ae030`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111a65e71ad846fe6bc5cf5d9981577f402356a07fa8643556a52a493832248d`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cbaff1778259b3073527b025ae9ab08156e23a8b7f42fbbc0fafca178fc2a4`  
		Last Modified: Tue, 19 Aug 2025 16:43:11 GMT  
		Size: 2.6 MB (2552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e527cfac45a96a64d7cc6821810e5660eec3f9f105ee9595ff5d0ef9ce3889e5`  
		Last Modified: Tue, 19 Aug 2025 16:43:18 GMT  
		Size: 79.4 MB (79368534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fb22e4edb908e9c9db1946c3275c80eb50f1b6a4a0a263e2bcc780d2db6cb`  
		Last Modified: Tue, 19 Aug 2025 16:43:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d62ff060ab03e0e18dd18b68bef85d0e6253116947fe2889d8b0627c72be5d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00067d3ac59b152349cce2ee62d1d1fc80d424366cca0741b5130316ec1f36f0`

```dockerfile
```

-	Layers:
	-	`sha256:ae9d5119dea6d9d8dc370f0197b7815e7ea4eab7a50e3962df4ff7507b5ec15b`  
		Last Modified: Tue, 19 Aug 2025 18:10:39 GMT  
		Size: 1.1 MB (1131697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2678129d408de246508eace01dabc93d4762f22a4bce5468f32eb78e3c0d9cf4`  
		Last Modified: Tue, 19 Aug 2025 18:10:40 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:236e9d66b8103bd93e3872764468db2ac263c373b260498613a72d79b42e7f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78624875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f602f26ba2bca549d1b9b7ae0a9904b7bb21d6746ba5781c2e0a9a6e6aea23ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 19 Aug 2025 08:40:07 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 19 Aug 2025 08:40:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 08:40:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:40:07 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ba851c3cc6f6a60e1f54d90b4a3e0088e3e71c1361234db72c0e681312948`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4ac1b57267caa5ade49b9cf526c34877421ccf3ab657266741789a47db05a4`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 2.6 MB (2616107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6254a8553d06cd74dd83678e67660d16a33aafe7a727405a4a8950db4c073a8`  
		Last Modified: Tue, 19 Aug 2025 17:00:55 GMT  
		Size: 71.9 MB (71877119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcbf034e9f0cedd31ed4f69e865f928e913e9e964d333ea83a0e38eab973e42`  
		Last Modified: Tue, 19 Aug 2025 17:00:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c7e18faf8edc102ce2aed72cca6a6ede5f0e92daa3e47336568447b0b82b2a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f034d01f06a7ef20999ff7fac16427ff60c143a68c0c7cd7ce2d43a9eeeffd`

```dockerfile
```

-	Layers:
	-	`sha256:b879ba997169df517ba2e5569a8fcd1783cfdde33a4b2a993479bdf25aeac651`  
		Last Modified: Tue, 19 Aug 2025 18:10:44 GMT  
		Size: 1.1 MB (1127336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c8fbc4be53f9d0b83f8a5baee19ef6ea265b37202aba06848c4f081543b0b3`  
		Last Modified: Tue, 19 Aug 2025 18:10:45 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json
