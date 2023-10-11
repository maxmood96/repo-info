## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:7b89691514a7ddc6bdd327821f7985adb176311d4278cead5d81fec17582d016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d9b30a86a46a5d5b7656c1d1f7211698a8b6feb72613f61dcf014a9c8dedbb7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88175650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6375c4167854d18f672c27e6ea737f21adb881782d15b95fa2c0edf31703c06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 11 Oct 2023 18:16:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Wed, 11 Oct 2023 18:16:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fLo /usr/local/bin/dasel "https://github.com/TomWright/dasel/releases/download/v2.1.2/dasel_linux_${arch}" &&     case ${arch} in       amd64) echo 'e4b43d8c7d76904e2401dc81de0900d9cb69b006794ff3901ec5d50e96baa8ef  /usr/local/bin/dasel' ;;       arm64) echo '92b83f30949679197403ff7a7e0f9ef3e458c1c55031d9c1bc112364e487d57d  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 11 Oct 2023 18:16:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 11 Oct 2023 18:16:46 GMT
ENV INFLUXDB_VERSION=2.7.1
# Wed, 11 Oct 2023 18:16:50 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2_linux_${arch}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 11 Oct 2023 18:16:50 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 11 Oct 2023 18:16:53 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 11 Oct 2023 18:16:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 11 Oct 2023 18:16:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 11 Oct 2023 18:16:53 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 11 Oct 2023 18:16:53 GMT
COPY file:0c651d5752d62a8235f9939458cdfe0447d6491e071a852d95bf87ff7179f6a0 in /entrypoint.sh 
# Wed, 11 Oct 2023 18:16:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 18:16:54 GMT
CMD ["influxd"]
# Wed, 11 Oct 2023 18:16:54 GMT
EXPOSE 8086
# Wed, 11 Oct 2023 18:16:54 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 11 Oct 2023 18:16:54 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 11 Oct 2023 18:16:54 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 11 Oct 2023 18:16:54 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779175f54086809f96dd5b117ed71f84dd847e86676070c520eaf459fa4e08a`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce4cd93cabfcc5506735509a75bf9f1dc63c85fb5e24446b5c1c0687197cfb2`  
		Last Modified: Wed, 11 Oct 2023 18:18:55 GMT  
		Size: 8.9 MB (8868224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2872f0f5121b8978ca9df2a5a78f7c36163a5e51283ef3058ad6ab6b24d26d45`  
		Last Modified: Wed, 11 Oct 2023 18:18:55 GMT  
		Size: 6.4 MB (6434122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fafd66db47354d2964c67f1b8e8f74bca944250acbc6c3c3a2acb48d50f8e9`  
		Last Modified: Wed, 11 Oct 2023 18:18:54 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5257e686e243a480319f5175e5be066447b560e3a0ab27e4460844224ca084`  
		Last Modified: Wed, 11 Oct 2023 18:18:58 GMT  
		Size: 46.3 MB (46334298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4739eb28eb05ea7bfc80c240441454a4d983a5adf6b5a81608c6e244e767ea7a`  
		Last Modified: Wed, 11 Oct 2023 18:18:55 GMT  
		Size: 23.1 MB (23128347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4c415b53c29bc3e99268f5cfbe7c0bcddfdbadd4e0b501f8436e3108aaa05f`  
		Last Modified: Wed, 11 Oct 2023 18:18:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bd3a08485b3472163cc1e9376fd350a70abba8941939bfeb5c4f5211c97f84`  
		Last Modified: Wed, 11 Oct 2023 18:18:52 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10dfd2bfe06447b59143cee5f094397c3ba9bb379db23485d7cf40485cfcb930`  
		Last Modified: Wed, 11 Oct 2023 18:18:52 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:afe04df584b9a4f2b00e93b553bfba61785c1f189dc502b793c466c1689a4cca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84354949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ccae2b84a3e585ddc95a93a861d98cc0c58387934cc9ed6820fab70bd6ed74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:04:12 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 11 Oct 2023 17:39:49 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates
# Wed, 11 Oct 2023 17:39:50 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fLo /usr/local/bin/dasel "https://github.com/TomWright/dasel/releases/download/v2.1.2/dasel_linux_${arch}" &&     case ${arch} in       amd64) echo 'e4b43d8c7d76904e2401dc81de0900d9cb69b006794ff3901ec5d50e96baa8ef  /usr/local/bin/dasel' ;;       arm64) echo '92b83f30949679197403ff7a7e0f9ef3e458c1c55031d9c1bc112364e487d57d  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version
# Wed, 11 Oct 2023 17:39:50 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 11 Oct 2023 17:39:50 GMT
ENV INFLUXDB_VERSION=2.7.1
# Wed, 11 Oct 2023 17:39:53 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2_linux_${arch}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 11 Oct 2023 17:39:54 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Wed, 11 Oct 2023 17:39:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 11 Oct 2023 17:39:56 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 11 Oct 2023 17:39:56 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 11 Oct 2023 17:39:56 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 11 Oct 2023 17:39:56 GMT
COPY file:0c651d5752d62a8235f9939458cdfe0447d6491e071a852d95bf87ff7179f6a0 in /entrypoint.sh 
# Wed, 11 Oct 2023 17:39:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Oct 2023 17:39:56 GMT
CMD ["influxd"]
# Wed, 11 Oct 2023 17:39:56 GMT
EXPOSE 8086
# Wed, 11 Oct 2023 17:39:56 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 11 Oct 2023 17:39:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 11 Oct 2023 17:39:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 11 Oct 2023 17:39:57 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945e94244715004b6f7ade3a66bcfa884d346f67af67149978de9ea31611ad82`  
		Last Modified: Fri, 29 Sep 2023 01:04:49 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed6b2bf8df78aec226f3aabbecf80dc45f50851d5a3c5bf947ac2fca1423e9a`  
		Last Modified: Wed, 11 Oct 2023 17:40:31 GMT  
		Size: 9.0 MB (8962272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de496dea77ac3a07bd1717e18272323937fe7eef25bf35fc2f6fdae112e09d5f`  
		Last Modified: Wed, 11 Oct 2023 17:40:29 GMT  
		Size: 6.0 MB (5953753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128eea8cd913f3a9ada1edae33dd201c315e4ae21adea75c6732d9a6437c4a9e`  
		Last Modified: Wed, 11 Oct 2023 17:40:28 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e63587c42f2eee28580b402c8c13c69ef5cb25cc654f0c6a8de4e1c528ffdff`  
		Last Modified: Wed, 11 Oct 2023 17:40:31 GMT  
		Size: 44.4 MB (44435825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6430d137c72244cfbf5b71a0c48e3c927dbc468a39a02b047b0065a1d56ec132`  
		Last Modified: Wed, 11 Oct 2023 17:40:30 GMT  
		Size: 21.7 MB (21662574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84afdd387ea37a00cb649ed6828f618fe2fea868f3dcc592a2b86a2527bd105d`  
		Last Modified: Wed, 11 Oct 2023 17:40:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd441b6011344762f1706ac9995fb2d292843045db75f04fbe7cc55088f647f`  
		Last Modified: Wed, 11 Oct 2023 17:40:27 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4380876f7e16c599d0804f6d696ff74038ce2813d95363afd12e156da4d1b82b`  
		Last Modified: Wed, 11 Oct 2023 17:40:27 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
