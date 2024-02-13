## `influxdb:latest`

```console
$ docker pull influxdb@sha256:24a503d8283c59bb741f77be3413c9068fc1dee6f5d9211d404ba90945f90e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:7d3ddaa15b316a038eff3d9cb632b1a9cf7d894dcd14e2cbff559b2a3f8d4a1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164678553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546676123e5d8466d266ec33fb4b1579cc58238862aa3d37e70a67c5e23161da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:21:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:21:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 13 Feb 2024 04:21:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Tue, 13 Feb 2024 04:21:05 GMT
ENV GOSU_VER=1.16
# Tue, 13 Feb 2024 04:21:07 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 13 Feb 2024 04:21:07 GMT
ENV INFLUXDB_VERSION=2.7.5
# Tue, 13 Feb 2024 04:21:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 13 Feb 2024 04:21:12 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 13 Feb 2024 04:21:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 13 Feb 2024 04:21:15 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 13 Feb 2024 04:21:15 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Feb 2024 04:21:15 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 13 Feb 2024 04:21:15 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Tue, 13 Feb 2024 04:21:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:21:16 GMT
CMD ["influxd"]
# Tue, 13 Feb 2024 04:21:16 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Feb 2024 04:21:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Feb 2024 04:21:16 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdfd97cf1da6c346a07342c682bcfc51c5fc10658b30c37e936daa90ab65a91`  
		Last Modified: Tue, 13 Feb 2024 04:23:24 GMT  
		Size: 9.8 MB (9784701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4a9addae614e5a65effd762fe63d058be52830284f99befa27b485bb39d77d`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 5.8 MB (5820925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2682f23af6c5af32faf625123e45692cd5f8046ce91c4bbd112cf45b1ba878f9`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 3.3 KB (3275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0d19c1b23c49c3c721b8970e51c0c6aeb36e56602f1379f9f3c7fdee619a65`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 1.0 MB (1006415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c18a467354ba9cdec6b0a5868a858779109bca36f654015fb30e93a157156b`  
		Last Modified: Tue, 13 Feb 2024 04:23:29 GMT  
		Size: 95.8 MB (95803971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa424e376698506b8c453c03617885b8abbade552aad4de5f42c5e7f5f691d2`  
		Last Modified: Tue, 13 Feb 2024 04:23:21 GMT  
		Size: 23.1 MB (23128356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00eaf16d113504247a89fa3e3a8a3312e3944a5e6d528a0ea57c6a01bcb512a`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bddb37abd6835e005b9654961995776b33d3a90f096c2b9dc9f599c07a1155`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4cdb66f197e98ed28ed50ab0bedfd1b2f0009ac1424cb991cb66919c4ff20f`  
		Last Modified: Tue, 13 Feb 2024 04:23:18 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:582e7df0fa5c4941c148e54e64be9f977b1b09d7d873edeb4dd0602abf21c306
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158896828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec5df16229a7e8f28f51b92c1bdac0988de08fc0cc85732ee5556249eb69b14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 10:19:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 10:19:29 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 13 Feb 2024 10:19:29 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Tue, 13 Feb 2024 10:19:29 GMT
ENV GOSU_VER=1.16
# Tue, 13 Feb 2024 10:19:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Tue, 13 Feb 2024 10:19:32 GMT
ENV INFLUXDB_VERSION=2.7.5
# Tue, 13 Feb 2024 10:19:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 13 Feb 2024 10:19:38 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 13 Feb 2024 10:19:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 13 Feb 2024 10:19:42 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 13 Feb 2024 10:19:42 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Feb 2024 10:19:42 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 13 Feb 2024 10:19:42 GMT
COPY file:b5520696339eadb7386055c1dc9487351aa145a79b0cf206d8b1a79699c4a7f1 in /entrypoint.sh 
# Tue, 13 Feb 2024 10:19:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 10:19:42 GMT
CMD ["influxd"]
# Tue, 13 Feb 2024 10:19:42 GMT
EXPOSE 8086
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Feb 2024 10:19:42 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Feb 2024 10:19:43 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c23471dfddf803b1351ebb5b3d4fe3707e3ac3a7a3c9574ff29c4f051ad8b9`  
		Last Modified: Tue, 13 Feb 2024 10:20:16 GMT  
		Size: 9.6 MB (9581551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c083731976ebb51878cd8a78a3bc4f8291c326359194369224c90e386e8c652a`  
		Last Modified: Tue, 13 Feb 2024 10:20:13 GMT  
		Size: 5.5 MB (5463787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92022dec65d38eb8b9209992acb610dd55be10e4158d3cab9a587b362accb80d`  
		Last Modified: Tue, 13 Feb 2024 10:20:12 GMT  
		Size: 3.3 KB (3276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec78cb36cb163b713b768330e0c7a303246ab9ffe29743408a7dc8e82eca67c0`  
		Last Modified: Tue, 13 Feb 2024 10:20:13 GMT  
		Size: 936.1 KB (936113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b205968d00a4520c4bf78b3ca4fc6066e6f9e931a460894845dc6e45a1824d98`  
		Last Modified: Tue, 13 Feb 2024 10:20:18 GMT  
		Size: 92.1 MB (92086333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae6677d78716fbae2bad54c391131b9c86b6852a8df46439cad3058d3d5b7cf`  
		Last Modified: Tue, 13 Feb 2024 10:20:12 GMT  
		Size: 21.7 MB (21662585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ac9207e54c3a01b693d2f94e1beb51afadd5359682257c569b65b5e178f39b`  
		Last Modified: Tue, 13 Feb 2024 10:20:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e516d64e2dd7b9dbdf9a409f11ba5c10a1ee078b9bfd51b47516f102930f5e6`  
		Last Modified: Tue, 13 Feb 2024 10:20:10 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8cdbfbd26da898bf48152a8d90896d41de757543164d7ff4ff0ebd77bb2aa1`  
		Last Modified: Tue, 13 Feb 2024 10:20:11 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
