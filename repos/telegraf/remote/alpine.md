## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:ef81917ebf37c5e115aa9850acfe6e259cd930a52d9ab631369860f5ad5f714a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:a6d691e966af30894110ca0c541de511c5673b1cea36531539efd075371dad5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84702775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f994615c47582f57294a82c6e40c34ecea33872a4a6bbe47ecda10ef51f28d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441bfd7cbe6dcce1d3a679483905055d08ac53a62c4b46f7400e56b6033c9fe1`  
		Last Modified: Mon, 28 Jul 2025 20:40:02 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61074257c6ed478d2d729dd4dbb47516bc6c05ae4aaa0a04c6a3760a44dbf9dd`  
		Last Modified: Mon, 28 Jul 2025 20:40:03 GMT  
		Size: 2.6 MB (2552151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e736009a88223d0f0a222e07fd4258d31efc4501ef0908c5913528d7c6d1b74`  
		Last Modified: Mon, 28 Jul 2025 20:40:07 GMT  
		Size: 78.4 MB (78350036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efff3a00ac272dc1ba9246539f23fb935a05ea610519bf545ac53ebb641ed40`  
		Last Modified: Mon, 28 Jul 2025 20:40:02 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8180485c3053244cf019026be34b55ef471f76d951ea3848a556e4c77fd7d26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1146874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ac32bf4bbdfe9dd36a984077c3aaa1b1a3996f894c989113cff87cc2595835`

```dockerfile
```

-	Layers:
	-	`sha256:97e004a361da778aa37b4a3cf769dfaf18eea20a989ee4881806bd6da90237a4`  
		Last Modified: Mon, 28 Jul 2025 21:10:34 GMT  
		Size: 1.1 MB (1131611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c5b7c0959010e9a80cb17b1a324f0e072bf2830d9a94d74f694bcdf97e6f136`  
		Last Modified: Mon, 28 Jul 2025 21:10:35 GMT  
		Size: 15.3 KB (15263 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:beeb9a84badaee837038459bc3704b40bd7c7ca7e0549ed46536c3baac5ffd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77773286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647f62df4ae4764d5521c03f468d882504f8ba21e446a90c9dddf3523ad15d78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENV TELEGRAF_VERSION=1.35.3
# Mon, 28 Jul 2025 18:45:03 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 28 Jul 2025 18:45:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Jul 2025 18:45:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Jul 2025 18:45:03 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b1f86b4ba4441253e81263e61cb7f6f39394b74b0581bb5e17c44991e92d47`  
		Last Modified: Mon, 28 Jul 2025 21:02:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a4824ddd6c41e298e5d586333adbb184c26b05b1ab9c1a4634f3201984f82`  
		Last Modified: Mon, 28 Jul 2025 21:02:44 GMT  
		Size: 2.6 MB (2616106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78acedd717276dc34c4db9cd0bca200c6e7d1b09113bbcea9701b87c2c80d90e`  
		Last Modified: Mon, 28 Jul 2025 21:02:58 GMT  
		Size: 71.0 MB (71025532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f530a71952f68dd125e267b32fe83d1a3cf0b84804a3e2c732d979b8d3ff76`  
		Last Modified: Mon, 28 Jul 2025 21:02:43 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d1e66627b765593009da0e1edcf5ce02c9f08a36204e5c2d5faa9a9e9f030dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1142635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1826a2c722e7ec911dc76c2fe2a2151f317a92825e69ff411129c279ca35d79e`

```dockerfile
```

-	Layers:
	-	`sha256:4c9bba698c7676088571f6e1a62024585a0e6c02e55c656d4736299d8b1f3128`  
		Last Modified: Mon, 28 Jul 2025 21:10:39 GMT  
		Size: 1.1 MB (1127250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446732bee9b46b11f5aaecad242187051df8c0d5027d5b0f987fe99aadd5e27c`  
		Last Modified: Mon, 28 Jul 2025 21:10:39 GMT  
		Size: 15.4 KB (15385 bytes)  
		MIME: application/vnd.in-toto+json
