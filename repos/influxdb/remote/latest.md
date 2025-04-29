## `influxdb:latest`

```console
$ docker pull influxdb@sha256:d92a10e9e75aff18eca38ff3a8f0b4a800706a5dd44d1b0ece264af04458525b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:81288d632101c9bb035ca29eee5c98350ab3f45254ae665f1ff3be5e27028181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168714517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e98870cd7bc176c8c21650b3ab3e6bb1b7cefee0a9b881f7e5b699bc993f811`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 18 Apr 2025 17:08:47 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Fri, 18 Apr 2025 17:08:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV GOSU_VER=1.16
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=2.7.11
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 18 Apr 2025 17:08:47 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e52b528d16852fd497e71feceda1b79a40a24f7d03f37898959736d38ea73c`  
		Last Modified: Mon, 28 Apr 2025 21:56:42 GMT  
		Size: 9.8 MB (9790255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d4b4b2a00ea6780801ceddbf6f0f73c89ef7675f5c94fa373218d68b6acc06`  
		Last Modified: Mon, 28 Apr 2025 21:56:42 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6694aa4f244a0294846cf14e8a21414b0a69b71b9428ca1a5b57db1cef8b7f6b`  
		Last Modified: Mon, 28 Apr 2025 21:56:42 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39495c4afb961000fdffba766f1c9401e43ebb0db1ea558d24038b638c5c505`  
		Last Modified: Mon, 28 Apr 2025 21:56:42 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a738af6c8bdc5ce44bbd054cb95e60c3153281382d2c16e5560b016516f7149`  
		Last Modified: Mon, 28 Apr 2025 21:56:45 GMT  
		Size: 100.3 MB (100312950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4ae9be4197bb3d6f58ca269e1c525cb10356b12729d58800addef815970158`  
		Last Modified: Mon, 28 Apr 2025 21:56:43 GMT  
		Size: 23.5 MB (23546420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0dd4a375f64ae950095b837951cd9f26b4999629544adec34ae8a7ec45a44e`  
		Last Modified: Mon, 28 Apr 2025 21:56:43 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a10144993cc740628df62533992f02f2b27c29ad9c010ec206d7bf6e0f0552`  
		Last Modified: Mon, 28 Apr 2025 21:56:43 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fd1e96734c9705b1813fcbff2571738103a89b835be164219fd39f6507e866`  
		Last Modified: Mon, 28 Apr 2025 21:56:44 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:e42a25165275b137976df14bd89a0f190630271215bb96a55020e6bd5aea21ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de29c60f4940dc4598612b48488739c743db71d7dcccbe2628504b299afc76c`

```dockerfile
```

-	Layers:
	-	`sha256:cf40586062f775937721bfa4b33bddde25d6deb91c06f6cc64333562a93d7e8c`  
		Last Modified: Mon, 28 Apr 2025 21:56:42 GMT  
		Size: 2.8 MB (2846305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e31c55425041cf501eba9e226c6181799897c9abf441e613d817a2187e1bda6a`  
		Last Modified: Mon, 28 Apr 2025 21:56:42 GMT  
		Size: 33.7 KB (33720 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d2c4ee9910fabfe41b079d024eb2746853b5748e775520a9c9527f7f457b92dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162413460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bf6682979031149a4457a3ecd6c4bc22e38debf0c19549f15448e15b543999`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 18 Apr 2025 17:08:47 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Fri, 18 Apr 2025 17:08:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV GOSU_VER=1.16
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXDB_VERSION=2.7.11
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 18 Apr 2025 17:08:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 18 Apr 2025 17:08:47 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 18 Apr 2025 17:08:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 17:08:47 GMT
CMD ["influxd"]
# Fri, 18 Apr 2025 17:08:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 18 Apr 2025 17:08:47 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 18 Apr 2025 17:08:47 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4a512cf652ec8534ce10049bff0cbe021edf2c83e7da5f0317d0ceb448b9dd`  
		Last Modified: Tue, 29 Apr 2025 02:09:58 GMT  
		Size: 9.6 MB (9587642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe17df72de6cb8729cf170c5f7921505a4c3ffab82019601c46f8bf10879b66`  
		Last Modified: Tue, 29 Apr 2025 02:09:58 GMT  
		Size: 5.5 MB (5463793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67542da5a95ae6378acf6cd35df508e20c27bfad7b8a7212ba9bcb7ad86cb1bc`  
		Last Modified: Tue, 29 Apr 2025 02:09:57 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710ea74a5df9a36b3fdc68f19a169255f98d0b95a133c3e13af9117feb6784cc`  
		Last Modified: Tue, 29 Apr 2025 02:09:58 GMT  
		Size: 936.1 KB (936104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad9e8c0a3ba5541283a89ebae46ed3cee037898f8ad986fc2d25ae45b759b5`  
		Last Modified: Tue, 29 Apr 2025 02:10:01 GMT  
		Size: 96.2 MB (96151405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee7aa3b641878aee2fa17f806943e5a4fe9f820f4db889f91042e1492ad7345`  
		Last Modified: Tue, 29 Apr 2025 02:10:00 GMT  
		Size: 22.2 MB (22197940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e528e5c5d3b239a7379e6dae87581e4304bf480e44a6aa1721128d3701643dba`  
		Last Modified: Tue, 29 Apr 2025 02:09:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dc281f2ec990536e09721416607aedd1203f25a9d6849e14ec9233df2f6258`  
		Last Modified: Tue, 29 Apr 2025 02:09:59 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7322614bb33d958cbf440e60f31575fa86680a1f2594992d80d4c133d12a926b`  
		Last Modified: Tue, 29 Apr 2025 02:10:00 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:4bb611b32064569f9878bfa7114fb59efccc11fb24e175078466f7c8ddcc885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2879436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bddcea3464f8dd2ee24cd423127141e56cbeb097ce07dd0bdfa47575bc42ae`

```dockerfile
```

-	Layers:
	-	`sha256:f9c0bdb827b4ba6287649d6ccc4959e9f327650ce5bf5afff32abefd65509f8b`  
		Last Modified: Tue, 29 Apr 2025 02:09:58 GMT  
		Size: 2.8 MB (2845533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7dc1bab11be09b6703d04984decdced7e71c8ab4e33b071e3e25c31271b676`  
		Last Modified: Tue, 29 Apr 2025 02:09:57 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json
