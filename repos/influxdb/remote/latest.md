## `influxdb:latest`

```console
$ docker pull influxdb@sha256:2958da2c8ecc64e5fde742c6b7a61c6bbc3c396eb461669f2c9068fff87ea23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:5abfe034ac6891fd8cdcd0df9978a4a0261afb2d73c1e5aec3522173c238215e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169188513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4af8075f1dfbd35acd95916b59a5b38313415f9974e2649ea7c7cb243a8b50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:54 GMT
ADD file:4bf66d4081da52e8b692fcff96aad84d3e68bda4f62e870e8f4803153c70e24c in / 
# Wed, 11 Jan 2023 02:34:55 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:05:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:05:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 Jan 2023 17:50:48 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 11 Jan 2023 17:50:48 GMT
ENV GOSU_VER=1.12
# Wed, 11 Jan 2023 17:50:51 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 11 Jan 2023 17:51:24 GMT
ENV INFLUXDB_VERSION=2.6.1
# Wed, 11 Jan 2023 17:51:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Wed, 11 Jan 2023 17:51:29 GMT
ENV INFLUX_CLI_VERSION=2.6.1
# Wed, 11 Jan 2023 17:51:32 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Wed, 11 Jan 2023 17:51:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 11 Jan 2023 17:51:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 11 Jan 2023 17:51:33 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 11 Jan 2023 17:51:33 GMT
COPY file:dbf3d010c7392537ae2b4c9b0d90a1ba01accd63948136585d5decc93bb52afc in /entrypoint.sh 
# Wed, 11 Jan 2023 17:51:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Jan 2023 17:51:33 GMT
CMD ["influxd"]
# Wed, 11 Jan 2023 17:51:33 GMT
EXPOSE 8086
# Wed, 11 Jan 2023 17:51:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 11 Jan 2023 17:51:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 11 Jan 2023 17:51:34 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 11 Jan 2023 17:51:34 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ac7f2e1c758675427623d0da4faa88b336c62466c15a98af61efd3f015282f2f`  
		Last Modified: Wed, 11 Jan 2023 02:39:26 GMT  
		Size: 50.4 MB (50448910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcdf7fce05b60278ea57279b4fd04f78778f80a6d64b6f875afc4bde32c2d1b`  
		Last Modified: Wed, 11 Jan 2023 03:13:10 GMT  
		Size: 7.9 MB (7859410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed0c2752d8478245519a7aab5e660053796af3c7ea7b34ad3df855b33ff5502`  
		Last Modified: Wed, 11 Jan 2023 03:13:09 GMT  
		Size: 10.0 MB (10001385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48017590002e8716ceb43c70e063a7507c9fb72448df11f9c69fa04bc0eb68bc`  
		Last Modified: Wed, 11 Jan 2023 17:54:09 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fe1f7c98ab28877706d5ee8210f401fcb074ab8d84e3f3b323571e3267b066`  
		Last Modified: Wed, 11 Jan 2023 17:54:09 GMT  
		Size: 961.0 KB (960962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdae51f5affc73a6549fc4c6e4e80303e85cafc843ab07965aa79fc61d86de2`  
		Last Modified: Wed, 11 Jan 2023 17:55:02 GMT  
		Size: 93.7 MB (93699451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926b710fc45102c4fd22f718845aa25abd62a1677f0beae8fe824dbfa2e49b`  
		Last Modified: Wed, 11 Jan 2023 17:54:52 GMT  
		Size: 6.2 MB (6210925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75f549d66d8fd9e4773016007add2e4171c0f6bf532e3525c3ac4407db2a4b7`  
		Last Modified: Wed, 11 Jan 2023 17:54:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c9bf5ace6f75dba7e8e165d87c9d74cda203919adb4ff9b6e2719fc73fe75b`  
		Last Modified: Wed, 11 Jan 2023 17:54:51 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dce1f756a322d61f554bfde2e704a69f33a8dc70420f7bb3f97f233bf91aba`  
		Last Modified: Wed, 11 Jan 2023 17:54:51 GMT  
		Size: 5.1 KB (5131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:750f7ade153ce2c99e6a718d63a82e6ef50c9b80edf08de87406a128725d0ef0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94794365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d965327ac4600487dce1bd0b2306373fc5b4ec9127b5274a7a4ca06c614dc065`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 15 Mar 2023 23:41:07 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Wed, 15 Mar 2023 23:41:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fLo /usr/local/bin/yq "https://github.com/mikefarah/yq/releases/download/v4.30.8/yq_linux_${arch}" &&     case ${arch} in       amd64) echo '6c911103e0dcc54e2ba07e767d2d62bcfc77452b39ebaee45b1c46f062f4fd26 /usr/local/bin/yq' ;;       arm64) echo '95092e8b5332890c46689679b5e4360d96873c025ad8bafd961688f28ea434c7 /usr/local/bin/yq' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/yq &&     yq --version
# Wed, 15 Mar 2023 23:41:09 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Wed, 15 Mar 2023 23:41:09 GMT
ENV GOSU_VER=1.12
# Wed, 15 Mar 2023 23:41:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Wed, 15 Mar 2023 23:42:03 GMT
ENV INFLUXDB_VERSION=2.6.1
# Wed, 15 Mar 2023 23:42:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2_linux_${arch}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Wed, 15 Mar 2023 23:42:07 GMT
ENV INFLUX_CLI_VERSION=2.6.1
# Wed, 15 Mar 2023 23:42:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}/influx" /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Wed, 15 Mar 2023 23:42:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 15 Mar 2023 23:42:10 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 15 Mar 2023 23:42:10 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 15 Mar 2023 23:42:10 GMT
COPY file:595a669a2c2c2f47df93700fcd3e412750aae40abb979bb4af48a89af97a8b72 in /entrypoint.sh 
# Wed, 15 Mar 2023 23:42:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Mar 2023 23:42:10 GMT
CMD ["influxd"]
# Wed, 15 Mar 2023 23:42:10 GMT
EXPOSE 8086
# Wed, 15 Mar 2023 23:42:10 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 15 Mar 2023 23:42:10 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 15 Mar 2023 23:42:10 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 15 Mar 2023 23:42:10 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fd6db03d5e7efd9c898c05fa431254e6753c9d39caf9a942d187e791ef698e`  
		Last Modified: Wed, 15 Mar 2023 23:42:58 GMT  
		Size: 6.3 MB (6308600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623e77e647b06d59d840fce37c059b20aa366a51af80637fd63e1e5512a9e5e6`  
		Last Modified: Wed, 15 Mar 2023 23:42:57 GMT  
		Size: 6.6 MB (6643045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316c8eeb27a0e8e1b5c0adabd0c1c7a915c9dfda919151dea2c1f0fbd9b5b8d`  
		Last Modified: Wed, 15 Mar 2023 23:42:57 GMT  
		Size: 4.1 KB (4124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed509fbb0848d068923c7c2fb0326172783db14b7e706111aa8d36fef0724e1`  
		Last Modified: Wed, 15 Mar 2023 23:42:57 GMT  
		Size: 916.9 KB (916930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9f815af9fa7713836edcaf8c0edfede3b00c2f262af85dee43e3bf5706a89`  
		Last Modified: Wed, 15 Mar 2023 23:43:53 GMT  
		Size: 45.1 MB (45145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e98fd076597f7d2ddfa0871be33a56e936d19752c20858efc5f76b0fe57e03`  
		Last Modified: Wed, 15 Mar 2023 23:43:50 GMT  
		Size: 5.7 MB (5706001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e1b9223729f0d3aebccfacb5a0b15c96af102a78398ac8b0df5cfa5329e7ed`  
		Last Modified: Wed, 15 Mar 2023 23:43:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc31e1ada9713c6aa0ae771c2ff4a99aeaa09bcd46114941d005d37a165d5c8d`  
		Last Modified: Wed, 15 Mar 2023 23:43:49 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f654e5c408f27396570fc3ebb1bfee8bd77d4e2f82a808aa4ce8cd861ff0af`  
		Last Modified: Wed, 15 Mar 2023 23:43:49 GMT  
		Size: 6.5 KB (6463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
