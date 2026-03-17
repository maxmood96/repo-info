## `influxdb:core`

```console
$ docker pull influxdb@sha256:609ebd662ae250de2979a14ebadb5fdabb638f36164291afbcd250689ce33012
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:485d207b488d55aeea7a5d3a3cc7840bb4f913d68672805dceae570a1d73bec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119332263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b859ca5ad155b3cc763d332fd2f72fe2a18dd7085b4caac8e1ff738126813e6`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:39:17 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:39:21 GMT
ENV INFLUXDB_VERSION=3.8.3
# Tue, 17 Mar 2026 01:39:21 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:39:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:22 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:39:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:39:22 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:39:22 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:39:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af5e6398084a9d4e75bb30b6c2aca56200184633c1cd8f7332ca9b42a2c10c0`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 6.7 MB (6671609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61664b8c9e70a8f737b8374de8a43c17a6e7ed951ea3405ae356ff8ac1504c2c`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb71f3ada84e0f969a23bc644cab325a901dea08254a55b58a3f4482f903b7ce`  
		Last Modified: Tue, 17 Mar 2026 01:39:39 GMT  
		Size: 82.9 MB (82924340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e231aea6c4f3bb50ae34666ed3ac19cad4ff24461b6c1c79fd9296e47a65b3f1`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1674f81369428f8c3e8ba40eb95877924aec2b43c2a40c127c1372a2227bb5c`  
		Last Modified: Tue, 17 Mar 2026 01:39:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:016e7be995c4b2e644e24cd8f6c53ddb00c9031c358699427d10bac41fcdc22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3a93850dd92cce14a5c095cabdac43aa4c2f8ebf5a2c52103d5e948c83f29a`

```dockerfile
```

-	Layers:
	-	`sha256:ad8d87fd71b8ca4613fb1aad11ecda70df15c75210e19ff5983e58fa9770a33c`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 2.3 MB (2310587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a0435bb1d6c40bfe6d6b5b90d7c15528dddc8ecc3b5a7efbe1a909f8bc727d`  
		Last Modified: Tue, 17 Mar 2026 01:39:36 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:63ea1e59b44f904a50bb2ca5c7fb9f9a8bb22a3c7a5c0587fbc707f7a2971db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110135104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341d195bbed7114c685d729af960d2fa3d95a56c3b8e8e702db8f68942e96dc8`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:40:06 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB_VERSION=3.8.3
# Tue, 17 Mar 2026 01:40:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:40:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:40:13 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:40:13 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:40:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5ff7761a3de3cfdfbde6b4aa7e485e10238103213ecb9db9c4609293d2faa6`  
		Last Modified: Tue, 17 Mar 2026 01:40:27 GMT  
		Size: 6.7 MB (6681856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1264b241981cfe9581d0ba6c743ec3b73bdbb1944e9081b0a022d4f407b473`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56a20c20f06dbbda1dd6a4ab1be0c7c77ea648b3965aba21c4e04af2c1a15a7`  
		Last Modified: Tue, 17 Mar 2026 01:40:28 GMT  
		Size: 74.6 MB (74579220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f703f18e65af6ac7ed5a6c75e70bd0a9e394f226f5ffc0e615d313f1202888`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbf9139ff50f89c76e18e8bd41cee3acb6e075925aa770b2ee60cc389321918`  
		Last Modified: Tue, 17 Mar 2026 01:40:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1aef9353b9015c5a38b910cffd2e48a199f9e96fcfdbf0bc40720e45c446f06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5730ad5f074116ae5eeafb6c90c912b8313fa502d86022540499653d7c2192`

```dockerfile
```

-	Layers:
	-	`sha256:8f0d054fc2be50c07051760fae65549046134b8a7433c570118936bbf76288b5`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 2.3 MB (2311669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee9350556a6e72b07053ccdedca25c80c0a30574bf73055e22981b7a17094266`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json
