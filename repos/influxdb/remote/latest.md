## `influxdb:latest`

```console
$ docker pull influxdb@sha256:9bd00fec36c83a49ec02696cfb81456e0829bb010d0a7f6ed3ded434c3647970
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:b41113d30857f58b87ce939fe32b20530e3f6824122565585d0da5acc8bfae48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157222143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c0c74874d23f7a70b6264595ca29d490243e2e29ef3420dcab3eb82f60aed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:31:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 04 Nov 2025 00:31:16 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 04 Nov 2025 00:31:17 GMT
ENV GOSU_VER=1.16
# Tue, 04 Nov 2025 00:31:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 04 Nov 2025 00:31:17 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 04 Nov 2025 00:31:20 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 04 Nov 2025 00:31:20 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 04 Nov 2025 00:31:22 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 04 Nov 2025 00:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 04 Nov 2025 00:31:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 04 Nov 2025 00:31:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 04 Nov 2025 00:31:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:31:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:31:22 GMT
CMD ["influxd"]
# Tue, 04 Nov 2025 00:31:22 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 04 Nov 2025 00:31:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 04 Nov 2025 00:31:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 04 Nov 2025 00:31:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 04 Nov 2025 00:31:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d760f36d574b5965ede55de1f37396e22c8274f01374dfbe2197a775a1b2c6dc`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 9.8 MB (9796285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c390d620c1b7c532b764c0afec58bb5a030ba4c102a471a6522056d7a1505d0a`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 6.2 MB (6156981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576c8f8f742b0f2c3ac97a0a75b22a01d969131f4f824ee55a5409cf6633e12f`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f021bfd8769cf9b85220eeb67586078def716efc7c018ce3ea754bf166698b3c`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 1.0 MB (1012034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d1336870787fdfb8f92270ea211c6045a68fa1de7c055a3ca48bb20a556c72`  
		Last Modified: Tue, 04 Nov 2025 00:31:55 GMT  
		Size: 100.2 MB (100244535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea566b45da855532b721d67767a3bec06e14386ef9a81b4d8aabd1602d5db33`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 11.8 MB (11773789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6dac5794ccee8f1989dcfc9b6fab4fa530e7068a60adddfe0330c4cdb2626`  
		Last Modified: Tue, 04 Nov 2025 00:31:45 GMT  
		Size: 206.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537c337aa0854d3ffaa7bda109d38c11f9116e76adf9ff480f5665b1c183cd5c`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09ce7419d2ff8a451c80e56762e720ee9e2fd5fdc32854b48de3fecca2ff03`  
		Last Modified: Tue, 04 Nov 2025 00:31:46 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:f7abc7614cc3d608038611ad0e9ac66615e49c46efcf929121a445f91100096e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0edf95195302d29166549e18c87891c4db4ae20f8fecfffce43e49d92da79f6`

```dockerfile
```

-	Layers:
	-	`sha256:ee940180b22d23a182c5f17efc47243b2128d2b1b9d9339b59d977b9c5ee61d5`  
		Last Modified: Tue, 04 Nov 2025 09:21:09 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c9cd91a7e043b29be8b0da575714e92200ce018ca51d62a619f0240423837a`  
		Last Modified: Tue, 04 Nov 2025 09:21:09 GMT  
		Size: 33.5 KB (33495 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1a31c97f6b4cecaa8e73ccb4a36145184b9cec34c7e748a440229387de703cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151607103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a065d42bedd46cddd3c6d0c7b934e0d56465314e52e76cc09c7db47300002ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:31:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:31:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 04 Nov 2025 00:31:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 04 Nov 2025 00:32:00 GMT
ENV GOSU_VER=1.16
# Tue, 04 Nov 2025 00:32:00 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 04 Nov 2025 00:32:00 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 04 Nov 2025 00:32:03 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 04 Nov 2025 00:32:03 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 04 Nov 2025 00:32:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 04 Nov 2025 00:32:05 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 04 Nov 2025 00:32:05 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 04 Nov 2025 00:32:05 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 04 Nov 2025 00:32:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:32:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:32:05 GMT
CMD ["influxd"]
# Tue, 04 Nov 2025 00:32:05 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 04 Nov 2025 00:32:05 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 04 Nov 2025 00:32:05 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 04 Nov 2025 00:32:05 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 04 Nov 2025 00:32:05 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3e3a82e484a72d89ff48a1924927dbb3d17fc4516d9190170d2d1d8fdcfaae`  
		Last Modified: Tue, 04 Nov 2025 00:32:33 GMT  
		Size: 9.6 MB (9626470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed92ae317202478c02b5a80d6103d10d43ab6a8defe421e871261c59424ed527`  
		Last Modified: Tue, 04 Nov 2025 00:32:30 GMT  
		Size: 5.8 MB (5790417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f35582e5088719e3f1ce6579771caee201cef32022b54f0cf1509e672a1b6d`  
		Last Modified: Tue, 04 Nov 2025 00:32:29 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da3a26975c383c051421f67b3781746f0d35f4e73e3be5021f7794214af1779`  
		Last Modified: Tue, 04 Nov 2025 00:32:30 GMT  
		Size: 938.9 KB (938873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31db8f202b2c3f4e055de7cf12d869e913eca195352df6f481aec4825e066fd5`  
		Last Modified: Tue, 04 Nov 2025 00:32:42 GMT  
		Size: 96.0 MB (96039023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42752e6252f00feeb78a466e2cd0a4fb0599f9e50dd16a0f186bb0bfdc9e1389`  
		Last Modified: Tue, 04 Nov 2025 00:32:31 GMT  
		Size: 11.1 MB (11099989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf0e4f70931efbd284491fb6215a57fca107e7846c89ff1c1c5fc7cf49dd508`  
		Last Modified: Tue, 04 Nov 2025 00:32:30 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1485f244faf094be0c063e8de2e61e1a8dac28ebafb716ab0f247b2f8d0ca3`  
		Last Modified: Tue, 04 Nov 2025 00:32:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf14a42672100a6fff2ea9f1ee9594ae90eb866525204d9754a4e3b1df16b8`  
		Last Modified: Tue, 04 Nov 2025 00:32:31 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:f7b5ba50f7b37a5e13bd6297ccf97057ea1149217e23e1a13b8cc52415eac4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51de0097c36339f0ea7467850435aae147cc3b0fed0a8321582d25c84ebd78d`

```dockerfile
```

-	Layers:
	-	`sha256:df884ca819a55a61855f4a24b401b2f2ef3c96bcb5f8fa01a101c9942cfe8470`  
		Last Modified: Tue, 04 Nov 2025 12:20:45 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949e604b5155ac1e136018c5691324a42f8d34e8cdef2361e7deff6f19067e5a`  
		Last Modified: Tue, 04 Nov 2025 12:20:46 GMT  
		Size: 33.7 KB (33678 bytes)  
		MIME: application/vnd.in-toto+json
