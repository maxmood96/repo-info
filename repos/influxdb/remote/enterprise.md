## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:8da8c8b4fd4364c510dcffccb9900ea7860ace230d102652d884f9e48eb2b4d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:e5d24eb6731f8dc81ac7453669b9ad56a64b27218bc0273d4cdc6cdb12d9fa03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121187580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422ef7a711e56878c233d9f10cd95118f3ceb7f34126bd8c94ed8568b10dc4e8`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 10:23:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB_VERSION=3.4.2
# Fri, 12 Sep 2025 10:23:24 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
USER influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
ENV LOG_FILTER=info
# Fri, 12 Sep 2025 10:23:24 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 12 Sep 2025 10:23:24 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 12 Sep 2025 10:23:24 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2106beaaaf47e64336a53742be07eb10390b364f1b6ea68fa860d59d617e6aa7`  
		Last Modified: Fri, 12 Sep 2025 17:36:41 GMT  
		Size: 6.7 MB (6665894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2dae8d76a5cfc80c95e95424016007d1135580c8355f838695141a48af7fe3`  
		Last Modified: Fri, 12 Sep 2025 17:36:39 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e9a12f4798b97d77c1c2de970f232a27e02db9e9c0163f59761c0c429e9ab7`  
		Last Modified: Fri, 12 Sep 2025 17:36:53 GMT  
		Size: 84.8 MB (84794495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e1f596ccbf240809794ac4b605af90c8834d3e51360c8c5918a2cfb0f78ca1`  
		Last Modified: Fri, 12 Sep 2025 17:36:41 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b23a2b0115c1bed2e97e097446a1361445cc633ca49793a7331a1056ad64dd`  
		Last Modified: Fri, 12 Sep 2025 17:36:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cfb742e6700237b430e4cc71358ded3db393ef82247cc388013cf425770c1f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f8ea8bf363e8d316f815541d77c69b4ad9184f8bd3e061f6138bdcc9421416`

```dockerfile
```

-	Layers:
	-	`sha256:ccc1086f7cf84408760225c41e4507f31b0acaaa471be93778de6eb636896d93`  
		Last Modified: Fri, 12 Sep 2025 20:20:40 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c76fcedea8627b55023d907f18cf900fdbcdd4c3100b22473ab26cb56808c3`  
		Last Modified: Fri, 12 Sep 2025 20:20:41 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bd995e48ce2b6e8ca039c556df873c55078c59b04e4291d24c6c3ebdbf3f8887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111862220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2079e29dd702551b329e1d43824ef3774fd4472dae0d5c08ee539c03e198f2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 10:23:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB_VERSION=3.4.2
# Fri, 12 Sep 2025 10:23:24 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
USER influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 12 Sep 2025 10:23:24 GMT
ENV LOG_FILTER=info
# Fri, 12 Sep 2025 10:23:24 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 12 Sep 2025 10:23:24 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 12 Sep 2025 10:23:24 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce7b18b386d30b43df14b4df82f9b459f88018d19e15c57dce41034eae94966`  
		Last Modified: Fri, 12 Sep 2025 17:37:00 GMT  
		Size: 6.7 MB (6676283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac1371131315f2fd1e93a23aac846135a69c2a24f522f416a81400830b21eed`  
		Last Modified: Fri, 12 Sep 2025 17:37:00 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec03231be60ccdadb79b352a7111df3d0d2b2d6976278787d843ac03824dc79f`  
		Last Modified: Fri, 12 Sep 2025 17:37:39 GMT  
		Size: 76.3 MB (76321565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485421b3068117d4d7a3ad04d236c5a099a3c744eb600dcd2ea3d144eadaeb15`  
		Last Modified: Fri, 12 Sep 2025 17:37:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e02f19247b827803a8c97bc3551fae2449852d219cb818babdca9d2af04660`  
		Last Modified: Fri, 12 Sep 2025 17:37:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:8cf50015e72e4053c1b796bad1b0403d5d3e101659e5716aa3244f72ff855e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682bb6bb21fdd6702eecdf61664efc785da632524963851bca7feed0d59875c1`

```dockerfile
```

-	Layers:
	-	`sha256:f49285567fc6b87e42ae71195b57bde88fcc0a4392aa6679d3777e3abea02dc9`  
		Last Modified: Fri, 12 Sep 2025 20:20:45 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3616268c8dba413104f06648c6953734b74c887bb3990a5f2a2e9f34db4f815d`  
		Last Modified: Fri, 12 Sep 2025 20:20:46 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json
