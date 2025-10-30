## `influxdb:core`

```console
$ docker pull influxdb@sha256:a25a19dce62cf445476f09246ff4fa148c5970acce533c761a627901b4084791
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:084e6388905ce8a40694400e6917e94a18ac36703c51e0d30f3cabd73e938dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118009788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c231aaad7d446107ceed0b5e59e07d94a46b5a0c73751412b444d83074a45821`
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
# Thu, 30 Oct 2025 18:32:06 GMT
ENV INFLUXDB_VERSION=3.6.0
# Thu, 30 Oct 2025 18:32:06 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 30 Oct 2025 18:32:06 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 30 Oct 2025 18:32:06 GMT
USER influxdb3
# Thu, 30 Oct 2025 18:32:06 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 30 Oct 2025 18:32:06 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 30 Oct 2025 18:32:06 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 30 Oct 2025 18:32:06 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 30 Oct 2025 18:32:06 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 30 Oct 2025 18:32:06 GMT
ENV LOG_FILTER=info
# Thu, 30 Oct 2025 18:32:06 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 30 Oct 2025 18:32:06 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 30 Oct 2025 18:32:06 GMT
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
	-	`sha256:766e2c6d3efcc07ff2a4c504f637ee9d7148b9f6cf1285c3fe25dfd5f3e17696`  
		Last Modified: Thu, 30 Oct 2025 18:33:07 GMT  
		Size: 81.6 MB (81616379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9290f652b91b6507c2b86910a2af3955e103df7cb2273e7504ac192baf1d29`  
		Last Modified: Thu, 30 Oct 2025 18:32:54 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce34ddd8984c94b940ee0c2a3f6e1127190991b45ca8d1bc6ef0d53326771ac`  
		Last Modified: Thu, 30 Oct 2025 18:32:54 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:b3da1fbb3dbdc9be2e45aa631ebd40a7f8ff90c51ba10f2a58f98fe58beb0446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336afa2928f3447033d67724807b5e503a7398dc630d201c4ec78f21fa5b3166`

```dockerfile
```

-	Layers:
	-	`sha256:c71ccf5f39f8e12dda291c5a79da6df3aea6b8d8d7cfe0f34035f13a7e6ba11a`  
		Last Modified: Thu, 30 Oct 2025 20:20:31 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10592ebc7cc3b4347fb55eb50d893219df3b63be154aa59eba97ad90eb12da0d`  
		Last Modified: Thu, 30 Oct 2025 20:20:32 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3afb32e4c0bfd020f96af904ae2efce9038c8c21fde04ea89708cd2daada917b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108536967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ba786d1d806c817a966f2d2e1fcb5c7ae0a087f31075865b03c18288eb8b1a`
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
# Thu, 30 Oct 2025 18:31:44 GMT
ENV INFLUXDB_VERSION=3.6.0
# Thu, 30 Oct 2025 18:31:44 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 30 Oct 2025 18:31:44 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 30 Oct 2025 18:31:44 GMT
USER influxdb3
# Thu, 30 Oct 2025 18:31:44 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 30 Oct 2025 18:31:44 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 30 Oct 2025 18:31:44 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 30 Oct 2025 18:31:44 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 30 Oct 2025 18:31:44 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 30 Oct 2025 18:31:44 GMT
ENV LOG_FILTER=info
# Thu, 30 Oct 2025 18:31:44 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 30 Oct 2025 18:31:44 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 30 Oct 2025 18:31:44 GMT
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
	-	`sha256:608c6abf26be903ab311520a2504822c926de03c7acb7bd6e1ae4111af60fb0b`  
		Last Modified: Thu, 30 Oct 2025 18:32:40 GMT  
		Size: 73.0 MB (72994484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d486965bf1d966b25f994fe8b597d3bd4d390f07bc5daa537b43265b815628`  
		Last Modified: Thu, 30 Oct 2025 18:32:35 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676cb34f85f639548ccf8895ef0b3677a81c11fc6edb0b88f0c3ccbee068b635`  
		Last Modified: Thu, 30 Oct 2025 18:32:35 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:2421fbaeb1cf929a5e6119dd74f94dc55ae0ca0294400fd9fa7683948ca03c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b4174d09e5c155ac2b2b1a50b27ac9886edaa26eefaf9428b84a7dec9526e9`

```dockerfile
```

-	Layers:
	-	`sha256:81ae236d59e3654921ccfbd1a767b9ad92489b86ff8181fd04f5f02146f9e160`  
		Last Modified: Thu, 30 Oct 2025 20:20:36 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4392bb936f255252fa3425dfb63e540b6d3f0bebb6ec437a4a1f6e54c479812b`  
		Last Modified: Thu, 30 Oct 2025 20:20:37 GMT  
		Size: 17.8 KB (17765 bytes)  
		MIME: application/vnd.in-toto+json
