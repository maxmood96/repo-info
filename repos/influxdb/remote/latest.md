## `influxdb:latest`

```console
$ docker pull influxdb@sha256:e3488e6a43e3bcd2362688f44af62f743a850a07b094cbd3df01724fce6b7f44
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
$ docker pull influxdb@sha256:6aa61b0709b741935ddc11b3feb8be7fd61d7cbe9c419134ace5351ad342f35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162413117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fe0b177a4bc5af1a6d23d4a29b862dc25ad3d95d1b5d9645e094721337e012`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Jan 2025 12:29:50 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a757182455a4e0cf07e5b909b055043694bc218177f4d959b2dc192483d7bb31`  
		Last Modified: Tue, 08 Apr 2025 06:27:44 GMT  
		Size: 9.6 MB (9587655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b13de37790c85f212ec3678ce7cb7f51ef1ef5e4d0b70167d0f7ebfc8a996d`  
		Last Modified: Tue, 08 Apr 2025 06:27:44 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14a115f225da66b7273eef0a892c5fdf9f45fcd6982cb80638fc05387002ab`  
		Last Modified: Tue, 08 Apr 2025 06:27:43 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0db3f56b30d5d2949b394b5f7b80926c76bc006e1eadb5cb50ae57457e529a`  
		Last Modified: Tue, 08 Apr 2025 06:27:43 GMT  
		Size: 936.1 KB (936109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466b65fc07b801823a30dc7bfc28cead3c82ab1084324a91fbbb21a559a22c93`  
		Last Modified: Tue, 08 Apr 2025 06:27:47 GMT  
		Size: 96.2 MB (96151343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dced1bac858ed83dd8f47354aacc2451e1504e7d8101ad489712e512a117bb57`  
		Last Modified: Tue, 08 Apr 2025 06:27:45 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70e71873bf8c06c93a99431cd4c182c027c6169c168b293aee114014b371ddb`  
		Last Modified: Tue, 08 Apr 2025 06:27:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04c1cf8b30ea21cdae4da298668a78cca571ef0a206e7890462137b28d37ea2`  
		Last Modified: Tue, 08 Apr 2025 06:27:45 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fe697f90b8832a7017fefb2df99c77ca02ffc07408377bb6a1253f510d4828`  
		Last Modified: Tue, 08 Apr 2025 06:27:46 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:e404d848f35e3e533c2e1a9a30af1cf44ff1de9bb294ca35f312380d9f94c76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2879436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1e58233d1abf25d160eda638a37138e983f870b6d6f56bc419a00c5ddfe964`

```dockerfile
```

-	Layers:
	-	`sha256:3df737ec64a5712025f95b22623a5aa3b111f48ed39cebb98f8a08ec8fa0fa36`  
		Last Modified: Tue, 08 Apr 2025 06:27:43 GMT  
		Size: 2.8 MB (2845533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7bb5a2334970bfd17f9ba3f99b4f41495eee93e04df4a6fadfc5433f5246cb`  
		Last Modified: Tue, 08 Apr 2025 06:27:43 GMT  
		Size: 33.9 KB (33903 bytes)  
		MIME: application/vnd.in-toto+json
