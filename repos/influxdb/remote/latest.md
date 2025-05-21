## `influxdb:latest`

```console
$ docker pull influxdb@sha256:c33ac14af66fee77fe5ba14d7ae3b7d7bdc53186cc589eceb413af9f02ca01a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:7be7e75f358cc9a41498b774a217457862e26b9fb0add2fb807cc8eeff8b09b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168645172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2def43b479b5213296cf94cc546f6d13f0b60f6891d9ba5034f5fb93f82c87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e42863fbf917dba1d766836b81770e15967448a3c6410d92e950ddecac6c55`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 9.8 MB (9790933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfbdcc44decf955f1d649b2ee7fb1dbfa1c71998d36496387259861082068cf`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 5.8 MB (5820944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dbeb28e9b9a5ac6bd7dc5f4e1a0492b48dee1b297b7960b9dbb5e70cfd316f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619522457ecb94cbc0e36611bbb2312d35b8ca38bac40596c4e5965a64ff6e6f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 1.0 MB (1006372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d3e2d4d64dbe43902a5d0f793e7bef3eea64d5a22f519ea3c4f36b8a78144b`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 100.2 MB (100242924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701cad0e28464a9b1c3f5196d8bfcdc50fd2bec501bb8fe30f5b0c3f1bb7fcb7`  
		Last Modified: Wed, 21 May 2025 21:01:37 GMT  
		Size: 23.5 MB (23546398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c58b87f333a4d73eea79083aa2294f7753b04c402a321e6098ef7a67dab54`  
		Last Modified: Wed, 21 May 2025 21:01:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6393554df92840606b3ffe8e897b394b7ce2b681cffd41f3e170a9446dc089`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc25c80f073d68bad44122268fd1a57631febec15ee6b544d34975ce4773ec4`  
		Last Modified: Wed, 21 May 2025 21:01:36 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:31ffdab1dcfa7b7027482c046340e0e4e3d3d5f746b81f0e5e25c81d8fe2bef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47429ba26e292482bceec4cdf8dbb0dca3795338f22c3030a890ac85d4ee8df`

```dockerfile
```

-	Layers:
	-	`sha256:b80c4678d52151bdba2ddadbec502eaf3df048dad8cdd7e73316f85c619a910c`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 2.9 MB (2869086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef63408be21053676231c89cbda0f54072a30c09521bb38c546f3823423a68f`  
		Last Modified: Wed, 21 May 2025 21:01:34 GMT  
		Size: 33.8 KB (33818 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:0839cb088f4a243f06560a4851d14ee7522263cce0b700cf84b53dd97ca900ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162301307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4045d580c6b33dc7f3056070fb3056024446dedf2f454fb9ac18669087e55c06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 21 May 2025 19:23:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV GOSU_VER=1.16
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 21 May 2025 19:23:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 21 May 2025 19:23:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 21 May 2025 19:23:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 May 2025 19:23:38 GMT
CMD ["influxd"]
# Wed, 21 May 2025 19:23:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 21 May 2025 19:23:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b410a06ce4fcda8c631e50621e6543d50ed900c819663b8e8c41c7f7ac89053`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 9.6 MB (9588509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de0fff97c4cf200ca210ae20785978cda6a042a650e28db59b324b44f41f905`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806918d354e310d08b135e40f2e2d26fcd65062af8700b837f4aa84de0482de6`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dd02a48352d53c118b216ffe4dbce8cea9676dd3da4bebf4dcefc7d299a03c`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 936.1 KB (936100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc6e61093af6624558cddc2362654c606748ecb54cee1a3486c6098cdbfed22`  
		Last Modified: Wed, 21 May 2025 21:02:11 GMT  
		Size: 96.0 MB (96038376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02942e730c824aa6fbe30374d5af1dd7d72e7c8c4c9a0298374f5c6962c87c`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 22.2 MB (22197938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b32a406b9d356f60656a71f8e36b9f9bcf243eaf723901c78828482765101a`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9872dc5e700b80dd89f142c8e61e7c3f60a789e35de74d0c0f4321b48245b58`  
		Last Modified: Wed, 21 May 2025 21:02:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f917e572fef7a9039d0ba795a86b841215a450065b9e2e783189157ef6e19122`  
		Last Modified: Wed, 21 May 2025 21:02:09 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:f0906a5dd25bedffed8866016cdbe9b64eeb5e6c3d11c522f74a73e616785680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2902315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ceac7e7fd2dc69af9be74f65c2a4737611300d774979a37d6dc13f6695244d`

```dockerfile
```

-	Layers:
	-	`sha256:1e76d058079ee2ce737fe5009b78a9362df4797f206fcf557ce706df337fde24`  
		Last Modified: Wed, 21 May 2025 21:02:07 GMT  
		Size: 2.9 MB (2868314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f554075615356b4d24f3930e6ac1ae2742ffae4bbd677ce1846d300062b29382`  
		Last Modified: Wed, 21 May 2025 21:02:06 GMT  
		Size: 34.0 KB (34001 bytes)  
		MIME: application/vnd.in-toto+json
