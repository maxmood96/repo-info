## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:a210c27936248e77d1646bd9e2e14c3c05fbc9c7c1f70768f76f866e24fd6bdb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:980de6c467cf58935b54df248930259c47771cec6d3580e4c899fce364186f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92011663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8369e23002583137c2fd7b5d9100ef3f597613b8d44a9652ad63b159df4309`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 11 Jul 2024 20:47:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0dc81762ab9cd4ef11ab0791cc1e4b892353c5ad16f3506e394ed6f4851e93`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f18cef9a6cf8c8b1886e10d167cf6ab545b58cf2b96ccbfd151486bebdc7e6`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 9.6 MB (9633256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c65a22e031fff63369e94994f8c1bf122ea9e4710a99745ba002d3668f2e53`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 5.8 MB (5820927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e14a2477df6c25c76b13f5009de5ceb13143a8cdae2647b3fda7d73cbe737`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc70ac1afb69874bc1da494b05e87a8b12713f12f637f0e28838a57debc79be`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 49.8 MB (49798314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff79ccb638859c2f93bc6b478d404485f0132770e580fd7c8d8a7fb8bfbe4b59`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 23.1 MB (23128309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d98ec689fb5fab393c0e5c79138f617fa94d1c90e1ad0282abca6621c24675`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ea18c19e317393625c2c2939b3521fbc7ebba56bcb67cb68c068178955be7`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be8260682ef0a7adf8bd76b1950e012e93251862938923b508d7233a4dda1e`  
		Last Modified: Mon, 22 Jul 2024 23:05:38 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:b54de15363255b99d02d523b11514f1fe6f0e3a5f2bb67f22630ffa114929e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ac085702ffdda597a0b0cd8a1d8a890d7be317e1ae9d80df00320ec263ccda`

```dockerfile
```

-	Layers:
	-	`sha256:ab6f2b1e7c2aaa25faf3c871425e0419810e6a848cf15112dd95d05367dc0af7`  
		Last Modified: Mon, 22 Jul 2024 23:05:37 GMT  
		Size: 914.1 KB (914097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db21d24731eed915a390cb46f22fcd094da7250ff07e8b773a1668085beebb1`  
		Last Modified: Mon, 22 Jul 2024 23:05:36 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:450e152aa5087036710ff4f22f9e50f246f38e163260b218604f31ece446b625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88700622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60331e48743fd295013bcde9d8415219874150a88a3b2391288902e5525dccd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXDB_VERSION=2.7.7
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 11 Jul 2024 20:47:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jul 2024 20:47:57 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jul 2024 20:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 20:47:57 GMT
CMD ["influxd"]
# Thu, 11 Jul 2024 20:47:57 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jul 2024 20:47:57 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jul 2024 20:47:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966ee58330d4838baa8b7f3790f1657e653c93e6af13f44a3a9e7ad5cab0aec`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c6a8887d050280cf2c7951a2c06d0a779601e7c24bbf367503decb0147188`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 9.8 MB (9760271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8dc45b737a429d43d9159b709779ab55cb50ce09059ddce29740841968d08b`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd3be33b2bcb4be0b1f745245347519b3af5ed664588610d6702a68467d4e6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ecd7b8bdd121b8e849c8a91e540c1afa835c3e4337da8b50dc91ab94018984`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 47.7 MB (47717265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e84a4ac3529aa6dd255e308ba9df3c09f4f0edb9a2e47b71eaaa8a5fd3549`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 21.7 MB (21662512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd5d15bf6a575f4472da34ad84e79ef39f7f527772f85acd96f7f824fe1fb40`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45250427d97aa0c820a41df90d98dc88c7f5becc7ca4c40da12ff26b9e6443df`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8259f1217c391e86ec6f5ea2b73cd8e7ca976f7dc3dfc5eb34ab41035d26ae6a`  
		Last Modified: Fri, 12 Jul 2024 00:59:52 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e133ec2fa0631cf8507bff16aecbd91c2dd6a2228452dd3586be5b470560a691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **900.8 KB (900788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d65cd96be187154def8dbc5f6759e7ce1ede0e23b85a6c416eaa6dd87b61a6a`

```dockerfile
```

-	Layers:
	-	`sha256:5c350da9e39aa184aaf4fb6ca36e515a98e5431217bbe1833d6a1fcbac4cbdf3`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 869.7 KB (869741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc93909d32c197cd0366637e383af1f40f2a2e9ae0224531f36db1a289e4b7e`  
		Last Modified: Fri, 12 Jul 2024 00:59:50 GMT  
		Size: 31.0 KB (31047 bytes)  
		MIME: application/vnd.in-toto+json
