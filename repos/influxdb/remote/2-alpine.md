## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:327be0243a329b1da350a37c1468d756f4258330d50d10a2a993e5bb9a6e3d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cac47619d57d832e6a0f787362eba5b3e1f36629afd0e2e843e066b35151e380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92006098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a7f3befda36a7f068f8339e56f8f59f6e527333e161482eae1d0df560e75c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078166243ebe0c2b9c91a2f7e164076218c7716b68301080fac2f19f177dd096`  
		Last Modified: Fri, 06 Sep 2024 23:21:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1587bf1467bd7fa0cc2b3706d4443a35b49f61bd49b1290f081643d747c38c`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 9.6 MB (9634631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395597bc0621a59fd604631b8c292c382b858b04d465c184da49759e54a5f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 5.8 MB (5820945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d0f5c43f5e203308ab55d4d25d6adedc07ff5e1ae398853254c3b438bbf159`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050deb0e5ac12402242203b9a1622d17bb64075b547efbbd845bec1f2a228b3f`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 49.8 MB (49790466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84be9b15369ef3c36eb630297dc094d0685e0b0b896139448712012f1770e988`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 23.1 MB (23128284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64fac09c6feb55954579c03c8eb95a176fa4466a843ffd0bff0f34285b16fff`  
		Last Modified: Fri, 06 Sep 2024 23:21:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc407c5347f2647cdac2b45ee7c93f275e3b7b3ae212b1ef9aa98d85bcde01a2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd950ffb540d8825efa00e5972a9aa81a31adcd1b9c6350cac0788e1a18392f2`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:acbb7b79cd5c3b0c183013df9776032eb14bb163e9eb2b3becd90c70b47a0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.8 KB (944845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3b3774810f57f3371aa23eaffa51ffbdc41e5b074a7c7e3ab902304cffe58`

```dockerfile
```

-	Layers:
	-	`sha256:5c072ab20e36c5f3b5b02ca06364a72e79aad9b7562f55eacf3460ebc071a8ed`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 914.1 KB (914093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b689f3cda8aaa0b6667d6a4d53280e261fa5922f2272a2269832f1b17f8711f`  
		Last Modified: Fri, 06 Sep 2024 23:21:39 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1000811b02d8b6fdb75ea723c4e9c33746c27e6d0be65a84b9152ecc28fb0f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88688483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba5f301346b7e3cba9218b3a9b5ae318b06386a0b000e04c7dab92f1576f5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 16 Aug 2024 20:18:45 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["/bin/sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '8e9fb0aa24e35774fab792005f05f9df141c22ec0a7436c7329a932582a10200  /usr/local/bin/dasel' ;;       arm64) echo '535f0f4c6362aa4b773664f7cfdb52d86f2723eac52a1aca6dfc6a69e2341c17  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXDB_VERSION=2.7.10
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CLI_VERSION=2.7.3
# Fri, 16 Aug 2024 20:18:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp influx /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 16 Aug 2024 20:18:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 Aug 2024 20:18:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Aug 2024 20:18:45 GMT
CMD ["influxd"]
# Fri, 16 Aug 2024 20:18:45 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 16 Aug 2024 20:18:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 16 Aug 2024 20:18:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4b70a44519145916f8803166c99c3ba52ea4bf109ad21b6d3e97aaa6f17a6`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9713c4c4a81b87a3373d8e7be5320c3cc5cc86ad74b6c2a3b331c3be04d8cac`  
		Last Modified: Sat, 07 Sep 2024 05:27:20 GMT  
		Size: 9.8 MB (9757048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbef7f92137af9c8d8b2ceb13c99138a68cd759251cc1d5e407ff11e6bd9db8`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 5.5 MB (5463803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a1f6a4d13197b794b1cec6c7f7160c8d5a86013ec29ba75ac7fb7cd7dda19`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928a7eba1ff5a21c666fa39ef8dade819caf6ce52010688b7d5b2d950456277`  
		Last Modified: Sat, 07 Sep 2024 05:27:22 GMT  
		Size: 47.7 MB (47709505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2432c5f0597753c705d3724184b3356815256a64a8c93aa3781d2e785593ce7`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 21.7 MB (21662516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933260cd0024e114bab17baef98e72aa06083573baa234ae705402c874b1a6e`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fdf5a00e872d5be68ab0f1f4c181170fb92a665999710b3589a2f80b8354b`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c614e03155dfd058b554c17f6b42e3fa4eddd5938d80ec113ef5ea4e07bc045a`  
		Last Modified: Sat, 07 Sep 2024 05:27:21 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0b50cc9671d0a3aded8e829d944212c24854b17ce177492fdd78e3c85adbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.4 KB (944406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436daff587bcef14431aa15b0a39ef47994bc66d9a0353450d30a519c01ad27`

```dockerfile
```

-	Layers:
	-	`sha256:ca5611f32d0ac5d978cefb8dc3b90ae6bfae5a67b19d2f2bdc02d6c9000569a7`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 913.4 KB (913354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e00d02321e4e44e7c735484a05227ce7d6b07e76a212b03bf5b22f30d7ee3d3`  
		Last Modified: Sat, 07 Sep 2024 05:27:19 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json
