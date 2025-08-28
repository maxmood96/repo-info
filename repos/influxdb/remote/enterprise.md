## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:28a44644d70a550cf54a982976c926ffaf7c751682fd39b96688c488f2e61732
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:cdcfa3de328f2f27cbad1686ec39c22599463b09a5b033b224f4be3173255bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121181571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73255fe4169f5e9ed3bf08ccc0c800434857710195c1eaf6a071cd1d696825d8`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
USER influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 28 Aug 2025 18:37:27 GMT
ENV LOG_FILTER=info
# Thu, 28 Aug 2025 18:37:27 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 28 Aug 2025 18:37:27 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 28 Aug 2025 18:37:27 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32852e5440bd0edaa11de98c9b84efee8b0be81e2b7fa74718fc710688f082b7`  
		Last Modified: Thu, 28 Aug 2025 18:56:32 GMT  
		Size: 6.7 MB (6665850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947323696c19ed184ffd48ec6564bb25bb13834f2a78584641fea053961519a`  
		Last Modified: Thu, 28 Aug 2025 18:56:31 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056b4aa716e9f2ce15b82198399f117f265b26cef3df8d93a390c47a51e72606`  
		Last Modified: Thu, 28 Aug 2025 18:56:41 GMT  
		Size: 84.8 MB (84788373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a125f31c6645ae9724faef9bf12fe5bd709fcf981515b127ad6fd206ecce2aa2`  
		Last Modified: Thu, 28 Aug 2025 18:56:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f080a48886eaebfb88b80193f8d3a00b0ed74a9f67fe08a1a24450f535b83`  
		Last Modified: Thu, 28 Aug 2025 18:56:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:161a4032456c60e940ec5f6ffc833b0c2bdf0e6420b6b5e606c70ece9208ab4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7754572a6d33008a5805b3a32f68c216786c0f5850eb32be8ef85545d952c8d`

```dockerfile
```

-	Layers:
	-	`sha256:c25a0627bc4149bc06b6d159fd9bf0816820091b8de415d7e812564c027fd13c`  
		Last Modified: Thu, 28 Aug 2025 20:20:35 GMT  
		Size: 2.3 MB (2311373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91d4ee754cad5244b5181587b27870f4294612108d827d075bdfd575a7548b30`  
		Last Modified: Thu, 28 Aug 2025 20:20:36 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f1f251f053c53c148bbb84d7726d719e725986fc886330a00b7fd7e145227d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111853246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8aa50a8435e9832d0e12b02590ac02d0c6409ffc51c3473856a87aa2aa2bc4`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Wed, 27 Aug 2025 00:34:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_VERSION=3.4.0
# Wed, 27 Aug 2025 00:34:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
USER influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 27 Aug 2025 00:34:47 GMT
ENV LOG_FILTER=info
# Wed, 27 Aug 2025 00:34:47 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 27 Aug 2025 00:34:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 27 Aug 2025 00:34:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8628ffec9dda4bc049719755d628560ca16ac61364a101ff6c22478848e1806`  
		Last Modified: Wed, 27 Aug 2025 17:02:54 GMT  
		Size: 6.7 MB (6676366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432ca6bd3af57def5016ada52bbb59e768669a06687a6c4b3bed81b95299952d`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad28f90cfd07ae2a34346f534f0a5afa3f2ba1808ca6e188ac9c1e98be7171`  
		Last Modified: Wed, 27 Aug 2025 17:03:02 GMT  
		Size: 76.3 MB (76312368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab21b027a1b91134863f0d6a8b0280defda9e18b27c6ff7dcfe45b94d481d663`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a834f37dd732c0c9d9c6642f3d91c1d86a731d30bf5daa86ec2c477b3cddf95`  
		Last Modified: Wed, 27 Aug 2025 17:02:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:692d56b80cade7cfac47d3b76427653e6444d222446943f72fe932572b961fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad5d878640e4ee213646beabdbd456adcbd69f0edf5fbfba2f702a98b5349b3`

```dockerfile
```

-	Layers:
	-	`sha256:f0de14be245955e27425063a3aa8640a256813fec0ec831f32483765689df663`  
		Last Modified: Wed, 27 Aug 2025 17:20:42 GMT  
		Size: 2.3 MB (2312455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3826b90ba182cf0fef86bdac9486bff26094964668218dcabc8efa7ca68c2acf`  
		Last Modified: Wed, 27 Aug 2025 17:20:43 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json
