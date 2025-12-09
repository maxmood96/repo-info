## `influxdb:latest`

```console
$ docker pull influxdb@sha256:22b5a1b144d4229358010c2bc4890d73e8ceb9e09b9c4ccf944e14fa3789b726
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:17d07f43a588bc9c68c575300d89d3fd7d2a3a806a7d0295d21e8c2bf0d0563f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223c19717338c6f70e54d12b95a09e7b85196eededfa5715fb519279690c7984`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:10:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 08 Dec 2025 23:10:48 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 08 Dec 2025 23:10:50 GMT
ENV GOSU_VER=1.16
# Mon, 08 Dec 2025 23:10:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:10:50 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 08 Dec 2025 23:10:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 08 Dec 2025 23:10:53 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 08 Dec 2025 23:10:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 08 Dec 2025 23:10:54 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:10:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 23:10:54 GMT
CMD ["influxd"]
# Mon, 08 Dec 2025 23:10:54 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 08 Dec 2025 23:10:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 08 Dec 2025 23:10:54 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 08 Dec 2025 23:10:54 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 08 Dec 2025 23:10:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604851effd25328dbfe6e64335694c877236aba3650b90faeaa576df028ab2c`  
		Last Modified: Mon, 08 Dec 2025 23:11:22 GMT  
		Size: 9.8 MB (9796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a364d1ca582d8d384f2639605845be6cd1933b7cfab23889e439b562ca635a0e`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 6.2 MB (6156976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290754ae2d8f82fad5a9c75bcca7147fe844a1b3c30b2c2fb4cbbb70aec7fe2c`  
		Last Modified: Mon, 08 Dec 2025 23:11:18 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28be85d73b543b531c1ca66ca171591169061bdbd60466c4f8009c6506b2f2fc`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 1.0 MB (1012039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f964140667d59d01540c8f77351e60f8c6b6f58ccb3d8a49c1c769aff5beb2b`  
		Last Modified: Mon, 08 Dec 2025 23:11:30 GMT  
		Size: 100.2 MB (100244549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9221d71d25e21b5b393f1287210930844f181053787ea11b1b0a50bb1b362dfc`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 11.8 MB (11773791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9710e0fc7410459dc775d3654bc7daeaed98ba535a04ed12edb1aa7906daf811`  
		Last Modified: Mon, 08 Dec 2025 23:11:18 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ceb1bcf27d8f78c368c37fbf43476e1a17d8a04fed85a064432a3631fe519d`  
		Last Modified: Mon, 08 Dec 2025 23:11:18 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb26bb2f00dd254a3efe5d5e4f1c8e29421089ca970e693cf6eae354f56c566`  
		Last Modified: Mon, 08 Dec 2025 23:11:19 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:19e66dbdd74c58f3868f29872473e52a385c8406ffa34fd74e19932474119a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732f61d49321ec9b6d7f8a73df33f591bf6998258f9af39bd671a6b274d06159`

```dockerfile
```

-	Layers:
	-	`sha256:c24dde83600ab1332dc432b5fe2943195942e9191a6c0f8738faedf5e5a74f7e`  
		Last Modified: Tue, 09 Dec 2025 00:20:58 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae222d7860eb52590dc5d754c27b7f13aeccd0ae371307a4def21db3d94e3a4`  
		Last Modified: Tue, 09 Dec 2025 00:20:59 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebf4fd439730dadc92b3bc3f565966f49e0026098626fa0bbd1bf4dfcd3dc23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efe22d086df7cc3f7292fb6c0bfeb0bfd1e7dfe9b4ab2f531fb9e3cde7a74a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:45:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 18 Nov 2025 03:45:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV GOSU_VER=1.16
# Tue, 18 Nov 2025 03:46:01 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:46:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 18 Nov 2025 03:46:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 18 Nov 2025 03:46:04 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 18 Nov 2025 03:46:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 18 Nov 2025 03:46:06 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Nov 2025 03:46:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Nov 2025 03:46:06 GMT
CMD ["influxd"]
# Tue, 18 Nov 2025 03:46:06 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 18 Nov 2025 03:46:06 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 18 Nov 2025 03:46:06 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f18804d67ac382eaeac668698515f80ba62f0269c38f762d1afbd6be3db798`  
		Last Modified: Tue, 18 Nov 2025 03:46:34 GMT  
		Size: 9.6 MB (9626374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d00886f89ffaf07d35f7df7c3069dd3afe08bd1dd499c2d3deaddaba64ffad`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e659ab431338c547c1f98f68f92e58b74c5a951004693b9d9c5b87c329da5d`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b59935d05743ffa02ec8f0b55b5ac55704d51555f71109d405d50fbc5e4c9ab`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 938.9 KB (938873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562febceec6f34093da512fc564ef68229e13b9cbc93448890ee3b25d4cba3ba`  
		Last Modified: Tue, 18 Nov 2025 03:46:41 GMT  
		Size: 96.0 MB (96039030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df32be97c38ea00ccc65fad323f679e2cdbdb0a21bc3401d70f74bcbf63496`  
		Last Modified: Tue, 18 Nov 2025 03:46:31 GMT  
		Size: 11.1 MB (11099988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbff83753ef6903833194bdec45bf87380a34a5c23aa0fc130e0bec7a4eab930`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fe0dc91a3c9b16f488df0eaa5967b709ea1bb28034bc8e0fd57b84fc6c45b`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80207f266c84c3062586aff91f93c2d37fbd833c2a4e160bb775fb6509c7daa6`  
		Last Modified: Tue, 18 Nov 2025 03:46:30 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:39b6cf435fde35f43996921bf986e0b8c60bac78e8b3fb7cf079990262481998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6475c2031479b1a92ed17ff24f69f4ce96e1ca85a835d81b9112d15ec2f01be2`

```dockerfile
```

-	Layers:
	-	`sha256:f75d415ae191d84746f95f4d12fa681a914b79864281212c05c5e323c2df000f`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca60a4fb48824c8d0e9b163faaa7aea6a7b0fe39e6e4faf8a38ecf3778f442e`  
		Last Modified: Tue, 18 Nov 2025 06:25:29 GMT  
		Size: 33.7 KB (33678 bytes)  
		MIME: application/vnd.in-toto+json
