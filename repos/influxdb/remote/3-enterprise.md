## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:4113f82acd887c5d0228865dbe6b3591794d78b6057458d655eef7f7b937a6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:7781d9f311036bbb44141f6983369f29b467a1fc82c3d9c3c3993f07adb9edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159923454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c982870ed0f2165579cc75426eb003f3ec1cf0501b950e53146052e68a7b34`
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
# Wed, 15 Apr 2026 20:43:33 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:39 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0999e8f1462fbb09cb39ef08c282eda58df5d1e8c389005f194ea00cccecf`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 6.7 MB (6671623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38afebbd5132d82f9901425991a82a49bf410374f60e1b0ba57e420f0d33a6e`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08080051254204def33427dfac5ec1b091a9b5849d1552a1ca4e632b7441b59`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 123.5 MB (123514533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79ef371b5b265f128726acb79e36bd502e0227916d0f86fbf724d348d58da6`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42215201c4d468436362f05d42e64e4431e5fc007db05220d0f0b4d3e72419ca`  
		Last Modified: Wed, 15 Apr 2026 20:44:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f3f71dc42bfbbfd2a66fc92826a16ba17524e254845208f94ac1b9e601993189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b6fa96bed968f1e3db363fbbbb9c073c019f438e75ca05b5cc05d1db2012a8`

```dockerfile
```

-	Layers:
	-	`sha256:7044d2ea7b43afb998f551a78cc6cca87a848c19440a08858760886060d29034`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0dc250eea8be207f77782a07b795db475744e9fb46ff0cbf67acc02fd41ce4a`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:50dfce3b801a3bb452684d5744f928286d8d70682cab1d39d80e53580a094a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150758023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf7cc1716fb81f0809d6de6a2da460353e027e871816f1904a91dbf4c8ed482`
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
# Wed, 15 Apr 2026 20:43:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:40 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e62244524400b4e44e3ad020813e0a0618188bb064c5732855c664af09a06f`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 6.7 MB (6681811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf1620991e32dbed4397cdb8eb7293d57ee810171bf8c1a886dddd30185cb9`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7bb728ae5e717ec96034e40136c46b01ea54f9d2b9142f000fbca57e405353`  
		Last Modified: Wed, 15 Apr 2026 20:44:06 GMT  
		Size: 115.2 MB (115196105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fd7d303d393e57b9f180646bdde3ef3cbf21f9612aac91a2a17c4430410f93`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e591569b32d278adfe2b3b261c7775fbaade74d1da69cbfda55f85e1be4d613`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:745f936b54711018736135ccfc600a044e5ae237c330e17c303f3856250ae77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0ed19d8d0b7ccbf973e3ca952ebe95b6391b09e5363c6bc98b16359316256f`

```dockerfile
```

-	Layers:
	-	`sha256:5beb6f6b3a5737648090b5d78aadc2bc4d7e778c10f15d2da4c1621082b926bf`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b2310865e366114310e7a1d79734538d6ff848e247c157eeaac77405db85e5`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json
