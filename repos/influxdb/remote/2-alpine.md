## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:a7a9e96c9bfc443a79d13e2b1989dc43608eb5b6c06fec6d30651ca5f8219330
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cbee5988f47dfa92bea7f72ff9e0fb07ba7956ead0141dc2ab27245b31f4f105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92785945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ade717ac7e624b9847ff64fa2b0f29775c53f8ea1418f8ec9c486ffc444719a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b4da6257d4dab81f7ea9b217e8990fa02b532b487dc09f66cfe66b7a5ab1b7`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227616a4b65630020272b1a4736c45d2072fea1f6ae56d8987f001bff1868e5`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 9.7 MB (9668254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28153e71486f54b7e2d6898878271446058952c9919aaad4310fd5662e14073`  
		Last Modified: Tue, 03 Jun 2025 13:35:12 GMT  
		Size: 5.8 MB (5820951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17da966601b69ee27cf7e07f71e8d3a293465f510f662a95761c204c476039`  
		Last Modified: Tue, 03 Jun 2025 13:35:11 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f351545292c8d4b32b561f37f2761b8143e35ea7b2aed6ada764d91675953e2`  
		Last Modified: Tue, 03 Jun 2025 13:35:16 GMT  
		Size: 50.1 MB (50115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec39c678e278ff055d4d22e8402129df928caa4a2647ff3024e97721f0f5943`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 23.5 MB (23546414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428d400809cb7ad31d35a7f2d948c8121b3f7499c617f94eb95080f6705d2c6`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195b609b670962adf4a4fd55112b8f3ee09ab9b864b63db78893c7e7b6de06aa`  
		Last Modified: Tue, 03 Jun 2025 13:35:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bcca749f51ef7f5ebe65ef3ee91941b8ead606c2179e2247bba98e5d1ba1`  
		Last Modified: Tue, 03 Jun 2025 13:35:14 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:07a190e7a4e44a2d2349ddf22bcf6a411cb327788d87cbe24dfbfb319e2346ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.5 KB (949513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0face7c412448d24ef27a189fc81813532f5930f3f6a820e3311b431cb71a2`

```dockerfile
```

-	Layers:
	-	`sha256:dc8858c4baeaf5b780566e1f56dac4769e4c5fb4a00452d59c94970c80b6638d`  
		Last Modified: Wed, 04 Jun 2025 00:38:08 GMT  
		Size: 918.5 KB (918468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15b588c6b6124a1aa918ae48f879aa8e721ecd2db834e3c78af76a20738c283`  
		Last Modified: Wed, 04 Jun 2025 00:38:22 GMT  
		Size: 31.0 KB (31045 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:acd117211c431790fc6d016c91eec85d13c132bf2179149dd9c1163fd5b36f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89567348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25c6a394b54e0d7afd6e4960b11cc3c7389d6a99abd4edc658192b2ed4782b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 21 May 2025 19:23:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 21 May 2025 19:23:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 21 May 2025 19:23:38 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434c8ed1b411bf87e31d51dcd5e11ad29b842c6ac23d29867f58c9b6657217f9`  
		Last Modified: Thu, 08 May 2025 17:16:04 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7581744a5f8b851a37b006b9f70c0dfc1aabfbbf6e54e0d468d11332b9a89155`  
		Last Modified: Tue, 03 Jun 2025 13:33:06 GMT  
		Size: 9.8 MB (9790275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8e2420533fb94a98c3c0cea702d65af3aac200564d71bf02039933d45752c4`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 5.5 MB (5463798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d98ff612225a614c58f5f650b55a20d2a5f607933c56ec0b343dc54d39316`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9943be5d4ecac40794357058ec1ead2ffe57b93ad82f1c046f9490950fb8be`  
		Last Modified: Tue, 03 Jun 2025 13:33:07 GMT  
		Size: 48.0 MB (48016208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592941019971dc33dba5c666bebc57139662a00acd86e6dc6e85310542b62a90`  
		Last Modified: Tue, 03 Jun 2025 13:33:08 GMT  
		Size: 22.2 MB (22197933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a652dc6c421b2c1298eb71f3a1a77ad5317359d42f97d2ba7e0256166f7908`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c5c55779859032454928168c0eaf5620289e22d09443a4c303e920fbc0f25e`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c5a87a5ee69568a4bb3e3c7fbcb83b0bd9250e68ef8618525ab0df87a7c0`  
		Last Modified: Tue, 03 Jun 2025 13:33:11 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:729a0121b69401596161e2c26bec6508731ab99a75514774f24c6af6bfc18323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.0 KB (948960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c122a9ee58ab54b906e11b0f4efc6fa24ec9862171d48194a1c13655341895`

```dockerfile
```

-	Layers:
	-	`sha256:5f2a9ab7569906dc8b16cb3c30fa1f29afe85dc187f764fa5f1821fc5d6848ec`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 917.7 KB (917719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4f5e2584d7feb4ec7fc289bad890abb4f9f813f7c20ca231fb580b0db01d6d`  
		Last Modified: Wed, 21 May 2025 21:02:35 GMT  
		Size: 31.2 KB (31241 bytes)  
		MIME: application/vnd.in-toto+json
