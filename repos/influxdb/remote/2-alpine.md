## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:d948cd7aa274696d76ccc3f7ef732180d9f9a4229aace3cf68ae008693665137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5ab58e6acde4a641694f7a2e6671a9f39921f3b8200e7cb04153599ff24a0171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81511579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcb7b71c691969ff5b9884bf92ef34f16ca26efabcfb7fbd6d0ada332fe1458`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41588b948a36335f02b1fe372411528fc71bf105e403c9b8476eaed4bc61b296`  
		Last Modified: Tue, 15 Jul 2025 20:47:40 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c40e86352d8732707283812cf31b4cb48410b4d43bd9a1ea799b969178e28`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 9.8 MB (9819933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124accecbf9a5d3fa58778cf7d727740b1808d84760e163ecbfe05c76fde911c`  
		Last Modified: Tue, 15 Jul 2025 23:20:58 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02be05aac4069c435b4c30f7102f4fef9d496612908c506d00a74fe121e992b`  
		Last Modified: Tue, 15 Jul 2025 20:47:43 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aba977cca3a9f384b93f852720b3fdb29821d9601ec5402b7fabb7b84ed188`  
		Last Modified: Tue, 15 Jul 2025 23:21:07 GMT  
		Size: 50.1 MB (50115466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e18b3dde9d2ebba50fb26deb3e132dbff7bce833d3dec715b997305f4b7ead`  
		Last Modified: Tue, 15 Jul 2025 23:21:00 GMT  
		Size: 11.8 MB (11773676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a605a3944855fed4b0dc37407f21364b863d736d62e512592c17f37614f634b`  
		Last Modified: Tue, 15 Jul 2025 20:47:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144ed5ee0ead4cb9ab07f97753eff4055313e54d6469a9a22feb04cc627f5b6`  
		Last Modified: Tue, 15 Jul 2025 20:47:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05126e91032baacdbb215f10aae69bd77e06da4add32161c42104ad83744d068`  
		Last Modified: Tue, 15 Jul 2025 20:47:55 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bce540c47d1075fe3bc1f3a18410f096d9a73701106a04b8724a850baa2a7e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9814dc0d960e1dd48ab16ce3799261d16c65d82603d5e8c7d98111eeac6cb7`

```dockerfile
```

-	Layers:
	-	`sha256:6d325d7ce69647356cfcce291f65ab689996946f197ffff1db072b832f421271`  
		Last Modified: Tue, 15 Jul 2025 23:20:47 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba6a4bbacf5ac36dfae6df2b86429b3103a25fc72709e829c3ba8afe8cf53a8`  
		Last Modified: Tue, 15 Jul 2025 23:20:48 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:328a4a0ffd4b2631ebbf3b75b62e14f3ddee93b48bca78be21da8f0fa818a823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78683906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d78e27ffcd6dd1fce93b95dcaddaa6c654dc6e7e6ee859bafc1df18b61481f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 03 Jul 2025 17:46:22 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 03 Jul 2025 17:46:22 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 03 Jul 2025 17:46:22 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 03 Jul 2025 17:46:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Jul 2025 17:46:22 GMT
CMD ["influxd"]
# Thu, 03 Jul 2025 17:46:22 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 03 Jul 2025 17:46:22 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 03 Jul 2025 17:46:22 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600bb37154aec80b9f15e982c92a4e37ba42feeb4cc42826f6add6b7fb79ad89`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1672beef7b2cc4b76db6451487d605bebd392e9d0f8c39b48d43cd4f0aba306`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 9.8 MB (9783360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529e7bf79faa4c179f30c08b6771dac030c31ecdd63018c7651338afdae27e3`  
		Last Modified: Wed, 16 Jul 2025 00:17:26 GMT  
		Size: 5.8 MB (5790433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e0f93130bfcea152418034fcf70f62c1b31b5edcf475d536ee84548219f449`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d60bf4032b74fcc73c1c56e254540e8960145dace3efcea4bd97297bd88523`  
		Last Modified: Wed, 16 Jul 2025 00:17:30 GMT  
		Size: 48.0 MB (48016245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d0c42d1d38a2397dde3e42086f8db8b36e263f884f0ce8262e26b056739eb`  
		Last Modified: Wed, 16 Jul 2025 00:17:27 GMT  
		Size: 11.1 MB (11098981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6bb2ad4fede2ef39df25c988f059baf0bb037f19a4120a3d05e07cc1bda614`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9162549b851b3e4b3fa90cbc20f18519037f21bc774bb33be16d4d12d3c8d7`  
		Last Modified: Wed, 16 Jul 2025 00:17:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c7cb76b0374befb4a7b810686ef1d646abcb15428a55630c40d2bb6535310`  
		Last Modified: Wed, 16 Jul 2025 00:17:25 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cd7717fcd61869be57b993a9722525fd3640ca6c52d336aff4389c12cfa83d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ba9a3b2a06597910ffc721dcc16534874f8b6068066a163f2298bf924c6ca2`

```dockerfile
```

-	Layers:
	-	`sha256:2e4eaed119ab9bd7fb9ec406598f4850075f76a7dc60d7ae0ec0cd6ad73111a4`  
		Last Modified: Wed, 16 Jul 2025 02:20:35 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b6129a43b1892d4bc0921a75ca680f9d9266e51b357532a467764c49c8f244`  
		Last Modified: Wed, 16 Jul 2025 02:20:36 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json
