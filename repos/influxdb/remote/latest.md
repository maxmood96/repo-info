## `influxdb:latest`

```console
$ docker pull influxdb@sha256:817a43e512687edbcfe0605df571d5e53b11f8b7ca7a6b317e69f763dc9be070
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:cf8c92784dc721e6310ada35067f9d5893bbc9b99e8052237dcbe262b2f8f393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169052639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5b5658780163fd49de58a05c85391fd350be4292c3e9a7b90e6be6303fae0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aafe8e30583ab32a1e9ee7e2646e9683801bd17e63d70bb3bb3f4297db8baec`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 9.8 MB (9786114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3e64af86929ccda214e59bfcd54380f99fbd2cfbf05983e15896756066a27`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 5.8 MB (5820922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b71a5ef49de7ee06787b83119ef3bcb1e81622e6be5f57a39b2c898690a0d2f`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0160b7176ca064e8395e1b99248ceed4ae5e3af57b7c152b522e9e64e53619`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 1.0 MB (1006371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d48b867737d10ef449f819f7fa36ea92a5ec7448b52063d4110e326cac34b`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 100.2 MB (100174652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31cbe0a3f25d229f895dc1d474144dcc31c90a8e239848c874184752383e751`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 23.1 MB (23128334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8597d281e9c9cb18a861eb227d9f3fa67b5cfa74b1bbbf16f951c694f37ae4b8`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcfb407f38709994863cbc982f8f47e428ed743239fa858736d02334bbd5a6f`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634cb105b59a74b80dcdb92049a091cf008cb2fea675da232f5ac1f2d93d9df0`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:9fb4a6136fa974e51994e3422345aaaef66b65ec3cb32779092981f6ecbcb32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6139fd1cc0146a76decf6a803f95c12ac50149ef22d4c77500baba8b9f02c572`

```dockerfile
```

-	Layers:
	-	`sha256:c4fa52ea5261538daf2912b038fa96eadce9ce9198409ba8938af04c2b68cdcf`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 2.8 MB (2833446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b7394c3923f72225c4d186b8b3c829f52d3bc04899c3afa693b35d62339a6d`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 33.5 KB (33544 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad1b67786fdafa8a6c928afde9514e9e61aa9196ba48ea0f85b02d46de88d4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162819854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b90fc212a2e15b03dfea6f55bba7e6841e9e68345b5de78ecae786f6715ee4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:42:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV GOSU_VER=1.16
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXDB_VERSION=2.7.8
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Thu, 25 Jul 2024 20:42:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Jul 2024 20:42:37 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Jul 2024 20:42:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jul 2024 20:42:37 GMT
CMD ["influxd"]
# Thu, 25 Jul 2024 20:42:37 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Jul 2024 20:42:37 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Jul 2024 20:42:37 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d86bee5eb6e09d1e4ecabe00877506dfef15eb8c1d0fb37fd03689650e726`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 9.6 MB (9585146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8102b54b2061157b520e8d0c54ab9debfd7caeecf5b04ee4ff14f2a58c7ae5df`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 5.5 MB (5463802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929f8e0bdc48c34a35a494a9768a1b505a86513c4cee278321f7df04a94698c2`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c078ee5f7362fbfa31e25a1b4c0fd0631479e57f820dfffe3d06fb939194699f`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dd648633f64d4e39c97d3ef2a1d2784576fdbf65f90a11200b251c3b94c315`  
		Last Modified: Fri, 26 Jul 2024 00:20:39 GMT  
		Size: 96.0 MB (96005753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603c87bd567840dca04aa427260c8a8aef651d2c7dc55c70764e63200994ee71`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 21.7 MB (21662517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7164f83c3085ab88b97f6aaecb51faaabcffcd70da9232e2a3982b9f6188905`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132469a32a34a142198cc86019e6873278d6c8d25d43211ce10fff9327b6eb5c`  
		Last Modified: Fri, 26 Jul 2024 00:20:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bee1e60c9fce079bf33dec8d4aa96459f86b491cb40d9a012fdf6c7eaf6663`  
		Last Modified: Fri, 26 Jul 2024 00:20:38 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:e3c42143d1c2133c4178ab80b70d5a71beec793914426d9fba59eee164af843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894b26438d5a95eac85d03b568c647befed1805d6e9bf36fc3d6de8daecadb05`

```dockerfile
```

-	Layers:
	-	`sha256:83a2c2603d57f30d2d08d326b754c1e47956a0c97cf0f068b975475b846e4c5d`  
		Last Modified: Fri, 26 Jul 2024 00:20:36 GMT  
		Size: 2.8 MB (2832683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db705f4da94aa74a70c426336d619b60b6abc61281b289133bd61d6273ce20d`  
		Last Modified: Fri, 26 Jul 2024 00:20:35 GMT  
		Size: 33.8 KB (33843 bytes)  
		MIME: application/vnd.in-toto+json
