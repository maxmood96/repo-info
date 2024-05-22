## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:3f9361dbade7fa110267d348f1aececfd28d55e9305f08289af5da388294eb63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f80ac3a7e04b757fc00e8a7d6b26ce2728d28e898ae3252338a309de2a7e6f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68608895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd66701dcc20b0646e947b9cb8860354d4a9ebecf958bf27d6dbf31bd9edcdc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 14:13:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d56880179c0173282d206f8905f45fa9d36acc0bb3fd17168ef4ea8fed246`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccb57210f04899dea68eac0db2bfe1e7462c254532b30bccd598eb8db0d3a65`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 2.6 MB (2618977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcde6f107a71c5ce886bf1f798b0fe237f729959d2f2ffc695ed2acb37dbde9`  
		Last Modified: Tue, 21 May 2024 17:53:28 GMT  
		Size: 62.6 MB (62580582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6725ee7028bc5f73be376c1879645751daececa916b333638122ae8ead461943`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:baf1983df6f26904976174963303f8cd47ec991aa70a1c328170a032032f91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1380934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d513343256a4bf1a6fb223bb127b915f5a8572df2df409ea8d9a2a2ad1eb3a`

```dockerfile
```

-	Layers:
	-	`sha256:c3ab684a0d57fb67f3896e010202d8f63a500d282fff70f2feab93135d7ab493`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 1.4 MB (1365782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfc7badb303d89ccd18de8de652b66c25f05f90e39c4337c8b00d9e94248691`  
		Last Modified: Tue, 21 May 2024 17:53:27 GMT  
		Size: 15.2 KB (15152 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:33c1a2cb6de73e279f2888dbfb9c2ab4d591ba512ed3b0c632943a3f293278d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62998531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f947f38465eaafcd3d85c85c55fdd97d65ff67cb124b935eabf51d4c80936d29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 14:13:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENV TELEGRAF_VERSION=1.30.3
# Tue, 21 May 2024 14:13:49 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Tue, 21 May 2024 14:13:49 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 21 May 2024 14:13:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 21 May 2024 14:13:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 May 2024 14:13:49 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b0ae9590aac951e94f2baae1a59646b1132c3e10a981231c743a821f41d9ab`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dd9c7b1008b5ca36e326e19552f59e8b410f609610a513c42712f471376e67`  
		Last Modified: Tue, 21 May 2024 20:01:36 GMT  
		Size: 2.7 MB (2702921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab3c82d9de8f26a41d48d18ba5c0e58b1c3c15ff6908f34e89a2fd53193718`  
		Last Modified: Tue, 21 May 2024 20:01:38 GMT  
		Size: 56.9 MB (56947288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83051d2d208b78832edbd8f3b86ccb69839f624c116289700a5b26a4da435127`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4ae630baa163ce0b8744d1bb6856fbed9b79c20ce53811cbd4b2c50bbb2b1bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1376339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48b6b7fc3662b331b9a7dc7cc18b73fcd03fd2689df5a672b9a0421e974fb26`

```dockerfile
```

-	Layers:
	-	`sha256:fb8c35c943dd6d3722715d167caa72fb6bdb338ad405085b693be64bd3c46a40`  
		Last Modified: Tue, 21 May 2024 20:01:36 GMT  
		Size: 1.4 MB (1361344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d79f11691deb44318e4551d0b381fbad6d42458e7f5f4ede4cb6c115cadfb81`  
		Last Modified: Tue, 21 May 2024 20:01:35 GMT  
		Size: 15.0 KB (14995 bytes)  
		MIME: application/vnd.in-toto+json
