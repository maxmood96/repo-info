## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:6fbb8ff2f014b783ed35d098aac3428448c81f470cbe5fb556719ace943cfa79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:b4aae23172008e162b9a084342cdca5d1452ae4a059304da6a6fabd59f76af22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92813970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b3e3f8000016363e0a784f8edcbf98dc4aa46b9bd27ebdeca576ffecece05d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92ac7301eb1d8a431d21e649728ac813a9810b06306e0816d682ad0be9ca0c`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c097ac5959ac8b7e5ce7e4625284fdc002f278072a8a534bbdea3ecd50e54c`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 9.7 MB (9664086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb104e3f0244f28d748ea2d7e74df268bfc91d976a040efdd8b6472e202934`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 5.8 MB (5820946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa6391ecf05bcbe8b467dbf27ab8a43f13cc250042561a1d506468cb0d2b38`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab10afa0a468cd5771fd77f7f5063bdb5ad4ac335858959ab0bdf509b5ee136f`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 50.1 MB (50148313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33662d6cd32b83879dfbf57d88bbfcc6d967f3f0474808141c15bd937c018575`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 23.5 MB (23546400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c327bb004d758bbb8c21ea739fe8e4121de1461e28a6991b2d79db665075a004`  
		Last Modified: Wed, 08 Jan 2025 18:12:08 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfda2b82a1866dcc3572daf050a9248464dc689cc9594f1322c28270c497df24`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ee9c3c3ab82c14c13a9355fe8cf4ce6147fb8f665e4d2403e6ec4d55430a70`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e64aa7820f3f75bfb9893c5c68463c206f04d425e64680274067fe3e3453b99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **948.2 KB (948152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101b1bdaf1a4935098a15031b753e4b76bf5700056850d7f9236ecc66b9ddae4`

```dockerfile
```

-	Layers:
	-	`sha256:23cbff2765458f31b583563fa71b23e8c50895a61da97a761de9b33301d22c7d`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 917.2 KB (917204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd3e60aa959b21ee324b6538f5b8a26f77d2fd9e22616fdd3c5271bfccbfc42`  
		Last Modified: Wed, 08 Jan 2025 18:12:07 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:381be70cf44e73d9e0bc55f8d0cac1f5a08f4c9869dfbbeb2495d227ae98d0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89599718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76114aa77360041ce959a4d707e27c03f02956315bf52b5682e2158368002a88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 02 Dec 2024 19:42:18 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXDB_VERSION=2.7.11
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 02 Dec 2024 19:42:18 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 02 Dec 2024 19:42:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Dec 2024 19:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Dec 2024 19:42:18 GMT
CMD ["influxd"]
# Mon, 02 Dec 2024 19:42:18 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 02 Dec 2024 19:42:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 02 Dec 2024 19:42:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce83109ec04193e8d1d95cc284000b3744402e6eb3a74774afb3a1dfca37714`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72ae5757088c40ba9252bc398341fd4347da11535780149b3b39104b7d2d2c4`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 9.8 MB (9769732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a0cb131d8295a6731b94e1af752bc44934519b9a440c2a25c516b0a53e121`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef225f1667c91e1c16b29bd860d533e6129d22ddb50151ed69e586ef708d62e9`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2039b5d949f249c870175a599013329b1e6f0631b518c33316e28879fa00b8`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 48.1 MB (48073590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee1236d68432abfbe0e2c1f5421adb5f913cf0c6e86728e51ee487789ab7c09`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a06dab86f6432e6f1830e226513c20fc301cfa593a32cd353fa027bbc15ee9`  
		Last Modified: Tue, 07 Jan 2025 08:37:57 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b9ac155e359247d7cb1f67b3a262378c152bb564e6b81de1a995578ceaed84`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d50c5fc2e43e90151e4bb9904c2501e53b67eb5fc11135d275874c918081cf`  
		Last Modified: Tue, 07 Jan 2025 08:37:58 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:ba339f2c08a3f1e9f61705b928b793f687fc093875cb670f7b7a03435d26ad64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.7 KB (941719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e02475e9d5775a128692deb8c2d0eabcd35a7c1103dc2929ff31ff6dd1f5685`

```dockerfile
```

-	Layers:
	-	`sha256:a9629ee45cb1140ccd226502c5b6b76a3f67eb352e1f5f21d76b1f64b62249af`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 910.6 KB (910577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0008f6fc76aac14445ccc58ad2278bd6eb76709c39adffe8df99f443d4092d41`  
		Last Modified: Tue, 07 Jan 2025 08:37:56 GMT  
		Size: 31.1 KB (31142 bytes)  
		MIME: application/vnd.in-toto+json
