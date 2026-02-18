## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:a74ab969bfea78bdb9b74f25c0f165a7ea8bbcae34a960794e566ec96158df51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:2ee599abcaf80831dd84f5c5f797b13cb5feedf91e97ab01f716503b73780cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127596441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b143087f8e1ff8b8feb452058e481f202da25ab44d32ccc0e339aa9a9c5615b`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Feb 2026 20:26:47 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Feb 2026 20:26:51 GMT
ENV INFLUXDB_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:51 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Feb 2026 20:26:51 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:51 GMT
USER influxdb3
# Tue, 17 Feb 2026 20:26:51 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Feb 2026 20:26:51 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Feb 2026 20:26:51 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Feb 2026 20:26:51 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Feb 2026 20:26:51 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Feb 2026 20:26:51 GMT
ENV LOG_FILTER=info
# Tue, 17 Feb 2026 20:26:51 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Feb 2026 20:26:51 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:51 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eb2c1e3918e3f72050828894c338eac23fc8ea720aa9257919f780198d0424`  
		Last Modified: Tue, 17 Feb 2026 20:27:08 GMT  
		Size: 6.7 MB (6669049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ac28a0b89d7412a041dfc4b2e111cee72801d3378e5b5953813bdea18e38b`  
		Last Modified: Tue, 17 Feb 2026 20:27:07 GMT  
		Size: 3.6 KB (3646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef0f2e144d8820a12e8041568b3de040e830d842fb63336960a7ef2a6fccd72`  
		Last Modified: Tue, 17 Feb 2026 20:27:10 GMT  
		Size: 91.2 MB (91195466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3aabca4361c9c1f82e02cd0146ffbca365524c79e5daefdc9ebcb729d955e4`  
		Last Modified: Tue, 17 Feb 2026 20:27:07 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e42d88b0d39d6a79d47a149234a411f87b63dd57c3602df4f4a1610c39d428`  
		Last Modified: Tue, 17 Feb 2026 20:27:08 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:2ad4aa717a5e403933b343a75c1ef0864d8d3b5b6438d91e1ccf1f0205086286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dd2aaf5181c22a52a72bbf1489ee0aa043c101103d2449f7432cf289105489`

```dockerfile
```

-	Layers:
	-	`sha256:754e87b08c8b9f00f6327dd8581612213c175d382fbbfb02f7944c570302eb06`  
		Last Modified: Tue, 17 Feb 2026 20:27:07 GMT  
		Size: 2.3 MB (2310619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404aaf19c2cfba1bb1eeebe2617f3a4af88b059475698479b7cc33677cf911ef`  
		Last Modified: Tue, 17 Feb 2026 20:27:07 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:099bf7f73f9e1ba728657c7017a9c8ca8cf810712c82a953ddbef7974e10d72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118247913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8a5c0c2f83c66122ad7cd0ed054be0793a3e935b599575e970d0581a295c65`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:54 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Feb 2026 20:25:54 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
ENV INFLUXDB_VERSION=3.8.0
# Tue, 17 Feb 2026 20:25:59 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
USER influxdb3
# Tue, 17 Feb 2026 20:25:59 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Feb 2026 20:25:59 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Feb 2026 20:25:59 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Feb 2026 20:25:59 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Feb 2026 20:25:59 GMT
ENV LOG_FILTER=info
# Tue, 17 Feb 2026 20:25:59 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Feb 2026 20:25:59 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Feb 2026 20:25:59 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c3ac202d89535f58bd4bf8abef22711b9d10012f839bc35cc6956eccd0571d`  
		Last Modified: Tue, 17 Feb 2026 20:26:13 GMT  
		Size: 6.7 MB (6680332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be26e0f8ed0a2670ecaf3be7dbd3df4b272f459e8fe04c79125c861a0ffc0f6e`  
		Last Modified: Tue, 17 Feb 2026 20:26:13 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729220a3c1ddfcdd40e45b95043c3ba18b8272e8e2b77a3f2a6fc5bd9ce1c9c`  
		Last Modified: Tue, 17 Feb 2026 20:26:15 GMT  
		Size: 82.7 MB (82698142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1054440cc675f706dc842e9554d46b9464063a6c048c875214cc5fe40ce5defe`  
		Last Modified: Tue, 17 Feb 2026 20:26:13 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14908fd67008afd27b7b09d292882d6ff4406c8d59e3394fbf4615fc18019ed1`  
		Last Modified: Tue, 17 Feb 2026 20:26:14 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0ac005ef183a404244a58809a03b046efe41ed655c336a0c926996adffd58c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92f27476e7d2d793b88f2770ad7eaaf7d6be1c1a66c517e2db6653d9fdb4927`

```dockerfile
```

-	Layers:
	-	`sha256:539649014870e4f8714104ed2dad24af95de209196bbee4b86b82c307b52ed89`  
		Last Modified: Tue, 17 Feb 2026 20:26:13 GMT  
		Size: 2.3 MB (2311701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028b12b7127a50393e67c6ed1dcd47627d45cb55f9036bbcc34a91bba138d6d3`  
		Last Modified: Tue, 17 Feb 2026 20:26:13 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json
