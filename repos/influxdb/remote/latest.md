## `influxdb:latest`

```console
$ docker pull influxdb@sha256:e6101deab8aaf54d4bf543e1835a57bfaf007d711c0ceb952f720250e081e124
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:d99286d6d608ab56c099a34cf89b06081855e4e74b7f19cbc77f0767bc481960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163963521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8e0548f67de407e9e1e4c3dd2ec1624e6580e697fdc0eeb8d297bfa6054924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Apr 2024 14:27:41 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3281a4f6315699b26a503c6566f103759a828f12f553d92c9b8568fc7c1559d9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 9.6 MB (9592066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771d8fabb6d8d6168dff52e46c2de8bd63cbd254aa1daaae0de29c4a8a9c60ca`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 5.8 MB (5820930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd80e673f4ae3a675aac60f5fe134631bf83ca02d261dbb6e0b2c5ac459fdb5d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbc0440f3fc95e1ee5718c116e488c2ef54dd855e8a785fe0df1b38d3772ace`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287862d976b0fb6bb758104e481b6ad632695afc1b02be6b63e62a7c08d181`  
		Last Modified: Tue, 14 May 2024 02:56:17 GMT  
		Size: 95.3 MB (95255495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600d43bc88368488e797321a2e61f29d6693c25109fbe3e90f0ace24ed64e94e`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 23.1 MB (23128297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c5b27d92fd53db8497e383fd147eac93f0e9855db3d6ea795a2b94db66a8f`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e3f9b103c4ff3003adecfabc60a61919e76d6e3ee51bef7922da4fd4288a9`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccdb2a969faa0715ed4dd94da0470c3f7c197963087f7583b9acdeefca42bbe`  
		Last Modified: Tue, 14 May 2024 02:56:16 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:f4b8b5685fa1e5e9b907546f08c5ad89a95a70e489fdd70d6c8162492791d1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7011ea586dd090e9eb31c3ad42fe4ecdf4dc7b525db11c74583f1d317c3c4ec8`

```dockerfile
```

-	Layers:
	-	`sha256:18a0d6b5136dce2ea4c5894cd551c68208911928081cfee3ec4909776478332f`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 2.8 MB (2755207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13cf10a8af436c29a25887e528c27a9c80df9830f83d34a67a68dd42f52706d`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 33.7 KB (33658 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:699bc7cf026d3cccc062d6eca5bb3885afd049805c1404bd22a1d0b848e32de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376f599e99efeccbea38563b17aabf1e993c84f2d34dd48295677f9c96c1ed64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 14:27:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV GOSU_VER=1.16
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXDB_VERSION=2.7.6
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 30 Apr 2024 14:27:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Apr 2024 14:27:41 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Apr 2024 14:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 14:27:41 GMT
CMD ["influxd"]
# Tue, 30 Apr 2024 14:27:41 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Apr 2024 14:27:41 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Apr 2024 14:27:41 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40563ea69cbff5c1a45dc75899f1920a44d187519177c04caa3e0f5f138a8c8a`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 9.4 MB (9388782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28c661e904ab15890c4a25b4217fab8234fc61bf4e1c058df70093905fbec24`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 5.5 MB (5463797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9a655a4caf7037c6216f987e7ea1c8fcbe01415474fce2e85ae098fcbafdf`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 3.2 KB (3238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf7d30f7eda7ceb44953d13f39d62db35a2ca13a0ba19e88682ca879010fe27`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 936.1 KB (936106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6c1ba5bd8bdd375ee2ddc8bd62fa973e7ad9ed6e3449be80e7efa989f374e`  
		Last Modified: Wed, 01 May 2024 22:29:53 GMT  
		Size: 91.5 MB (91453330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fb235dfc2b03bcc24acbdc416c33dec3257d88ae34cc37dbd77d82339c6482`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 21.7 MB (21662518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7b1954b4b11866cd6f33aac1578f4f63da2b9a87dbf7aa3a750444fa5fb191`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80783551125bd030a5b4801fe8a543f9992dfd78cc8167287f8ae7f0bdace9ed`  
		Last Modified: Wed, 01 May 2024 22:29:51 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2745e5c37bcf74a3f4367693b5b8614ee22f8acdba508ac87dd077ee2f643b4e`  
		Last Modified: Wed, 01 May 2024 22:29:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:763bbeb6a5448752089fa864751e6a65218cfe71820b613c0ef24d493615248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2788036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d633e6c24b200747f5250a8fe360118217b18a2a11e2682f806b2eb3146afc`

```dockerfile
```

-	Layers:
	-	`sha256:ddce326635feac46d03bcc4edf86da3df7acd27e90b4d375d9a3d3b1381a1bb5`  
		Last Modified: Wed, 01 May 2024 22:29:50 GMT  
		Size: 2.8 MB (2754542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee75260e7b456b1e3b48a502858dda3e0be6db7bb9bf26b87c6dff2b2e4bdb3`  
		Last Modified: Wed, 01 May 2024 22:29:49 GMT  
		Size: 33.5 KB (33494 bytes)  
		MIME: application/vnd.in-toto+json
