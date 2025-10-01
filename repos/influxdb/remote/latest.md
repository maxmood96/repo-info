## `influxdb:latest`

```console
$ docker pull influxdb@sha256:4b420bab57e838178886bacf70de8a6da398497718511da1e637780eeee41106
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:0121b1ef000ad9ee6fd18236fbda5b578e2d2b53ebf88b2852a5df1a2e6b88d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c729c6b61bf04bccae282b4a88b0af07233b54566c44357100bb3f1f93d5bb09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Sep 2025 13:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 13:45:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV GOSU_VER=1.16
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Sep 2025 13:45:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811aaf99bbf19a9910d62277e035aceff4198c7f376b20d593edff533f641d1d`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 9.8 MB (9796261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343156d2f44315d2944d689a3b6ba5fb12db96d0735c74f9f5061dadaa5ee050`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45de5a0fe55cef8d3934d43433657930fba76ec5ddc4d981cdb77a35dabec0f0`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17580cec1ecab1149b131bab26b9ef493f6544152e36e43a4a8fda262ad2f742`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33043d02209c6f842255867f3e7a3cad421ba64cbeb2927ddda8ceb54856a854`  
		Last Modified: Wed, 01 Oct 2025 14:21:09 GMT  
		Size: 100.2 MB (100244546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0f8fa108abae31ed054ba64b943b34c7f988766fc3cabc0fce10f5829c87f`  
		Last Modified: Wed, 01 Oct 2025 14:21:07 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6a602b2831120358c8dc7d1f25aeef36e9c54553e633ad61ab3fb092c94ab2`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85a2aece113cd4582f9805ef8101ef31daf5e4fa684167883c30011b7c0606`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6f0e586b1a73cc1ab4ccebc8f1a38ca717d394b624b137718be85c1bbeeeb`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:185b77ece5df1f271f383b88de53edf5a6de19f2ffe13d95248ad30a48bc316d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd30accab1f61a0131fa41611377459c8480e8dd58fe1768c27ca200763ac693`

```dockerfile
```

-	Layers:
	-	`sha256:92d23af2aaf90e882cd2ebd504b46e52e629c0f42394d304d6939d7b8560f61f`  
		Last Modified: Wed, 01 Oct 2025 14:21:04 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e33518cd60ed9dd866b1f385742a274e53eecdf30023662122b59428aedd35a`  
		Last Modified: Wed, 01 Oct 2025 14:21:05 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:360dcee62c844c23a234bfafbfe5511a9eec36708ac018898417109abf442919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be31ac8b81e9cfd609c523de74012f65cb50e861e392ba63ba22aabd796f607f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV GOSU_VER=1.16
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb01127f4ecc7cec32d1038e47228414dc56b31af3bbe48fef16e87315ccbe2e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 9.6 MB (9626297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946c56889b4245bea086fd3932326e26ad874953fe751707350630acdae998e`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 5.8 MB (5790419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9e3f58b659a18c358e334cc15930a931b940051e6d5c5ea9c651490f58865d`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5242355409b896247ed91922f8f8eed4ff5cbf779a515539eda0d707bc28fd38`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cce3bcba21ff833984ada7e3fa4ecf3160c0b46f032bbcf082a0caa3d7fd09`  
		Last Modified: Wed, 24 Sep 2025 20:42:21 GMT  
		Size: 96.0 MB (96038999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db4d928b52404e26b6f1c213333ab49fc4d1f2e17d01312187f82e96fb5478`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 11.1 MB (11099991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802ede4ca46ce31c894904679fe589cc47cb6a1623f99c04f2f0476135eb2fa8`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b64c4076b267fc9adfeab0eadbfabc70fd195b90720bfe6e74378fa0621d42c`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7864a9ac5c643bf554f8ba4d96a66ab30967e45048c19bbc695e08f70d2ba50e`  
		Last Modified: Wed, 24 Sep 2025 20:42:17 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:740c7608085e12a989c31bb6765091b2e748e1ac2e1ad5b729683c9c7ed8445b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f4c48a7e65713d45172ae2f2cc1fe1409b4d8d33212de76f972c846d8c46bd`

```dockerfile
```

-	Layers:
	-	`sha256:6fd46fce2dd3e7092712a8481fd90a644582c32e5ba9ea39c77ecc42c7ff7511`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b376a7e3f08be287cee166060598253dc80b41b60df84212e3b7b21d5ab60cb`  
		Last Modified: Thu, 25 Sep 2025 02:22:02 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json
