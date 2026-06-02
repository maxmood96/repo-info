## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:95cc0f73d462902f77896a8524079b13c1d90fd93d11130bd3b64617496fb4b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:f54927c5a5a80eb559e02f72a447b171b60186ea4c922f587595bb99d7a357e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148828364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3dcc12fa76a635da99bc3336934bef4be746e94b09552a7efe3041636ded10`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 01 Jun 2026 23:16:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 01 Jun 2026 23:16:30 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 01 Jun 2026 23:16:35 GMT
ENV INFLUXDB_VERSION=3.9.3
# Mon, 01 Jun 2026 23:16:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 01 Jun 2026 23:16:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 01 Jun 2026 23:16:35 GMT
USER influxdb3
# Mon, 01 Jun 2026 23:16:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 01 Jun 2026 23:16:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 01 Jun 2026 23:16:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 01 Jun 2026 23:16:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 01 Jun 2026 23:16:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 01 Jun 2026 23:16:35 GMT
ENV LOG_FILTER=info
# Mon, 01 Jun 2026 23:16:35 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 01 Jun 2026 23:16:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 01 Jun 2026 23:16:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954fc2236a59caa2fac4ea3422b5c7e64026c585f6f9ca473699bd345f2371b`  
		Last Modified: Mon, 01 Jun 2026 23:16:53 GMT  
		Size: 6.7 MB (6672738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14624ec82d8ae2249d6d50d4f8eeeeecff652e2f69410baa898debec6f00aee4`  
		Last Modified: Mon, 01 Jun 2026 23:16:53 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11125bb55541ee68862325a177c4c27b04e33f6499341a19b377cd84ff39945a`  
		Last Modified: Mon, 01 Jun 2026 23:16:55 GMT  
		Size: 112.4 MB (112418328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c670b20d467c4f66acd42ee719982ee71d52233087d57d4ac1649715645e87e8`  
		Last Modified: Mon, 01 Jun 2026 23:16:53 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785cd8e3d184530d6660f15bdf6dcf8e504a1ec56cb21c3e506248c0afba493f`  
		Last Modified: Mon, 01 Jun 2026 23:16:54 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:53d64a10444622b7bd6a19e756860129c7a2836b59db3eac29f354d02af88d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c204a19c103f7c99dff79794a479acc8cc70bf9a7cf44120fae3877ccff83f`

```dockerfile
```

-	Layers:
	-	`sha256:2257f4ce8de3eac880abd90116c66dede19d86a88fcb1f839ef63ef03b5c8783`  
		Last Modified: Mon, 01 Jun 2026 23:16:53 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c61ab9f801edff27f6c01d00d19df8518aaa2ca68372d31e59539ccf828596f`  
		Last Modified: Mon, 01 Jun 2026 23:16:53 GMT  
		Size: 17.6 KB (17618 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:7d3623f58c29569664f970d7144c396d40951bd7f805920db732ecb1cff42a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140020291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae74187ef22ad8663f68999aa5e2493c45653a21a763c531f6e418ca25383247`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 01 Jun 2026 23:55:20 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 01 Jun 2026 23:55:20 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 01 Jun 2026 23:55:27 GMT
ENV INFLUXDB_VERSION=3.9.3
# Mon, 01 Jun 2026 23:55:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 01 Jun 2026 23:55:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 01 Jun 2026 23:55:27 GMT
USER influxdb3
# Mon, 01 Jun 2026 23:55:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 01 Jun 2026 23:55:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 01 Jun 2026 23:55:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 01 Jun 2026 23:55:27 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 01 Jun 2026 23:55:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 01 Jun 2026 23:55:27 GMT
ENV LOG_FILTER=info
# Mon, 01 Jun 2026 23:55:27 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 01 Jun 2026 23:55:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 01 Jun 2026 23:55:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45f291d1600fa29781de1a4dd47f3bed21c81a9b5f452117ba59e52425c16f4`  
		Last Modified: Mon, 01 Jun 2026 23:55:46 GMT  
		Size: 6.7 MB (6682548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d685fe300fa4c1cfc6abacb8a71d908413ce652a08da3597e64646c30ca4e627`  
		Last Modified: Mon, 01 Jun 2026 23:55:46 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bd98872a94a01473ca137ab25eed849bc9157e60f84493f9782e128d2f3dec`  
		Last Modified: Mon, 01 Jun 2026 23:55:49 GMT  
		Size: 104.5 MB (104457630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b2750f7026b63bfcc71de97a5931f33237acdc496f2fdfc235650caeb22b1d`  
		Last Modified: Mon, 01 Jun 2026 23:55:46 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf920c02471a3780ba712ec8723fae47c5e3339a482371dc200e15b8c4db6ac`  
		Last Modified: Mon, 01 Jun 2026 23:55:47 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5ccefa9405b7cc45ed6cf3703245639a446627342cc257c4b6209f6b9ba5cdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbf68cbdf38270fd9990b45b169e81a19bdb597372711b27a2bc0cabdc8235f`

```dockerfile
```

-	Layers:
	-	`sha256:5e2b065676781eaf85ad9dafe63b7a4d8814d7bff2eb4bb9f32173bbd7a872b6`  
		Last Modified: Mon, 01 Jun 2026 23:55:46 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf598a7fd3e48da95eb9afcac01abc193695517e4feec30ec3281f2c7487c5e8`  
		Last Modified: Mon, 01 Jun 2026 23:55:46 GMT  
		Size: 17.8 KB (17767 bytes)  
		MIME: application/vnd.in-toto+json
