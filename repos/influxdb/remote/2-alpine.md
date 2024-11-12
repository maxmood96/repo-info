## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:d0b9d5b8df3b6edca8e232d0a028b01de4b00a20bf87d2d159ec57ce482c7f02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:016696f871af9501d2bc8de125412ea11d6b06255c94b7072116ff9bdbf75565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92447366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c1600abc60dd628161036525341fdf5f9bffdd371e2f579beaaca306c6bab9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXDB_VERSION=2.7.10
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Sat, 26 Oct 2024 00:18:17 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 26 Oct 2024 00:18:17 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 26 Oct 2024 00:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 26 Oct 2024 00:18:17 GMT
CMD ["influxd"]
# Sat, 26 Oct 2024 00:18:17 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 26 Oct 2024 00:18:17 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 26 Oct 2024 00:18:17 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca4e78c51cf4f32aee0112b39eee90ec5adad51bf06d230cf84703a7c6d95`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58b67e284d401e7fd4d54596f90f54c3cdd037874acc84cb4f8077d1702a9e9`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 9.7 MB (9657640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c539d32573f2c3a568d8156ef3011bf685fb1ae318fc0e22b00b8c5af5da06`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 5.8 MB (5820948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69a09b073184b319d09b27a4a9ffd399f213b4f726be4aa212abf8875f42080`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30b2a00406ce3e77a88383b59693aa6cf6964e5e5a40889f5b3c7bf5563495a`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 49.8 MB (49790503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b47d751c1de460253085b2b61ce94f5c4b6c2fba2aec50ddc52c75ec5697c38`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 23.5 MB (23546399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61e966ba5d507be2689f099daab5a6d576aa8ce6b913d29d5241116f14e68f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8df45b28aaa2017245994d083bc1c4f4c458a94ad4d15fd70700bf13ec6ca8`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ae1b04c1b23614536b52471d7a6c4f80897a884d06a9979559eeca7ff1eeb`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a5f3b51d4f67e7f4944706ce0671151da9ed28c56d76261b6e75550f7decea16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.6 KB (945575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d4fd40043261f88c2e90979cbb077235817d36456620aaf121c7562f4f6904`

```dockerfile
```

-	Layers:
	-	`sha256:fcf01541daa9f52095830599da571f955b900cce93bf6a02a6eec5c47799166a`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 914.6 KB (914627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b910bcc341ba0f74ad9281164a23e1c102c09a5aa16cfd7a2d21069a13c536c`  
		Last Modified: Tue, 12 Nov 2024 02:14:03 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:01d0fcd91674b394d26ef8f1eec9c475b7f403cf10257ebaed77ec26145856ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89244002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb389848654e8f0ea7f36e3dfb29bf5e97ff8c54e33400209ee70a5fb81ded1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 18:38:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUXDB_VERSION=2.7.10
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 22 Oct 2024 18:38:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 22 Oct 2024 18:38:37 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deeb5bb87a9b047197ab047408d669771534ddd651ad86d0935717add352c29`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad71f843ccedd874c5468e97b4b7c17395262d7353e4ed6006aba08e18fae887`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 9.8 MB (9777142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a3e38e2ffb00f3e4786fdd01dd079eda34b3f65d8a05db74836f3739c0c8d1`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2def60e9aeb441cfc22ae4a5c007f86e41791863e6784828ec74390badf73a`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ea43a5fa5d50a03fbdbb5319d38071b43fd93879cfbb15f62721f491a347e4`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 47.7 MB (47709532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047065b1bd569a1dee11f1813ce0051a11c7472c7d35e711609ecc2cbe7ad5d`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 22.2 MB (22197917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9468215c53e8a896f9b934d83b0d0768f4e0e81441f0d8c5add921b1174d2`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a140ff0494c018fe34ddb0023fba7f95c40cf6201e1696fcec6901da350da6f0`  
		Last Modified: Tue, 22 Oct 2024 19:55:42 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae45bb58db1b991a86bfe2c36cc8a55c4a9edcfbff715ebbab68907c6fc408`  
		Last Modified: Tue, 22 Oct 2024 19:55:43 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:5557d1011f8db6c8306114ebdb7f1caf2d969f06efc2b66ee34bb61b1fbb78a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.9 KB (944862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed25776500d61570cd6a6deb6a7b8e1855d3e69d44483c688c9a45185ca50ac6`

```dockerfile
```

-	Layers:
	-	`sha256:3af9a32ee0668a6af608337bcddbecc855029efd69933e9046f36682e84a2ad9`  
		Last Modified: Tue, 22 Oct 2024 19:55:41 GMT  
		Size: 913.9 KB (913888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3370bfe3452a6e94532bb5823680a91661f51f027ee384f8ab7db7f969d8ea`  
		Last Modified: Tue, 22 Oct 2024 19:55:40 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json
