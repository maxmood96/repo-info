## `influxdb:latest`

```console
$ docker pull influxdb@sha256:13579a335363aa9721985087af25afcaf71fbb566dd0d758078f27e0ad9057a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:320b09dd9fdf88d3e5e279b1117f854c7680d62489a442ff6a19ce56f6555972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a087752ab8a7ad3b11ce82767c68fe6ce8046ff3d5e3cf276889384715aed8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8170e6c8b5b3ea069bc5fc36a8cd2a73786660643fd6f6d86dd017355cffc`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 9.6 MB (9592091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7975cebe753fece4b01d83191733754cc672e30a5ab432e947ed06be8d34bc5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 5.8 MB (5820923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a7d512a02b1ad2aeaf4f331f37237a0c688ce3bf238ed32626a3385c8a659`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323fd3a42118e489eb04f0cb4e66140e9b77738c5d09169009e2e37ca63ff5f8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8258065e79d1ce73e35fd7b1e72ae73037cb757ed6be1e69847e3bc5745de2df`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 95.3 MB (95255503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a65d57478ce8fc72fc34a67910e1e50c64693e72c564b31e7a821c9d18acd6`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 23.1 MB (23128319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394fbb7bd6706dc09b4b01478313c007b0d5e05fc639d1badb052f5b0183194`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27e810bf29cf774ea3693f137c338f48a55fcd9b0b4fea5e1d2caf58e236bf`  
		Last Modified: Thu, 13 Jun 2024 18:28:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d5888dc1284a2aa4bce210dbf8af2e970f75ccd7c973e418acbb28515c1b98`  
		Last Modified: Thu, 13 Jun 2024 18:28:54 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:20424bf712d71c63b9f7544a480fdd2a517e38857ea60b4a6670e57df14df869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f234781a8ff2d1edf9144f0b45a9c506f5b1673984c7a04c61eaddf56677ba`

```dockerfile
```

-	Layers:
	-	`sha256:d12f468f75c562ece4a7df52ba540696d1bdb860670d38bb74613e32d0cd12d5`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 2.8 MB (2755162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081106b445bdecce52ce39df7f878ccbec04062065d2a592f85046859107c9a8`  
		Last Modified: Thu, 13 Jun 2024 18:28:52 GMT  
		Size: 33.5 KB (33540 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d9ccf4d36f36102c1a38d7f385c4b33a14cc69ba4f3c64af0d3f542289e98dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54ea7920d13b97b3ecf7f351e9cc4361e0147736f2ffb8b2e5a00420355e4ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 06 Jun 2024 16:24:41 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["bash"]
# Thu, 06 Jun 2024 16:24:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV GOSU_VER=1.16
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 06 Jun 2024 16:24:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 06 Jun 2024 16:24:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 06 Jun 2024 16:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Jun 2024 16:24:41 GMT
CMD ["influxd"]
# Thu, 06 Jun 2024 16:24:41 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 06 Jun 2024 16:24:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 06 Jun 2024 16:24:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1ea3b6373448936e739ee0f0ebf73ae303d4231eb55cae9758d1a3cf05951`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 9.4 MB (9388817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a0c4887383b15b407aefefafee7aa3f7d365458d3b6a596f2b61bd6da0db4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf59e453e7b5c98871fbf3cd2d0223f337134760424ba431e324474daff757`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa93a5d874d074948e80d205b4e508c417624943bb88e2e35fb65f92fd90b4`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9bec4fc4e59e2023689d18549ae2ef013ff5dab335528a5f48b698684b96bd`  
		Last Modified: Thu, 13 Jun 2024 19:06:35 GMT  
		Size: 91.5 MB (91453318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1efac592486882b6e74f4f28ce817ef11ec79b5f5b77adbb8fbfad52489e7`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 21.7 MB (21662521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b72ce02738a13a6b5efb59a8a98b3755bf73f55c2147fa3f43edfdcfd6c5b3`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc8a55c0ea84af9576af5a680bc47bae003061c547f72548f711d1a1426471`  
		Last Modified: Thu, 13 Jun 2024 19:06:32 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4e70be6e23adc337e9ce6111f51ec49d07c0b7014c49918e347457e998cd6c`  
		Last Modified: Thu, 13 Jun 2024 19:06:33 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:1cad6a2c3e6e18cf7dede6ddfa98559a36133aab9a40a04084d2ca6d2c182f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6c7da3f669d816be0bb1c6c8ae4c83b0d9d32b619216330fbb1b1f4c38af5`

```dockerfile
```

-	Layers:
	-	`sha256:3ffff0605b518572f1ad5dd2a1b9da5eb66d86cbeaf8b8bd19f7fff86c74f02f`  
		Last Modified: Thu, 13 Jun 2024 19:06:31 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5414cc3be457867e9ab93f1555fce2d2a1971d42bb48c5846e7cdf1e1149907`  
		Last Modified: Thu, 13 Jun 2024 19:06:30 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
