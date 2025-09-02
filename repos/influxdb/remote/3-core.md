## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:8c3f00e2753ae66e10d4ed703f1dd81db837ca44b77a02f807ad3452305c4398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:277e9bb79fc0d67ed0887ecad7e727b984e91c4bd17712009a760727170a4cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115970202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97e09d535f57ec1618d718dbb8b321860a8f514110036fbbb94f3c04f1d729c`
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
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58caa54dae6936392a7d6810c9eeca044e5577994d946e6d522b76a83f52f59f`  
		Last Modified: Tue, 02 Sep 2025 00:24:06 GMT  
		Size: 6.7 MB (6665866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0b406ae8788be66faac6c384c5f7812bf46980a092f0b4aa0725d3956a368b`  
		Last Modified: Mon, 01 Sep 2025 23:46:44 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8c3b64e38059133ace238c3245222415d08b3dfd73e6184dfcdc0f57f5fea5`  
		Last Modified: Tue, 02 Sep 2025 00:24:16 GMT  
		Size: 79.6 MB (79577148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34674521d2d4724573cf4ed17e4ad132029957d5b57778b2caacc90416a72286`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b7e55a70382fd70564f93819b4cbcf759cd42c69fc75bc56a9de325fa6883`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:ce91f2aae27acb09b2166a43b8ced0b3182217b3888543809781fec0753b0988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c890ae03564b3efa65be90026287be84a5662795b27d57ee77495da681b98c05`

```dockerfile
```

-	Layers:
	-	`sha256:511b04d131f1e70ca40ca6a34b183af114bdaede0a96a7380a90ca57d647ec23`  
		Last Modified: Tue, 02 Sep 2025 02:20:35 GMT  
		Size: 2.3 MB (2311325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3e58644f894989c3832fee34f59b2ee2996400a1344525df0927fbe9613e00`  
		Last Modified: Tue, 02 Sep 2025 02:20:36 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:645c2db68ce0c9719dc36cef4f0942f04b4c2a765ec7ddd73f9c28566b47dfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106744391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c167dbdce8c3c2146c1af1303819f7b65f838f0c195d3422b062005ef1f7a4cf`
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
# Thu, 28 Aug 2025 18:37:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 28 Aug 2025 18:37:27 GMT
ENV INFLUXDB_VERSION=3.4.1
# Thu, 28 Aug 2025 18:37:27 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c5a748f13282a6d7aa41e6163030ef39209e05b4989378fb3ce8651e50756`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 6.7 MB (6676253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690f73b0940ac63456c13f244f6534063ec34d4807eeeffcffcfb15ce3b6eb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3102fbfd72fdd51b8b4567f96f3f202572c056064b12d7f88e7725485131fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:13 GMT  
		Size: 71.2 MB (71203770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1402cc014213ad6daf2e15b070d46ffb5bf7f94eec764ed85c8af4183d3bc3fe`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5940274ce8f96af68b646040a97b261c971b60dd71c8d53d628991b29fc883bb`  
		Last Modified: Tue, 02 Sep 2025 01:50:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:564ad84bbfe4a79a85f11cac717a492900dcccefa2c1320788515fdd9c9e3fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4414ee60de0301656ac337c9c8f28b535bb99ca966730724f26bdb03a71531c`

```dockerfile
```

-	Layers:
	-	`sha256:2a732303da3ec80b3fdedca489e93a6dc6ccdf95857ed0996a1a4c2ccdf2462c`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 2.3 MB (2312407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcfe401fef75d3354d0c656e0b0713ab11383b720eccc193c6caee349f8e87c0`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json
