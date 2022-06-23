## `influxdb:latest`

```console
$ docker pull influxdb@sha256:ca7c85bcfb9aed2e6a3b27c4bcff83d6a6f0743d6b7b1e3b7c8337d4dbe35201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:cced4803590d8958c34d1caccfe677ede1a78fb4aa81724937a3b28efd546fe1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255108505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2cc92a02625e5f9f2a083f88cba052766a8508ca6ba15873f954e94b4327167`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 15:18:53 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Thu, 23 Jun 2022 15:18:53 GMT
ENV GOSU_VER=1.12
# Thu, 23 Jun 2022 15:18:57 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 23 Jun 2022 15:19:36 GMT
ENV INFLUXDB_VERSION=2.3.0
# Thu, 23 Jun 2022 15:19:45 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 23 Jun 2022 15:19:46 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 23 Jun 2022 15:19:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 23 Jun 2022 15:19:49 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 23 Jun 2022 15:19:49 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 23 Jun 2022 15:19:49 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 23 Jun 2022 15:19:50 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Thu, 23 Jun 2022 15:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 15:19:50 GMT
CMD ["influxd"]
# Thu, 23 Jun 2022 15:19:50 GMT
EXPOSE 8086
# Thu, 23 Jun 2022 15:19:50 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 23 Jun 2022 15:19:50 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 23 Jun 2022 15:19:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 23 Jun 2022 15:19:50 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a014c92148934973210d840dc7cfed53e0afba38d839afaa48ed5150eae19af`  
		Last Modified: Thu, 23 Jun 2022 00:59:51 GMT  
		Size: 7.9 MB (7856631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ff1be7001d642a624409e2d5f90e7708ef7e6f1a75f4eb7362a9296e18d20`  
		Last Modified: Thu, 23 Jun 2022 00:59:50 GMT  
		Size: 10.0 MB (9997231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2be5f1f5e36b84c231e9344fbdad80d3d25b429d2173ae4413e80bb9219f2d`  
		Last Modified: Thu, 23 Jun 2022 15:21:57 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e83dddbe160e4867179c02b322db6077f1247b6e3873fcf5e775a58c7f79044`  
		Last Modified: Thu, 23 Jun 2022 15:21:57 GMT  
		Size: 961.0 KB (960961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d930ec052a194785e77f4081b979b5c3d9364f957f0b045123a098cb97bba5`  
		Last Modified: Thu, 23 Jun 2022 15:22:48 GMT  
		Size: 180.5 MB (180478673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07bf48ed2c02bd714a95aa87dd8b1e888876289d9e4a3011d9c3c3163a03a5`  
		Last Modified: Thu, 23 Jun 2022 15:22:35 GMT  
		Size: 5.4 MB (5366843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd172e175c267578d305141602fccd14a242548d8dd40f68bf61335b0f8de0e8`  
		Last Modified: Thu, 23 Jun 2022 15:22:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31207bc54f84d0cc3eff27ec791fd85db44f676e55c422adb21fffd3ea700f4`  
		Last Modified: Thu, 23 Jun 2022 15:22:34 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09205f425110e616664cfae2b543ef2c5e43dffb11313082bc27caa51b04abf7`  
		Last Modified: Thu, 23 Jun 2022 15:22:34 GMT  
		Size: 5.0 KB (5013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2baa682aed86638d87383b2a3b9abbbcfa35e62114086e9f5e8b683e2ca085d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253364693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0584bae5a57fb85b00457d29e3b73fbf861472d13a7be7b8e306b728bdf80fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 28 May 2022 00:40:49 GMT
ADD file:af879be34a7eccc177a3000eb8c45d5207bfbec108caf9be9d11c1a6620c376c in / 
# Sat, 28 May 2022 00:40:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:07:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:07:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sun, 29 May 2022 02:28:55 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sun, 29 May 2022 02:28:55 GMT
ENV GOSU_VER=1.12
# Sun, 29 May 2022 02:29:38 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)" &&     wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" &&     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 16 Jun 2022 22:09:07 GMT
ENV INFLUXDB_VERSION=2.3.0
# Thu, 16 Jun 2022 22:09:16 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 16 Jun 2022 22:09:17 GMT
ENV INFLUX_CLI_VERSION=2.3.0
# Thu, 16 Jun 2022 22:09:22 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 16 Jun 2022 22:09:23 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 16 Jun 2022 22:09:23 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 16 Jun 2022 22:09:25 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 16 Jun 2022 22:09:26 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Thu, 16 Jun 2022 22:09:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jun 2022 22:09:27 GMT
CMD ["influxd"]
# Thu, 16 Jun 2022 22:09:28 GMT
EXPOSE 8086
# Thu, 16 Jun 2022 22:09:29 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 16 Jun 2022 22:09:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 16 Jun 2022 22:09:31 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 16 Jun 2022 22:09:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:fadbed17b01e84815ca3018d3dc42670c3add65c67e7cc74d6bc477ae8425934`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 49.2 MB (49229054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5795076bf6e9bf96da71f2e31cbe91d3c49a17f211c5b0d33e032e095c5564a5`  
		Last Modified: Sat, 28 May 2022 11:18:22 GMT  
		Size: 7.7 MB (7719823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1eda3e266fa432ba8ae8ba25a5ad2fa4c5349ef2aa244612c89f990704c5b25`  
		Last Modified: Sat, 28 May 2022 11:18:22 GMT  
		Size: 9.8 MB (9767307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0f5443af812585848f35a0c394a1510e548db84651500f20b69c8fd177c0e2`  
		Last Modified: Sun, 29 May 2022 02:31:56 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74321fb0673e5200e61727207187742de353b576e99c069daa95938cbcc3c34`  
		Last Modified: Sun, 29 May 2022 02:32:19 GMT  
		Size: 896.3 KB (896336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d991e036fe38dc0a00285f4de2a8cdd495356e2fb7b38fdb25eef0cc8753f1b8`  
		Last Modified: Thu, 16 Jun 2022 22:11:03 GMT  
		Size: 180.8 MB (180792418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671788a7abfe0d76498592ee8a2c990727e58bcba3e1c2df5c9961d4ebe7bcae`  
		Last Modified: Thu, 16 Jun 2022 22:10:49 GMT  
		Size: 5.0 MB (4952639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b013b66a18033798f3d8a26ef2b2422e91a4b1bfa9851dc1e5a3f687810a08e`  
		Last Modified: Thu, 16 Jun 2022 22:10:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f95ffe9fb81cf4aeeec17a092db313ac1671992f39e321c692da34db7d6518`  
		Last Modified: Thu, 16 Jun 2022 22:10:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8da8cb9433922bfac35cee36a9ee463b1a786a17b30cac15fb35b392201fd16`  
		Last Modified: Thu, 16 Jun 2022 22:10:48 GMT  
		Size: 5.0 KB (5015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
