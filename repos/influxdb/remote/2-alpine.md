## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:aa7c7967db6299829f225c931edbe2e53cb74bc32d8a8689eb10a71ec0cc4f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9df149c10d324879963a5a690c3b3ba71bdea5208d5cb595d5aa083314438e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92302723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197b9f7cf87e0c89204d30b0327432a13a7d21e94eaaebad1208953a34be32b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d45a0a4871208edeaf34244b70f2d47191b76f2b4997648bacee65f0bb9b50f`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee199347147ba36a9ac1c8db22d05c1c0b79ce7413994e38d8195544577dbca`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 9.6 MB (9640728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa969dbbaaa21fef569a8823d550f3eb33e6b24d275e9c20b68b15cf0c605015`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8142b4768fda9be2ced3e3eca82355fe675152715254e0baecfbbe1d80f5236`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380d583d17bced46b979236bdba753d5f94fa5a1fcadce3e45283a7d08918db2`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 50.1 MB (50081865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5e1ae40d1867d5fe7a6e65a7cc6488a475e6f73a97b2a4da6f8578ad3c21c`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 23.1 MB (23128318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c693aab95480f71f592cc525cc940a6432037406963ee4ac5ad6035bd262167a`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a68978ad7a69b0b85802e8367847c0ece31edd4e193283c0c40774fdbe43001`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d385c3278fe6011ecc879151ad7f9bc7ba4a811b3c443d3b80afd979ee26eee`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:097e3065499d4cc13248203886f2943f82a6e3a0ab2ab07cf9378e18831f7e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab074677763b44aaf3b7d3bcacc8bd61e7fdb67dfab0e15c66f6ffa9c557a2e`

```dockerfile
```

-	Layers:
	-	`sha256:0a9cbd4c122519853b11796e1db3443af625b2b65b4199f595f63057b1cd5175`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 914.1 KB (914097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ecdfd8c6d37eac63328f874fbb9ad15ce00adce6366792a1af4c8fc13ade0a`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 30.7 KB (30746 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:38069e07791802e3ae859b88d3ed24ae39bd47c0c262fadcaa5a19b6cc695307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88982239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170537657cff123e5c869bab2bb7ea295cdc9d87b7ed152fa3a22dfc1fc381a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1de5eaf2a1972853375a025a0309628552446763159c73f9fb971eedad7e97c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42d817c706fa63528ebb9df4f22670ee67a5c112ac51b215bd8678ac9d67ad`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 9.8 MB (9763425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62906ecb281c2a5bc707f62ab2b4c4d4b2a03aa7f72fa2a50690041ee145d0a6`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 5.5 MB (5463800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061f6bfbb64e47b965b683ae90ab51edf297759c77aaed222b5fe725bcbf12c`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ddf646868bea20fb9c33985e55a3399b91f7542506e04b9dbf75d1f577751c`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 48.0 MB (47997597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4e2b2b9f546f5ee7181d8d42ca929bc02f55aa86d66ceb9ad510107149aa0`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf7866d6e2a92bb62169de5a27f2d1e5ff074c3fa58197a2a8b0c3f5e3795a`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e860d28620195865eda75ca3b59e127cdfc148e6f2f569d8bed47d4f0d03d1`  
		Last Modified: Fri, 26 Jul 2024 00:21:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9275442b1367a934d6ac0672ae7677e98ccf3c367a779f1bc30d26421ee6bbfc`  
		Last Modified: Fri, 26 Jul 2024 00:21:11 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ef8e5056db345477948ce7481141622023935805a47ae0134cbf533b0e803dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2454014d973cf1c51ebd53b433151b51881c4affe5d5939ce894b2d0cd644705`

```dockerfile
```

-	Layers:
	-	`sha256:e3a5515ff59a3c4f7db137d7f91ed80d45620c9b4aca52f8dba2028f051a7610`  
		Last Modified: Fri, 26 Jul 2024 00:21:09 GMT  
		Size: 913.4 KB (913358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5480a638871ea5968968e63a134f3227aff5394e81061cfdad6ca533566a75aa`  
		Last Modified: Fri, 26 Jul 2024 00:21:08 GMT  
		Size: 31.0 KB (31046 bytes)  
		MIME: application/vnd.in-toto+json
