## `influxdb:latest`

```console
$ docker pull influxdb@sha256:604286b4809c702b06f3f259938744457efb62357080e05d1e00637fb9dce9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:30d2b24b36c0d763de6be494e4caacc9f7c32f99a50a359569bc52aa51f0da03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116231917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129820bf5dd739acef3cdecb79f2fc6dbcfab47c88ca424906f8fa4a1060fef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 19:15:02 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 10 Apr 2021 19:15:02 GMT
ENV GOSU_VER=1.12
# Sat, 10 Apr 2021 19:15:06 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Sat, 10 Apr 2021 19:15:07 GMT
ENV INFLUXDB_VERSION=2.0.4
# Sat, 10 Apr 2021 19:15:12 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Sat, 10 Apr 2021 19:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 10 Apr 2021 19:15:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 10 Apr 2021 19:15:13 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 10 Apr 2021 19:15:14 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Sat, 10 Apr 2021 19:15:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 10 Apr 2021 19:15:14 GMT
CMD ["influxd"]
# Sat, 10 Apr 2021 19:15:14 GMT
EXPOSE 8086
# Sat, 10 Apr 2021 19:15:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 10 Apr 2021 19:15:15 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a23e1225dc83c683776f535e68ad815ca7fd88c6c5604c26e020658bef6e67`  
		Last Modified: Sat, 10 Apr 2021 19:18:26 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6503eaa7838769ede3a9772dbb56a771ffcff6780cf948129d329992abe7d160`  
		Last Modified: Sat, 10 Apr 2021 19:18:23 GMT  
		Size: 961.0 KB (960989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443db3bed31e3f6fb984281dfa7d2c8d15be4e5ca07ceed2cadee242a1ba9611`  
		Last Modified: Sat, 10 Apr 2021 19:18:30 GMT  
		Size: 47.0 MB (47001563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4eebf6b1be91780c0adad84076fcdc0d6b27a0e9e3dd2beccff3ab43f0430d`  
		Last Modified: Sat, 10 Apr 2021 19:18:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e2dd6edd49acb591991bb34a60adcfd18f8538758a4e05b63a3ea17b3e2fb5`  
		Last Modified: Sat, 10 Apr 2021 19:18:23 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17634653b3b73c75dfed114a62745f36b2953b61c7710c09960d3faba927a39c`  
		Last Modified: Sat, 10 Apr 2021 19:18:23 GMT  
		Size: 3.9 KB (3926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a1ad4c91f785c5192e14fdf09a8bdead94427331a15b89defc5029a0436f02f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112211365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4112fb1b3e6123701042257e654e3eb1faadfb007ba9044f69a6e4cd9f99469e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Mar 2021 21:46:50 GMT
ADD file:6a5cce92f1039ef2cb7ac6dd999c9f84289a9f6e1c0891d1edf791ea73b7e125 in / 
# Tue, 30 Mar 2021 21:46:53 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:15:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 17:12:59 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 31 Mar 2021 17:13:00 GMT
ENV GOSU_VER=1.12
# Wed, 31 Mar 2021 17:13:04 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Wed, 31 Mar 2021 17:13:04 GMT
ENV INFLUXDB_VERSION=2.0.4
# Wed, 31 Mar 2021 17:13:14 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Wed, 31 Mar 2021 17:13:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Wed, 31 Mar 2021 17:13:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 31 Mar 2021 17:13:20 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Wed, 31 Mar 2021 17:13:21 GMT
COPY file:f9664ff5942fcf872d1fcd8f91b28e3f7a4c39246a1a9f538b22029c8aa1490f in /entrypoint.sh 
# Wed, 31 Mar 2021 17:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Mar 2021 17:13:23 GMT
CMD ["influxd"]
# Wed, 31 Mar 2021 17:13:24 GMT
EXPOSE 8086
# Wed, 31 Mar 2021 17:13:25 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 31 Mar 2021 17:13:26 GMT
ENV INFLUXD_INIT_PORT=9999
```

-	Layers:
	-	`sha256:ef28e7e77ecbd3b3b426832bc12e8f5e629959683767466e9bac149c3286e126`  
		Last Modified: Tue, 30 Mar 2021 21:54:03 GMT  
		Size: 49.2 MB (49225808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344d2d9a9cf41c137b0dbb41df255f95fb812a23771a10ee2ab5a8a5047c62c4`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 7.7 MB (7694530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299f3631f6b52be065a7342da0a46978d55cbd0d15c57fae22f4ca24efcc295a`  
		Last Modified: Wed, 31 Mar 2021 00:29:59 GMT  
		Size: 10.0 MB (9984391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9ab46ceeb0a146647f85ddaf1972e840edb697acbf5239abd74ef0702c64f`  
		Last Modified: Wed, 31 Mar 2021 17:14:34 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335750e6519d2672bc292efbba97df6886170f9ff85556904ec857e218d2eb85`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 896.4 KB (896382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78780f92b7d6137947ffeb91607bad3e51a884a6113e35ab3fbdf2feefc38ea3`  
		Last Modified: Wed, 31 Mar 2021 17:14:43 GMT  
		Size: 44.4 MB (44403984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aec80c1e56918a8623d485e1e9c5e6843a8a2ad28daea18ae37b0629640ae8b`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc98efdfdd2d92c21d88e19eefa2bffc7bc35d527328605e95e1e4c36d12120f`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c3d67602b6db6d61c3b39a478e309af96fd2162ca6ba90424de77488e48165`  
		Last Modified: Wed, 31 Mar 2021 17:14:33 GMT  
		Size: 3.9 KB (3925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
