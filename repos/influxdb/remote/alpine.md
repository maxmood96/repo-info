## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:1cb8fa92ff9d13518d8198dae872b7ea523757a03c655d12a67175b1ab7a72f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:99e216544ab6f8f8d4180d06bcc8deb61a676971c63e31faae24fc169945c4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86902190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343b7e7e34cb3b0c8e6c7a44f74f147f01f7ab4022ad1aa3c99ee43701d261f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:27 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:27 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298fb8d3d07e69a02cd49af0883ae79a93c4625bc43501293daf0d954698afb5`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896207ace1714281476706f02a38f5bafa2e8b0d466910e59c4abe1f0ef217a3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 10.3 MB (10274619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2fcd4f5629f0c11692de5d63652eda9a1de734dedd342a70ef1a8c1915d6e3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 3.8 MB (3822787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7399422b7a7b047fd9f9ae6a7b1b3c379169c0320d8c89787c7e57e378c95d46`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a421d960302e6e78e3497cecdfbf7e68f9f87afb9c264f7efd238f037129c2`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 56.5 MB (56510610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af09c2df41ffda41b4df2fd992fb0be316e613c2f08ecac1733e26e530fd6fb`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 12.4 MB (12421822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141bbaa5308a2f1112e696cb9e82bc575508bf3fdba5b192f4c5017ed1ff0345`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8db14735975847fbcb27a366734a994b19e81b52f37258eb95514dd7f2e7403`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66dbce9517e43a94af04ed7171b8a8c4174f59aeedd523604e88ced95a82de`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 6.5 KB (6493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:45ebd475ac2880a68c21896d4cb1186238df70770b3318fdfcc83ac0f437a337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.6 KB (982563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d587a6c839e8fdba54a6798485c7788dea62d5dc23bb982ddb676468b555f2e2`

```dockerfile
```

-	Layers:
	-	`sha256:00fb4b7e94546950e1d396936b5d2b235f6b34d79341a38bea451349ae4e71ad`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 952.0 KB (951954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c7670b411083afd6e9eee2031e773c5f9c80d7684afade5ae50a6602f99766`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 30.6 KB (30609 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:02a1ea25d55126eb4d17a75d949f6939f995ee716a38d5cf87dacbfcbc43b5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83028837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4487542a8db6296883e5107322a4eeb7ac2f72cf6251e1b284eb9f8ba30ad0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:29 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:32 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:33 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:33 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4647b3db14cecf9d1d3425f0c3d71e29d76706a4ba687c996add84a9e46d7ac`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fff389d9cde97293c698f3913f18598979f35d0502a8e50385bda21328b81c4`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 10.2 MB (10244532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b6866a06fadef09561556d16e7b2b3e0279d4ca952ac2e3675803c00008dbc`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 3.5 MB (3459165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f34a583141b546c821a5ff21181240e09fa803803fe707d8da1b354084a33`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a88da843f8eafbaedc72d393269a63b69eba46cd5780a319eee812b3428b8cc`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 53.6 MB (53636820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd2e861c1ced42fa6d0ba182a983a7cf3b6d02f861f36efcfbe429b15544c4b`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 11.5 MB (11480281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d56e532ff265b275aae709861e82df693b3c0e28e467fbd828aee0eb0d88`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b8df16388dbc099806c1c1818c3a2bde146ee08ff812e31237dd89b42b910`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97561ea1445f287f13425e0d8c6cc555dda4521823c070aee98a51e1ca95aa`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 6.5 KB (6492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:93902ca0265dee33a0a0ecae116ee8a0737de7a4b93bba1f8cadd54423063670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.4 KB (981356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ec019bd514eb7e1cda009f18e83ee9eb4242bf44eccda3b8f5330ee187a1a0`

```dockerfile
```

-	Layers:
	-	`sha256:b6b9ccdbf33b901df2b0084d3c64070e298e28ab046116b504914e56b831cb5d`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 950.6 KB (950553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b372300ad917b42bbf5b0f86f143b26dbe1d2b21c384a53e3a0fd0c0c2b4c6`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 30.8 KB (30803 bytes)  
		MIME: application/vnd.in-toto+json
