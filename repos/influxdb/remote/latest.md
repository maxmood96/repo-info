## `influxdb:latest`

```console
$ docker pull influxdb@sha256:32418efff9e2e2efb99f0c93c78f2a2cd4f5316ec8c2983a64c9a53925f96fcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:f5d5196210d9fb9acf485f18bdba66a0146b4ea1565005a6dc222e54c73f1390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168893012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903cf06eba30eddc4f08a676144fd3b03d2d0ac76bcdc42911bfad8bcca01b56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aafd1fd27c9676f57cb06374aa92c43541fcf93e2720bf3fa5d5bf45a284109`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 9.8 MB (9789031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61735b6533a48feec22deeb5e11cfc795f344ddd91e8cda094b5fbbfd789c6f2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 5.8 MB (5820924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f27f427a2ce3808d8d9a09b50c52ff0933efa417b0bb9d281ec378def2d968`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf90975e867fab7ff0862159e12b24232ccebe662618746db3dc2d820506fbb`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 1.0 MB (1006363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55253b104f96a5e5ab0e9190cdbbf891d973155a6bd43a3e0f7dfe665e9b84b6`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 99.6 MB (99594050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b1de93c35668207e140c849313b99d49006c6f8fcc9cb1623a3a3915f10590`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 23.5 MB (23546404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd940528b08fc4347e306e9ba4c6be5cca185b598a9545f915c09fc97c2727a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d55333cb59d840ce4b040a27abe0d24b5e44c9ec76107ad85193b5b3a086606`  
		Last Modified: Tue, 22 Oct 2024 19:55:48 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff84a72bb18b35058f8c116017714f3b4a543263aa2aa29ecddfca1b2519479`  
		Last Modified: Tue, 22 Oct 2024 19:55:49 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:9cde691a07e51f352cc9ee6307c46b4a793741ba7a49f418037bba33d7ab9fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2883180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b20c55a4f47fd0d3aec51ead07b507cd683ae9693d265dd7e85159462b6d3df`

```dockerfile
```

-	Layers:
	-	`sha256:25056c70fdda68055fcfffd672a27976cc63407c18987e45e009d739d4e06e9c`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 2.8 MB (2849661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3057611b4133f25ca576be26bf2380aba98ff5136f48e234f51188f477b24de2`  
		Last Modified: Tue, 22 Oct 2024 19:55:47 GMT  
		Size: 33.5 KB (33519 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:53c9749a685778bacdae9243980b8e5d0d0ef1ceb947ae41f91f50f621bdd595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162779131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bba075abbdb7b751d98b8f4ea79668db114d755eeb1e92bc60f42cb0086c961`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV GOSU_VER=1.16
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 22 Oct 2024 18:38:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
CMD ["influxd"]
# Tue, 22 Oct 2024 18:38:37 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 22 Oct 2024 18:38:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07320876b49207ad14955b1a31e4206a2a4153727413f4e8fcda5fd99916b4d4`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 9.6 MB (9587112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270e2f52b84341a01fd4a919bc929d7490c2caa4e34017d8376c18acf47acab0`  
		Last Modified: Thu, 17 Oct 2024 13:12:50 GMT  
		Size: 5.5 MB (5463796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837b8381563c809d09e25282b246ced163daf23d4c3c348813468b2323ad3a8`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 3.2 KB (3226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054534f2dd1b04e74b7e15809341ecf0eaf97c8736f86600f77b8e29157eb2ec`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 936.1 KB (936108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d35e35d48ef6197e613fc0a0ff0dcc745084aa9439077bd2fc66add3b7885c6`  
		Last Modified: Tue, 22 Oct 2024 19:55:11 GMT  
		Size: 95.4 MB (95427909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb1b21f57ab00e3ecc4e16f96efeb63f8475fef567e59e85331bfb428ecf23f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 22.2 MB (22197911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b88297b74f1c1c8700a853a735372741aadc94d4467ea21b2373a36ed465bf4`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37363f631d39bc3f49ae72bacaad18758d54157dbf4308a1a3f1b7aaa3eb4b89`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013632725e99110127ab8f36dca492a8346ea517875e282a611b494b519e33d9`  
		Last Modified: Tue, 22 Oct 2024 19:55:10 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:684e07d361a121efaffb0611b94bb5bd45e4fbfd743f323029d3a52f633bd3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2882659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d6ca703457d4c565f9d48a20f346d8cfeaa0d9d18d394c948b0017c3e323fc`

```dockerfile
```

-	Layers:
	-	`sha256:f8b67510dcce1fc81e9b513aa534ce749c701750b139696527cbb54bb78e320f`  
		Last Modified: Tue, 22 Oct 2024 19:55:09 GMT  
		Size: 2.8 MB (2848898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514acbd511f7db84016cde5cc9c611926cde97d7b7733a7fa188ca8993a6d91b`  
		Last Modified: Tue, 22 Oct 2024 19:55:08 GMT  
		Size: 33.8 KB (33761 bytes)  
		MIME: application/vnd.in-toto+json
