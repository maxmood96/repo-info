## `influxdb:latest`

```console
$ docker pull influxdb@sha256:05ea1901ea421acf031b74e65b737fc911500e7f61189380596f84da18963fd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:c1a54a99df67b5afc8e957b325b1abfdbf3a381442c987e68ab0815eec8c5122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110771137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136bb61703cddb7634d59ae73ebcd901711083532c2dedcdcf65b81b0e3dbc56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:19 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:42:20 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Fri, 08 May 2026 19:42:20 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 08 May 2026 19:42:24 GMT
ENV INFLUXDB_VERSION=2.9.0
# Fri, 08 May 2026 19:42:24 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 08 May 2026 19:42:24 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Fri, 08 May 2026 19:42:25 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 08 May 2026 19:42:25 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 08 May 2026 19:42:25 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 08 May 2026 19:42:25 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 08 May 2026 19:42:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:26 GMT
CMD ["influxd"]
# Fri, 08 May 2026 19:42:26 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 19:42:26 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 08 May 2026 19:42:26 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 08 May 2026 19:42:26 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 08 May 2026 19:42:26 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5e99a62a654e977d6805f2687220f6713711b5f78ac9489111076f92ae6240`  
		Last Modified: Fri, 08 May 2026 19:42:39 GMT  
		Size: 9.8 MB (9799019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f47322e39b1705abd30b9c76bfb3c30b9c18b9c133b45ed822def32be004d6`  
		Last Modified: Fri, 08 May 2026 19:42:38 GMT  
		Size: 3.8 MB (3822788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f92e949eea1e243560fe5cde491afd90017487844bdea3d41670a0179369d0`  
		Last Modified: Fri, 08 May 2026 19:42:38 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15bebbddb82deeb55dfabce0ecc185fd50a3e920f7f59c68beab69813411de6`  
		Last Modified: Fri, 08 May 2026 19:42:40 GMT  
		Size: 56.5 MB (56481042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362f15d1489275cc9a26d8411803c2ae6885d96be4c7773f5fd8e8e59f4ff8d4`  
		Last Modified: Fri, 08 May 2026 19:42:39 GMT  
		Size: 12.4 MB (12421823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72b4ad5bcdcd19415830e67dd1b07ffc46427ff1f7d5bb6aaa94b44a499fb4f`  
		Last Modified: Fri, 08 May 2026 19:42:39 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4929852a9b0eaaaf6ce094918c8d7b3bbe270b9edd6309b997a7927845455b47`  
		Last Modified: Fri, 08 May 2026 19:42:40 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25e450bd8fea224c27ff2c8d3b1f7502bd04df38bec524efdf468f21403beab`  
		Last Modified: Fri, 08 May 2026 19:42:41 GMT  
		Size: 6.5 KB (6508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:ef67c3f9415020aea924b76b2e8f1a1f775572678828842c8da22370ca6f5a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a255b6f0a21f07bad405d2934b91b0bb5132c3fd5d6ec28cd0ec56d4b8c8db3`

```dockerfile
```

-	Layers:
	-	`sha256:bc1e413d012bc037989be4a897a53271bd8f40eb2d249a6a1397d3257b7223fe`  
		Last Modified: Fri, 08 May 2026 19:42:38 GMT  
		Size: 3.0 MB (2958900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55292d2ab06379add6c6ca441f45f51dcf84f4e78919e8cb8d344e732e7946aa`  
		Last Modified: Fri, 08 May 2026 19:42:38 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:34f990b5045a9fe57d4e996cb7f033cb049a58c24ef45b43bb59ffc27811c9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106319337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f91ee0964eddddca490e1d582dd5dbdfc345761ca8b6b82053e6a0c4a1bf11c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:04 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Fri, 08 May 2026 19:44:04 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 08 May 2026 19:44:08 GMT
ENV INFLUXDB_VERSION=2.9.0
# Fri, 08 May 2026 19:44:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 08 May 2026 19:44:08 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Fri, 08 May 2026 19:44:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 08 May 2026 19:44:10 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 08 May 2026 19:44:10 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 08 May 2026 19:44:10 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 08 May 2026 19:44:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:44:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:44:10 GMT
CMD ["influxd"]
# Fri, 08 May 2026 19:44:10 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 19:44:10 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 08 May 2026 19:44:10 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 08 May 2026 19:44:10 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 08 May 2026 19:44:10 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7dbcfa97a21e101dc0dd7e67e9acf1f130b75d0aad66b6c6df0fc06bd3a2b6`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 9.6 MB (9628168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586c844aca57bbdec889307dbbde44d190f3fae5f8b866548a431bcc2c157206`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 3.5 MB (3459166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb32b158822f4d9f318ff7589fe1bea03e35367ffc5e2ba3b3adc4454fb8d0a6`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96a9162070dccdd616a8537a06f33649a68622348f3751dede2b941c6e652ac`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 53.6 MB (53625366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b726c20d99572b79b55033a0de26e3d084692059676d889ea5c30b56d4122309`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 11.5 MB (11480291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d8d1eed87d8331d7f90fcf79641e3efd85f4e099ea867ccd0c5b36f51f207`  
		Last Modified: Fri, 08 May 2026 19:44:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0fb83f38502f5862b827d1e9206be7f1a70a33be92cfb7d14da8f18a2215ad`  
		Last Modified: Fri, 08 May 2026 19:44:23 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893feb67fdf4ec08ffe50bf77195628c9384cda475e0ab77c1161f11e6a26e7c`  
		Last Modified: Fri, 08 May 2026 19:44:23 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:d705309464bc789a261545d475a50b8789a0189571eeb175fdcbb66de7580892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5c7f7a695a82c73581521c62365c4457e9c2e2e3739d3cebfaa7a9cdb4aeda`

```dockerfile
```

-	Layers:
	-	`sha256:81e43af9c08246cf2889ca5dc9a4707aef336b21077a3925e87d08804af37416`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 3.0 MB (2958378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e18899f2c3b6533aff50a8c89d97034512a7346d2b0ecf91cdddfdb530e854`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json
