## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:670c787160e2d5d132cfd8cd44640db06e0c814538ddf52ae326c96f2c63ed67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:ec6482948dc399ec027dc40a84378bbe208ff5e4c3577e2e51a859372fa489a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124634971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0841097a6632eac24817fd323e7ab612cfd1e4a525d7cffa77ed53a195fd4ac`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:32:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 30 Oct 2025 18:32:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 30 Oct 2025 18:32:37 GMT
ENV INFLUXDB_VERSION=3.6.0
# Thu, 30 Oct 2025 18:32:37 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 30 Oct 2025 18:32:37 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 30 Oct 2025 18:32:37 GMT
USER influxdb3
# Thu, 30 Oct 2025 18:32:37 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 30 Oct 2025 18:32:37 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 30 Oct 2025 18:32:37 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 30 Oct 2025 18:32:37 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 30 Oct 2025 18:32:37 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 30 Oct 2025 18:32:37 GMT
ENV LOG_FILTER=info
# Thu, 30 Oct 2025 18:32:37 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 30 Oct 2025 18:32:37 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 30 Oct 2025 18:32:37 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da20188c46cb2cbaaa3296e6cd5eea94d165b3608cfb4829e9a920c615376d89`  
		Last Modified: Thu, 30 Oct 2025 18:32:56 GMT  
		Size: 6.7 MB (6666140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9acd8e86ffa51ede57e6f9d3b175cf86ed76cb86731b6fb8cf3cac20fe648c`  
		Last Modified: Thu, 30 Oct 2025 18:32:55 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28af1f204e6fcfac6d3ef92f69e5430a795dd298fcec1e4115a4d0a52790f4ad`  
		Last Modified: Thu, 30 Oct 2025 18:33:13 GMT  
		Size: 88.2 MB (88241560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8cd5b6d1d30086005ef18704c67d36e8b2fa988defea2ba94a4573e9aaecc1`  
		Last Modified: Thu, 30 Oct 2025 18:33:01 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4624dfd10e6f130ca51cc7d90844036f78af3faec147b31a61c3b6d4311d0d`  
		Last Modified: Thu, 30 Oct 2025 18:33:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:7784b447a84796ac75d22e0bb60f9e8507c5726870dfbaad7476367be1e29650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39776235ed5165b58d567f6781f9357cb275f0c31b5cf9b404ec4991ace2f5e9`

```dockerfile
```

-	Layers:
	-	`sha256:c8e18caed20ca99e37150f3a7a416f8ecf2e916929470a553435f9bf3c73a1c0`  
		Last Modified: Thu, 30 Oct 2025 20:20:39 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd73173fe2ac178a6bc955a3f83631fe5fe760bfa8216c7fec61611acf323d0a`  
		Last Modified: Thu, 30 Oct 2025 20:20:40 GMT  
		Size: 17.8 KB (17796 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a6447529ab8432fdb982a8aac1535cc02349a1abe0e734740a0d8c76ed58da75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115040040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0151e6bfd09e80940b6cf3c16141348c827fd10ee5a377e8c142dcd183d9a587`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:31:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 30 Oct 2025 18:31:38 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 30 Oct 2025 18:32:12 GMT
ENV INFLUXDB_VERSION=3.6.0
# Thu, 30 Oct 2025 18:32:12 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 30 Oct 2025 18:32:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 30 Oct 2025 18:32:13 GMT
USER influxdb3
# Thu, 30 Oct 2025 18:32:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 30 Oct 2025 18:32:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 30 Oct 2025 18:32:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 30 Oct 2025 18:32:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 30 Oct 2025 18:32:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 30 Oct 2025 18:32:13 GMT
ENV LOG_FILTER=info
# Thu, 30 Oct 2025 18:32:13 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 30 Oct 2025 18:32:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 30 Oct 2025 18:32:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539bc34e9ead0d3297471cdef928fbcf43477462ceee893be10876a3f3cb04ff`  
		Last Modified: Thu, 30 Oct 2025 18:32:36 GMT  
		Size: 6.7 MB (6676640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9be9adad60e477e108e4628310b4c4ed12042edf0c06e21b746f00283aa282`  
		Last Modified: Thu, 30 Oct 2025 18:32:35 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d77b4739ca6b5e78498591ed4966ff1e3ed2c23ca35ef434b7dcbb945a1b631`  
		Last Modified: Thu, 30 Oct 2025 18:32:45 GMT  
		Size: 79.5 MB (79497559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1031c2725becaf84b714b5fbd65275a5c3669149020a078bb53eb0f549464383`  
		Last Modified: Thu, 30 Oct 2025 18:32:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b166e1f4bb9781c9a8625872a4db82cfe369b64cc286be66c2038606592d6b49`  
		Last Modified: Thu, 30 Oct 2025 18:32:35 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:519d7dd2757f6eb2d0e82d901ba9061cc57d61bdf722a02bc334ed4893ef656d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e247684a7640ca0cccace67913efd763cd03ece2e2d50c4f8d99a4036578194f`

```dockerfile
```

-	Layers:
	-	`sha256:de5f3e2432844705e22dc786cfad36b92b559994f23d7a520a5e2d886cd6c535`  
		Last Modified: Thu, 30 Oct 2025 20:20:45 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46d321d403576c47173e388e0ba546a1c11f0fa1b5b07bb90001db871afeb7fc`  
		Last Modified: Thu, 30 Oct 2025 20:20:46 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json
