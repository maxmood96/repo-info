## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:bf0c681f61c39bab65c7f279752811d8be56e0a9383ceb93d14d5d71f4dab446
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cea79a5632fbe1b775eb0b5e3981cf7db25bc9facdf9ab2ec664609f8ac493ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179e85bca4a5ed06987cd9cc98a88e84ea7f6c9f7595074fcb0b9c65bd5860cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc543c237aca646b092c4fdea01ab9b8bde787628b47abc72dbae1d179996a6`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98f63f2c15a2d76083a496a488478760a73dcf9e27005d98c677346ccb2254a`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 2.5 MB (2452615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ade9494bd1902c71aa690099ca31d39ac3cdd3d988805ff9b17827e25114`  
		Last Modified: Mon, 10 Jun 2024 22:32:59 GMT  
		Size: 64.9 MB (64891822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaea357ec378621b71776a323682e0f82ec65a54bef1706bf8994bf04dd2b35`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:031ef6a4e0c263cc2ab30eb3d97c55cb6e5aacf456ad1a72425c73cd4303f146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed53af325068dcf824b312cd823469fbe369e7023dff8289a05a60203b78c2d3`

```dockerfile
```

-	Layers:
	-	`sha256:2819af046f27e0e9300377570774c7c28ea5915bb7f0d6bceb87469ff75a91a6`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 991.1 KB (991068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940319c9ee8fdd4367be09932abf7350462a2daccbc076dff9f6f95f3479a6e1`  
		Last Modified: Mon, 10 Jun 2024 22:32:57 GMT  
		Size: 15.0 KB (15036 bytes)  
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
