## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:c5fcf0f3e6fc4d30646666ce9466e5022f2d35ab30ee56fc254da7b00897ac90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

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

### `influxdb:alpine` - unknown; unknown

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

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:683574882337d89ba55b47ec2239c9304ffbdb2a9b5d500a4e10149d0ca3607f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89246784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6939dca89d326a57786860064203b8e7d1b373094a310fa5d27e6fe1cbbf35f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de63ce930d0f77f6402e61ee732ad4f784c59fd26df033bb1b7d6a0b87a2f4`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca3884ecb2e01cc65615fbe7048afa29c9c999de55aa88e1d6b387145dcd94f`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 9.8 MB (9779862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bfe4e135f18780a8d70c200e6244ef50d4311f2d786b210cce82c9afcf4b51`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 5.5 MB (5463799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cd5ee8b73fbef9d7556ef226315ce8a0aa6839f5120dad8b3c7c54ac9089b3`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581641f4c063dbaf1e6608dfc65fcbd8cf4d88834c016ff89bd1a60a5cff3b73`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 47.7 MB (47709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dfa20b1284e4022b9d82bb6648314f82cedeac1aefc7fb5eb6a449c3425040`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 22.2 MB (22197919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eefb802b10b14779184170266c3cdc56aa734880d5612242e2708507587d79f`  
		Last Modified: Tue, 12 Nov 2024 13:17:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6276080857087ce5c820eff3e3050daf134e85ce8a4b99cda5b1d0c863016`  
		Last Modified: Tue, 12 Nov 2024 13:17:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328ab936fb2b98bc25b20b1ce89e9db5116ac84e88abc2ba1f7adeaed3eb8968`  
		Last Modified: Tue, 12 Nov 2024 13:17:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a79f6e8d0e4c420a240b72bd4d1f88411ecec4dbcfd37f6a237d6d4b3786ccdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.0 KB (945031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64762a01a3fc2611c65a4ff9832a72540bd540b6908c89c2bf9bf0c6c270702`

```dockerfile
```

-	Layers:
	-	`sha256:f5a82395e10d447f3421cac787c8be250079fed545ae107342063bb886cb56af`  
		Last Modified: Tue, 12 Nov 2024 13:17:19 GMT  
		Size: 913.9 KB (913888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd070e7c1391a788b25bf86f5dd27f01597ce5b01a48117f40afcf4fbebed3e`  
		Last Modified: Tue, 12 Nov 2024 13:17:18 GMT  
		Size: 31.1 KB (31143 bytes)  
		MIME: application/vnd.in-toto+json
