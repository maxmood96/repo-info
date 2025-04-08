## `influxdb:latest`

```console
$ docker pull influxdb@sha256:9e555ba870e72b298db9edcadfa8a088715732e6be092dd9b7eac90119c17ccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:7a268a0b02f1da10448d534b227d2b5c6271545697bb494d578792d64f2c96eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168714078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae3d3e17015c5bfdf097ef6fc37885326ac42571decb61cd67f45064ab57aab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 16 Jan 2025 12:29:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV GOSU_VER=1.16
# Thu, 16 Jan 2025 12:29:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=2.7.11
# Thu, 16 Jan 2025 12:29:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 16 Jan 2025 12:29:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 16 Jan 2025 12:29:50 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7569dfbf1b2ce67d7f227401714eb0202d3a34b182065b6d9ca46cbb2e313b8`  
		Last Modified: Tue, 08 Apr 2025 01:25:48 GMT  
		Size: 9.8 MB (9790210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edfd550ddc4fc1b306d180d6a8e7c8d14595424850c8b61293ea9fa71394735`  
		Last Modified: Tue, 08 Apr 2025 01:25:48 GMT  
		Size: 5.8 MB (5820930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c0d915e2771971695214690fda4a9cf5eb4bcb014a1c86a3fde0a08eb1bce`  
		Last Modified: Tue, 08 Apr 2025 01:25:47 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0213fd34911043cc111d4caacc50e8c4972eeda16ed8c52750dc3cf47915ae5b`  
		Last Modified: Tue, 08 Apr 2025 01:25:48 GMT  
		Size: 1.0 MB (1006369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d215588bda8308838e37d9a98417c94999cbe15377e694debdb05546b8a97f13`  
		Last Modified: Tue, 08 Apr 2025 01:25:51 GMT  
		Size: 100.3 MB (100312942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae03cf3fc689e0bcc273b9180e71b773de3c0667d2e776913bb199660653dc67`  
		Last Modified: Tue, 08 Apr 2025 01:25:50 GMT  
		Size: 23.5 MB (23546410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb49061f909930a7c928933ab03109d7952445512c8125287ab0d43d2b1f2a5f`  
		Last Modified: Tue, 08 Apr 2025 01:25:49 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7df58809827561c88b0fa73087f4316e80ae6267ae91473ce42d826af422fd`  
		Last Modified: Tue, 08 Apr 2025 01:25:49 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ce553ea730f83f961d722dbd3a9b0f93884aff8b3cc0d91a9a04c1a037468`  
		Last Modified: Tue, 08 Apr 2025 01:25:50 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:2ff9f1fe57d087ec6a02e393064f7e030a87f11bb8112f09826397c47ef8267d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb232d294aadc4266222ee1da8607a07ceedbc122758cfb3c3c10c6a93a00ad`

```dockerfile
```

-	Layers:
	-	`sha256:808b90fed417c50f2ceded2709e0e39043b1c49c43e06c6f55446ae29d897345`  
		Last Modified: Tue, 08 Apr 2025 01:25:47 GMT  
		Size: 2.8 MB (2846305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2fcc7d5759682ad61a23242fc4f3cba8408b8c55c5e24a8a5435295e478f3d`  
		Last Modified: Tue, 08 Apr 2025 01:25:47 GMT  
		Size: 33.7 KB (33720 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c111ae90336e7161ea0b561fbad2313ebe2d2a780c3b03f7bd5f44d69edf77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162390860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f3c3669b03b683a982ce47547baee52045b6aeb97be45dc7afdd9d4e6c3eb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 16 Jan 2025 12:29:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV GOSU_VER=1.16
# Thu, 16 Jan 2025 12:29:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXDB_VERSION=2.7.11
# Thu, 16 Jan 2025 12:29:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 16 Jan 2025 12:29:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 16 Jan 2025 12:29:50 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 12:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 12:29:50 GMT
CMD ["influxd"]
# Thu, 16 Jan 2025 12:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 16 Jan 2025 12:29:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 16 Jan 2025 12:29:50 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2539f5934bf78a20ed72078642386bfd427cc80b86231c70f2a9f325b46d4`  
		Last Modified: Tue, 18 Mar 2025 04:00:36 GMT  
		Size: 9.6 MB (9587625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd1b82bf9bdda41498363a4f65102ccd382aeed1a1c96c5a0494af5610549ce`  
		Last Modified: Tue, 18 Mar 2025 04:00:36 GMT  
		Size: 5.5 MB (5463795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fefb2cb2fd330a346eab19bde7df4325db3ece683919cf4f31a5b8f383d9241`  
		Last Modified: Tue, 18 Mar 2025 04:00:36 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30334ae928180181a20a6fd2ec9c09a63543c878150ca73004ba9f90669fafb3`  
		Last Modified: Tue, 18 Mar 2025 04:00:36 GMT  
		Size: 936.1 KB (936100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb86366f0c9bc6c560ea08953977213faaaf1a7d6e63b5d252f442bda7f54d34`  
		Last Modified: Tue, 18 Mar 2025 04:00:39 GMT  
		Size: 96.2 MB (96151401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c63fdd53f07b41d33700709c6741534b4f3d45d1bef05a2ff225b2e6328a1f`  
		Last Modified: Tue, 18 Mar 2025 04:00:38 GMT  
		Size: 22.2 MB (22197942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d854b2c94de0a5064ec87623c86e958e3ebd4d8944611628185b2c557a0b2333`  
		Last Modified: Tue, 18 Mar 2025 04:00:37 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1960380a2e8b338a50a6a46db543cf868b76a02ef792a04952de511b2732e27d`  
		Last Modified: Tue, 18 Mar 2025 04:00:37 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a005551db9395fed4b0682d301b5f5da40153ca4c73e7cab7f1c13c9a480d5b`  
		Last Modified: Tue, 18 Mar 2025 04:00:38 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:455801152cf5cfae36cfbb3d92ea03699137481b8e1da49dd50991eab7513151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2881788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285996bd4b2b10d07651bdb18a57fb2a9ea0ab804d7811872a957fd202d75f48`

```dockerfile
```

-	Layers:
	-	`sha256:725e6b3f9db426f6a06e57850ab9fbb9d04004edb49604e3e42523605aeae990`  
		Last Modified: Tue, 18 Mar 2025 04:00:36 GMT  
		Size: 2.8 MB (2847885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92446e2e01d19234157f319f44c7a75733a1aa7d485042c27d36655d765a883`  
		Last Modified: Tue, 18 Mar 2025 04:00:35 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json
