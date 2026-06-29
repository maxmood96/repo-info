## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:4ab2541742661448a279287f41e3660e528b2083a7a46cccdf559a3094b8fd8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:57332205f6585766cb89a5bdef225c0f3ed2b21978b2a84a98253ec92f6b396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90752352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f4bd85179846b2017929654e1dcbf125adf4eddd48dec97db0689f08a4f71c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 20:50:33 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Jun 2026 20:50:34 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Jun 2026 20:50:40 GMT
ENV TELEGRAF_VERSION=1.39.1
# Mon, 29 Jun 2026 20:50:40 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Jun 2026 20:50:40 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Jun 2026 20:50:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Jun 2026 20:50:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2026 20:50:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578919e246e1ce8850b88e157c9b1e425a63c45e8a4419580c14f6b0789c6fcc`  
		Last Modified: Mon, 29 Jun 2026 20:50:55 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f023cf1d26c3a3212f3e328f697f6520492c833cb88aad74ee3e1a5db98e2c6`  
		Last Modified: Mon, 29 Jun 2026 20:50:55 GMT  
		Size: 2.6 MB (2568182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758d7a941c12529e184c9b776d50de028d681e1b0c449ea76f620cc1d1af5947`  
		Last Modified: Mon, 29 Jun 2026 20:50:58 GMT  
		Size: 84.3 MB (84338849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b767314499da405da4d32aa091df7022b47b92daf6138f9cc548336717e351d5`  
		Last Modified: Mon, 29 Jun 2026 20:50:55 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e8167b2cd9f313ebcf56b7059b3042a64862391862450d9187d3b64a9c591deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb30f06e6463b5b6bb3d71ec07e2a905c9dbc66820eca35bd9ff85d9f8215d5`

```dockerfile
```

-	Layers:
	-	`sha256:dfc880e0ea012f031e840dbd9b1a6c4eec72a233c4cada60bb8ca1813a1382c7`  
		Last Modified: Mon, 29 Jun 2026 20:50:55 GMT  
		Size: 1.2 MB (1153787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:511395aec5586a97ae46f49158af5554efc75700b5ae445a48862204c95d4329`  
		Last Modified: Mon, 29 Jun 2026 20:50:55 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:929b6200645052dde3b27700e6cdb5d5e7546e7f1634bbc1f7f1933ba6d09eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82080093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbffc0f704f613c3a28a9d603b33399d5243d377b1f95814645c26991206507a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 20:50:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Jun 2026 20:50:43 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Jun 2026 20:50:49 GMT
ENV TELEGRAF_VERSION=1.39.1
# Mon, 29 Jun 2026 20:50:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Jun 2026 20:50:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Jun 2026 20:50:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Jun 2026 20:50:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2026 20:50:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd1b0aac0dafe3bea90e300c781479fafc400dbcdb5688b9c867655a5cc7506`  
		Last Modified: Mon, 29 Jun 2026 20:51:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5e4f8be2e8ca407fc724357e2ad3091d0194d3f6a9d91cb017ef9112e3b101`  
		Last Modified: Mon, 29 Jun 2026 20:51:04 GMT  
		Size: 2.6 MB (2617136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ebc3c18f0035117f8c268ba511d7424a5ddca6c21eaf0d5355926600988c9a`  
		Last Modified: Mon, 29 Jun 2026 20:51:06 GMT  
		Size: 75.3 MB (75280200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212b828e7194e70ddafbac715e571762b3596143d30c44dfae62c5733203531`  
		Last Modified: Mon, 29 Jun 2026 20:51:04 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:e670dba7aa43ce4d5149b3bd60f95e1d52f44c0c0c0130f9606b986501b0b6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5bae9c496c8949e7486fb1494e34a10eb37a675dd4cdf49c107f8bfbec3f1c`

```dockerfile
```

-	Layers:
	-	`sha256:63543dd7760e9c2a94c639b2bf62a5985f11fe3fd514810d86b13618b5e7da54`  
		Last Modified: Mon, 29 Jun 2026 20:51:04 GMT  
		Size: 1.1 MB (1148776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b4f8081cb6ca7f2d396bfa8838bd70463e254e8bb687233965f76fd285f7ee`  
		Last Modified: Mon, 29 Jun 2026 20:51:04 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json
