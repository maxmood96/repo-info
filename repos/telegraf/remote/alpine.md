## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:b6a7ad2cb069e9d1517cf15a891f6f97e7c7d9490c26dea988579ec970fa1a0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:56afc6f08c2533886c59d0eaf48f7cac46b4033c184f679f6e7320dd436544b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78895357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4403577c5afdca639d437c201a9aef292a5c8933ac4d890ba63c10b4e4d33f75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENV TELEGRAF_VERSION=1.33.0
# Mon, 09 Dec 2024 21:08:54 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 09 Dec 2024 21:08:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Dec 2024 21:08:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 21:08:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946b3ae4514a58a37deccd6f84334267981743132330e6969cde8ba7d51511e`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d223af490ee78c955b2175e1febe79c8cd6081622ce206ed5c8ffb586e54a`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 2.4 MB (2444832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c5a91a122385f5fad17011d530eb32627133b82b9397a561f515f3db6f5483`  
		Last Modified: Tue, 10 Dec 2024 01:29:13 GMT  
		Size: 72.8 MB (72826013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6824f28cce7261bf9b8fc7fcbe15409b8d00440edc41b67fd641af40d213f112`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:2883f62bcc05b5fb1fb8d695b8ea9f4cfc3d8c57b0f5651156f0c2535cdeb318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1099566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096aa8c212da9dbf8160d81904149a293cd310ee73bc195696f9c926acdd5f5a`

```dockerfile
```

-	Layers:
	-	`sha256:8bdf0771a78b5d9029133efb52d2404092cc534da014190eed53c59a7154085c`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 1.1 MB (1084303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1cd315410a7184b1a5f15718af4ba6c614d910bad4091474080465a1498c2a9`  
		Last Modified: Tue, 10 Dec 2024 01:29:12 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8c583f2ca801c3c4e1d85d418904406884f11a8faf69abff30fcb998be6ae7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69563728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a3b7bca19af75445ee828d6ae44a4aca6001ccfbc285e03a0bb04d3c59c691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENV TELEGRAF_VERSION=1.32.3
# Mon, 18 Nov 2024 20:48:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 18 Nov 2024 20:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 20:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 20:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2136f9e7feb99945e2787587daa3284c73e45adf2e22f99ad169fe2df7417c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261692eb4698b8fef35728a5f463bc73da3690cc00050ff8eae9c2e6b6f2056c`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 2.5 MB (2530622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c097c44c7b51c633d2ea3c42c293141f0aebe80769accd240ba2787ecffc3221`  
		Last Modified: Mon, 18 Nov 2024 23:53:12 GMT  
		Size: 62.9 MB (62944775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cacd0e5e7d2ccf9cf75159eb73e57bd71b2d79b7099539c28a3e36b072c5b7d`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c85b59700690d98745cb96f176ac655994b903886cfa983cccbd3eff660a8254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1085315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680778e461d1fab783a7e89f344f6d64cda902be5c72231d3124ae143f05dc76`

```dockerfile
```

-	Layers:
	-	`sha256:61652ab748fb8c98a72a67271f2195ea9bfe2fbdcb40aefb9c49c77d57f46c33`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 1.1 MB (1069930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec49b11d7c57d08dc2c42d71b46d3a5df4d2f3c151e691be742b9ffbc606c06`  
		Last Modified: Mon, 18 Nov 2024 23:53:10 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json
