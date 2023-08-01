## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:9eed265caf84780235c080edfd7bde73f419371e1cce7556e615bc733d1e009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f3ed6b37ad6ee55a4974c4d2fa860989ead536e0ce4e7e2b76254513b20774bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61081480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65b4600b2cc1cb69243f733d4adf3ac7488737ce5358a64d3fcb62d7e8fd93e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Tue, 01 Aug 2023 03:25:29 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Aug 2023 03:25:31 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Tue, 01 Aug 2023 03:25:31 GMT
ENV TELEGRAF_VERSION=1.27.3
# Tue, 01 Aug 2023 03:25:37 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Tue, 01 Aug 2023 03:25:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 01 Aug 2023 03:25:37 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Tue, 01 Aug 2023 03:25:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Aug 2023 03:25:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839306c3a032fc97cd54db5c24422f71f0c7a4782c9b299a9866cfc1639623ae`  
		Last Modified: Tue, 01 Aug 2023 03:26:23 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c490e07ab2c161cd23d2fb3711bab444203aca484c3798f0980303e90a6c4b`  
		Last Modified: Tue, 01 Aug 2023 03:26:23 GMT  
		Size: 2.6 MB (2643776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfe3cf099ede538fec92058fad7506c38a76613e08433aeadcd7b40cd7ef07a`  
		Last Modified: Tue, 01 Aug 2023 03:26:31 GMT  
		Size: 55.0 MB (55039216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6b62e0771b3c345a0ee02a2f26f55f1ab9238ba73e18fc4c3fd57fd539c620`  
		Last Modified: Tue, 01 Aug 2023 03:26:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fff23717ae96246e876840ec6c57ab9d94c7411eb2b2cc8bb540b35c45ca9aa2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55671404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6738a5181d9babc3c53ba62390b5c8801d2a1d9d459477ab80547d21fc9f6624`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Tue, 01 Aug 2023 03:31:33 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 01 Aug 2023 03:31:35 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Tue, 01 Aug 2023 03:31:35 GMT
ENV TELEGRAF_VERSION=1.27.3
# Tue, 01 Aug 2023 03:31:40 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Tue, 01 Aug 2023 03:31:41 GMT
EXPOSE 8092/udp 8094 8125/udp
# Tue, 01 Aug 2023 03:31:41 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Tue, 01 Aug 2023 03:31:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Aug 2023 03:31:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbcf83d62346eb5ad560e23001897f7bcf64d92c28073fe92f42cac41c4b289`  
		Last Modified: Tue, 01 Aug 2023 03:32:14 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235ef9514f479dd165bcca0cc8eeda8f3bf7d505e75aa03ef1760a02e1781242`  
		Last Modified: Tue, 01 Aug 2023 03:32:15 GMT  
		Size: 2.7 MB (2671177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7162b1019b2f945612f09fa0eb108ff123b443f2b8e9046dcf6e0212ed5532`  
		Last Modified: Tue, 01 Aug 2023 03:32:20 GMT  
		Size: 49.7 MB (49670370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96afc68d4a3459dec0a38caa3f163ca72d17754ceee83f7a0e0133de48e63930`  
		Last Modified: Tue, 01 Aug 2023 03:32:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
