## `influxdb:latest`

```console
$ docker pull influxdb@sha256:fdc021c53c8cf02d9a532d45e2c8ba036178316b0daacbc22d44d81da2475c1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:565fd3432b668a2fea119e9d2d7e857c49688af708aafb30cb5c6476b8d73e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168475058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82765bab090017edb2e03a187c5668f5f9048b52efb857d458521dd5774160b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477705850a3a7f5f03e5d6a1a59a0dcfa91b94206e39a56cc6948133bfeee20c`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 9.8 MB (9788950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb97151d37e4aa70aa077f6162a9890304784966c35ba5d3af11f1def2b263fd`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 5.8 MB (5820938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f3fc2b91f4c45426d08bb4e1a3cbf12c856cfed711e1d43c65f2cc105cc256`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389c37eac14d118b3cb70b72e1f477a24c4986b26ade1960b57d552bbcd57f19`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 1.0 MB (1006368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd854556873c80b5145bf59213db12c5417313e31ecb8190690ce1899737ad10`  
		Last Modified: Wed, 04 Sep 2024 23:10:07 GMT  
		Size: 99.6 MB (99594066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ae1439b7721fdeded51a74c06d4911e5aa66f9c6de27df9df050d64d194d56`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 23.1 MB (23128301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81be0a7f65a5159ce17c6a5c844f578c79cdc48d004173b15b6fe6ed6b225dd1`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8f8db7d47ab30ae652279949643449f0f4722ac4e8f0a6bfcbeccf6a54b12`  
		Last Modified: Wed, 04 Sep 2024 23:10:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fc8982233fe665574473fa1c2f285de2428e3ce74a9d595f6ae0744bbcbdb0`  
		Last Modified: Wed, 04 Sep 2024 23:10:06 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:67c55d73c97a06ccd1f33b9623748a63f4bcd3bf5b9a466699b240eaa03a716f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de69f4b4f8604f2c94d486d1b0a00fa53c547ab5de99010a8578be79610d1673`

```dockerfile
```

-	Layers:
	-	`sha256:af7960aa38e90d8826134f7591e3b020c58f42468d23e5ab3ff2a5edca9bea22`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 2.8 MB (2833443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35599651b4f0cdc382b9c7d513b3fd5e35824e7a6c12b885cbf120268e730a08`  
		Last Modified: Wed, 04 Sep 2024 23:10:04 GMT  
		Size: 33.5 KB (33545 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fa710c0b48fdcf7853f4f7d46f5446972f533841d0d7bc17281bbb94b0499ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162241944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fdd459558be5fd739791861c73a281fc11836981158b41288c489253880160`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV GOSU_VER=1.16
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8cd4147de7f78511d80ebd168ada550c516bc7b7ed15865aa5a32fbd733089`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 9.6 MB (9585117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53bc08419b6bfeb1324aa33ae3db2694f2fc8584e5ca8cb0ce38b69722e84d7`  
		Last Modified: Tue, 13 Aug 2024 07:21:58 GMT  
		Size: 5.5 MB (5463786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538c7efb8a50366ebe479fb1164ac5884b2c467bd5679c363728e31a9d571586`  
		Last Modified: Sat, 17 Aug 2024 00:28:30 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a750c202e5b50033ce6a36919e5443d64d51e7922b6d199cd32282357cadab`  
		Last Modified: Sat, 17 Aug 2024 00:28:30 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388ea13e7c081897f99f624a419e2fb6ba40250abca939aa2fc44d28954c4db2`  
		Last Modified: Sat, 17 Aug 2024 00:28:33 GMT  
		Size: 95.4 MB (95427928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b5f9eba25f6be5e420691cda0d3d0ebb5b863318baf121e10c1373d1e3aaa2`  
		Last Modified: Sat, 17 Aug 2024 00:28:31 GMT  
		Size: 21.7 MB (21662515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbcaac9a6f0be85159f51a75a6329441708909cc50e576ed4dac254751d6c6c`  
		Last Modified: Sat, 17 Aug 2024 00:28:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba728053a8fbf27d554d1b41bb78e53e55d6ae71777ccbf455980455f9d53d1`  
		Last Modified: Sat, 17 Aug 2024 00:28:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a40daa09774d8b9597c3c294e183abb6ed0f068fdc3c571a58f9ca509a86f`  
		Last Modified: Sat, 17 Aug 2024 00:28:32 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:f47f278f6d673c7a43b2e3a0f3152ac403504959b478ca8e8f68d34acda23dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df9003c617c6c805c646942857b03ee0acfc18e5641fc9c70e8343a3b233366`

```dockerfile
```

-	Layers:
	-	`sha256:e74a13020760d0b1594e2f468a7e062c963f0d40b1b905b098d91ebf3e884fe8`  
		Last Modified: Sat, 17 Aug 2024 00:28:30 GMT  
		Size: 2.8 MB (2832680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab8b24e06e3966d3c99a91ff8ccb33d3f6a77caab1a7934d3715da10292e0fa`  
		Last Modified: Sat, 17 Aug 2024 00:28:30 GMT  
		Size: 33.8 KB (33848 bytes)  
		MIME: application/vnd.in-toto+json
