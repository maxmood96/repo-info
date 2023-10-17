## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:c96cd67e9171a9f4055f77d5be1826060ee976065775fa747efb76855a9a054c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:04c0b7957462f84bef8eb19e07d42a07e2ec7d9cd42547f0236efaedcc958e82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88175666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cc99515bfd31730349b0c6c2aa018e2b71dbbcaeed22e515c9720baa3f4507`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 17 Oct 2023 01:31:11 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Tue, 17 Oct 2023 01:31:12 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fLo /usr/local/bin/dasel "https://github.com/TomWright/dasel/releases/download/v2.1.2/dasel_linux_${arch}" &&     case ${arch} in       amd64) echo 'e4b43d8c7d76904e2401dc81de0900d9cb69b006794ff3901ec5d50e96baa8ef  /usr/local/bin/dasel' ;;       arm64) echo '92b83f30949679197403ff7a7e0f9ef3e458c1c55031d9c1bc112364e487d57d  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 17 Oct 2023 01:31:13 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 17 Oct 2023 01:31:13 GMT
ENV INFLUXDB_VERSION=2.7.1
# Tue, 17 Oct 2023 01:31:16 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2_linux_${arch}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 17 Oct 2023 01:31:16 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 17 Oct 2023 01:31:19 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 17 Oct 2023 01:31:19 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 17 Oct 2023 01:31:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 17 Oct 2023 01:31:20 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 17 Oct 2023 01:31:20 GMT
COPY file:0c651d5752d62a8235f9939458cdfe0447d6491e071a852d95bf87ff7179f6a0 in /entrypoint.sh 
# Tue, 17 Oct 2023 01:31:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Oct 2023 01:31:20 GMT
CMD ["influxd"]
# Tue, 17 Oct 2023 01:31:20 GMT
EXPOSE 8086
# Tue, 17 Oct 2023 01:31:20 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 17 Oct 2023 01:31:20 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 17 Oct 2023 01:31:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 17 Oct 2023 01:31:20 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5352bf3aec614dde8ac36d38f28f5021eff4c2ff0226eb22dfa667f2b2add1`  
		Last Modified: Tue, 17 Oct 2023 01:33:20 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1571fe6e896787a9ed8a94a131ff6ea2380ac23074890f6eca0b0508ce78e4b3`  
		Last Modified: Tue, 17 Oct 2023 01:34:04 GMT  
		Size: 8.9 MB (8868212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39440e9faa9e55df70138260c3e8deba8040a52aa612269873118811755dac7c`  
		Last Modified: Tue, 17 Oct 2023 01:34:04 GMT  
		Size: 6.4 MB (6434122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713e365c08429ef4ca6fb360291a58e51a44a15f206de8851ddf86ab4c827d31`  
		Last Modified: Tue, 17 Oct 2023 01:34:03 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e560edeabee9c70ca41d001cb434a9fd3134d7f465d53ba2c547ceedbbad6c`  
		Last Modified: Tue, 17 Oct 2023 01:34:07 GMT  
		Size: 46.3 MB (46334318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da414ee54fa983ef0ed4a2b6575527c74d280b816cde8bed0ac0f29769f2652`  
		Last Modified: Tue, 17 Oct 2023 01:34:03 GMT  
		Size: 23.1 MB (23128350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ca1ef9a7cb145b26c46906197351b576b7f4004e7121564d212e1907429f2d`  
		Last Modified: Tue, 17 Oct 2023 01:34:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7706e83932be29da21b99b1be7b75789b1af15829aa6c74510aa06bd65eaa704`  
		Last Modified: Tue, 17 Oct 2023 01:34:01 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d630755bf25b47905695c5035e2fd23f6bdbe41b2821bb851a67c6785ab92876`  
		Last Modified: Tue, 17 Oct 2023 01:34:01 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:678580d8acc8a983b3cb57aa9435e3010c9e6ab95fe7303481947c6934132a67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84354940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2183d7219e1a410cad9db4ca5730de79d202bddb1d362e7fbcf95381346330c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 17 Oct 2023 00:43:53 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Tue, 17 Oct 2023 00:43:54 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fLo /usr/local/bin/dasel "https://github.com/TomWright/dasel/releases/download/v2.1.2/dasel_linux_${arch}" &&     case ${arch} in       amd64) echo 'e4b43d8c7d76904e2401dc81de0900d9cb69b006794ff3901ec5d50e96baa8ef  /usr/local/bin/dasel' ;;       arm64) echo '92b83f30949679197403ff7a7e0f9ef3e458c1c55031d9c1bc112364e487d57d  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Tue, 17 Oct 2023 00:43:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 17 Oct 2023 00:43:55 GMT
ENV INFLUXDB_VERSION=2.7.1
# Tue, 17 Oct 2023 00:43:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2_linux_${arch}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Tue, 17 Oct 2023 00:43:59 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Tue, 17 Oct 2023 00:44:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Tue, 17 Oct 2023 00:44:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 17 Oct 2023 00:44:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 17 Oct 2023 00:44:02 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 17 Oct 2023 00:44:02 GMT
COPY file:0c651d5752d62a8235f9939458cdfe0447d6491e071a852d95bf87ff7179f6a0 in /entrypoint.sh 
# Tue, 17 Oct 2023 00:44:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Oct 2023 00:44:02 GMT
CMD ["influxd"]
# Tue, 17 Oct 2023 00:44:02 GMT
EXPOSE 8086
# Tue, 17 Oct 2023 00:44:03 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 17 Oct 2023 00:44:03 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 17 Oct 2023 00:44:03 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 17 Oct 2023 00:44:03 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc059a59f82bcb99dccb07e78bca560aa59ed7395b4e1aca88e17625928caac3`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 9.0 MB (8962246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6a92e4aeeabe0db41582e915d546ba0cdf83b3fa3b763d525457048749a9c8`  
		Last Modified: Tue, 17 Oct 2023 00:44:21 GMT  
		Size: 6.0 MB (5953765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e150933dfc1e072cfad77c042576074dad28047c0f9048064040a3bd04052307`  
		Last Modified: Tue, 17 Oct 2023 00:44:20 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e439624cf2dc8a873c9a70554bec9f5c6e968b8ceed262a2ecce5eb54569ae`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 44.4 MB (44435810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec856ad98375f36ffe64f3e6f1a78a9ff290a83e82a38be8bf1ec21e7f89029a`  
		Last Modified: Tue, 17 Oct 2023 00:44:20 GMT  
		Size: 21.7 MB (21662592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c061063415fd5aad1f82f01a5cff14a6737c2813c731bd8a75304a7734b1fbae`  
		Last Modified: Tue, 17 Oct 2023 00:44:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c5566f54510d1c770c00bdfadd4a8e3fe6b5570a4835924edca017964d2fd6`  
		Last Modified: Tue, 17 Oct 2023 00:44:18 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd11ead2c8b13ec8fb165570327a1601416e1822be27b668b79b1ac6cce9bb9a`  
		Last Modified: Tue, 17 Oct 2023 00:44:18 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
