## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:fb537cf0d57937a57eac33efd079ae5b36a1d35437dc1eba1ecb8800a352b62a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2e03ae8e0b59c4a7b060238e4246b8a003c7b429019bdce39c024b1d5b056afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81890627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926890384ff7b559be8bac4f1e03f0d4ee3ca31ece6f2d938f483b97131ce363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:47 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:48 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:48 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:48 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:48 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:48 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f7056aa72ef8463a31e6afa1dec61d746d3cec587e13de9bcf28396caa037`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d56024c76d43582ac2f12311746a23ad83f148c5b42da7c957da34b6cdac498`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 9.9 MB (9862216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71475ef0f8f2c5f8c394cdda52333392709fc87e769397a0389fb1bb743d399b`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315475c1c17f7a223ea2b8a1d9a1985ce438a3bae2dae153555a5d457b051c1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9021d0ef61725243ae72546a2a75243c5424fa7d0fc53f20c469d377cba3`  
		Last Modified: Thu, 11 Dec 2025 21:22:01 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c548f8f09a0ce506a8c2e69d75de76926e996dfe9a46448c756d6647e8a04c`  
		Last Modified: Thu, 11 Dec 2025 21:22:08 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e504a5513a054282de4e3d4006c910c7003f8804e45058cf073a0422f0212d1`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d818200c6c4e7df4884a358b6f80bca9c959914eced87214ae2c44e58fd35b`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d217bc1e57c2c30506373ba1fe825b2fe61e5f1ae8585753f0ea1989f9c9f31f`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0843ea7d0b590a344252c4735a3b5c3259175326169b796c7863dc7e9409fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25347cf7627bd9599b9ab13a522f86bc1aeca3a4ebde0a65a1049914e53760c1`

```dockerfile
```

-	Layers:
	-	`sha256:94e7f5d4397e9c4d837b19c5727041c7f199d84bee573cb60c1f76fbfe39e3f0`  
		Last Modified: Fri, 12 Dec 2025 00:20:41 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0679192f4161cc8a9733b5905a2517d3b39a4d0813431aae1e63606bfccd37e1`  
		Last Modified: Fri, 12 Dec 2025 00:20:42 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2b5c1683b2644bc0f3962b069552a6ee4e299162cce72dc8a18758ded5d40771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c8d9f31ecd07666432029fe547d3ee536ca6cb4dc83bd8ff55264e2f368cc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:28 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:29 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:30 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46991d2c4c48fd52d13891e1b5eb0777120c6d83d07fcc82f06c4340cfb6ba`  
		Last Modified: Thu, 11 Dec 2025 21:21:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af32475cc26ad10355d0ebd8d9c80f88c7f6c44bcf28115edc647d31b95f9884`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 9.8 MB (9822470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafcce51f3333786fe19ee810e7107ca5c17a1a11e4b278b34d6d8989811de7`  
		Last Modified: Thu, 11 Dec 2025 21:22:06 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b70514028425c28cf39d8baef11c310457123a628d37c437bd6661fbaad6e`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f20cada75ad84d27130c93e200a873f7b2f5078d5a2049be4894b3a568aa4`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 48.2 MB (48229359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea275cc0d43ac8b796329c90b2d0397003fdf129d2fa4b0c407b9ffb957177b`  
		Last Modified: Thu, 11 Dec 2025 21:22:11 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18f15a6ac7b5a0a7673d362af6cd43b52cfe07914127acffa738249bb566cd`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de188f5486eb8567f178074e890509083cc993bcfb3a37457dd2300060ec14ff`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abede7ea0d56bd3a18f4443dc825494ff3d4993f87fee95b61f6d3153eb3f702`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e77a7505f9f1c8c8b7b80194b833dd81001c9138a0903c7724960f3ba8ab3144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeb577948dfa768d82764b6865eefb8962787cd5730e3e137fed9cf5446383c`

```dockerfile
```

-	Layers:
	-	`sha256:cde75b715d9b30d5cfecd23a0bdfb9e19b4e7fa446afe27e1057910a31641dfe`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b4d294b1204d82261147c85c10da7d18f3fff5439e60155204f31729b2b191`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 31.0 KB (31039 bytes)  
		MIME: application/vnd.in-toto+json
