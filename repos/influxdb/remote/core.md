## `influxdb:core`

```console
$ docker pull influxdb@sha256:8adfd9e62f7cab5ad8a8ecd776d4c7e77ee021e9813511cf5bf259f404c04b90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:c130a14b203091429f86b59f3d67a7acf388e14975c6dfea5491dd67cfed3301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (118011315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d883336301d9401f01e87e40c44e8d0dbfdff34ed86d6075f12d65ed7cbc72`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 13 Nov 2025 23:28:07 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 13 Nov 2025 23:28:10 GMT
ENV INFLUXDB_VERSION=3.6.0
# Thu, 13 Nov 2025 23:28:10 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 13 Nov 2025 23:28:10 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:10 GMT
USER influxdb3
# Thu, 13 Nov 2025 23:28:11 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 13 Nov 2025 23:28:11 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 13 Nov 2025 23:28:11 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 13 Nov 2025 23:28:11 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 13 Nov 2025 23:28:11 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 13 Nov 2025 23:28:11 GMT
ENV LOG_FILTER=info
# Thu, 13 Nov 2025 23:28:11 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 13 Nov 2025 23:28:11 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:11 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d85557ec595de1c3a60764a8aba957346cbba4339266a14255a1d3c29c675b`  
		Last Modified: Thu, 13 Nov 2025 23:28:34 GMT  
		Size: 6.7 MB (6666140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db07a204c3ef6a274ef7d33def97c46a83aee8fcab45fa109b182d8e7a1002e`  
		Last Modified: Thu, 13 Nov 2025 23:28:34 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b09663fd0da5e25bcde8263667026b624d19a339698c5150fe147a64566980d`  
		Last Modified: Thu, 13 Nov 2025 23:28:45 GMT  
		Size: 81.6 MB (81616354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1e55f8757c354abdbb61a4e6d933de0024e1c155b29b0b0e1a3b3aadfc182e`  
		Last Modified: Thu, 13 Nov 2025 23:28:34 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1fb1333b0ddf0e0407cf21279457653ace1d14868a3cef71c93143f99b6522`  
		Last Modified: Thu, 13 Nov 2025 23:28:34 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5a75b1b2ade34a3f7978b5f97bb4f70c7abf0a6f7e48ea18023c785ec7bb3121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc3419fdcc0630df53bc9d9db43111cb4e0b66fe9f2c7fa800b63cf8e467074`

```dockerfile
```

-	Layers:
	-	`sha256:b54cc6b520369fc8928f4c441fca16c83d3a27d74c1fb110c2023082478f2b07`  
		Last Modified: Fri, 14 Nov 2025 03:21:17 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6716fd33a7ea08ab8a6a8493182b73c72e8f692f5ea8e7d6a702701fe87410c`  
		Last Modified: Fri, 14 Nov 2025 03:21:18 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5811963580b06e8362ef6ad5308d3f4892b521ae4bcf91977d3db21daaaecac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108537195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc57734a1de74fe797d9cf22146e00b85faf366517af7373d188a459c7825569`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 13 Nov 2025 23:27:27 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 13 Nov 2025 23:27:31 GMT
ENV INFLUXDB_VERSION=3.6.0
# Thu, 13 Nov 2025 23:27:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 13 Nov 2025 23:27:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:27:31 GMT
USER influxdb3
# Thu, 13 Nov 2025 23:27:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 13 Nov 2025 23:27:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 13 Nov 2025 23:27:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 13 Nov 2025 23:27:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 13 Nov 2025 23:27:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 13 Nov 2025 23:27:31 GMT
ENV LOG_FILTER=info
# Thu, 13 Nov 2025 23:27:31 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 13 Nov 2025 23:27:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 13 Nov 2025 23:27:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b605091cb06332ff88280c68ce8bc3744ca18591e541da3a0e209c848a11a`  
		Last Modified: Thu, 13 Nov 2025 23:27:53 GMT  
		Size: 6.7 MB (6676637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa12b160bd09e4d8fb3bfd367590b3b1511141bc3474c3e323812f92d44544a7`  
		Last Modified: Thu, 13 Nov 2025 23:27:52 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0994ab1ebf5217fc1bd1b2fad9e72ebc0fd88dd8f0cb7719f4b507bfec56340a`  
		Last Modified: Thu, 13 Nov 2025 23:27:59 GMT  
		Size: 73.0 MB (72994476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1776b52bd1e59cdde64071b104b2b70dab326883575c4d7cc80fe4ba7f85adb`  
		Last Modified: Thu, 13 Nov 2025 23:27:52 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc17b62c44573b75c8d47a5019c57fe016b3813589ee2fb416c39e569e9937f1`  
		Last Modified: Thu, 13 Nov 2025 23:27:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3ca9df5015815436c4cb494e0e374a9c7c329387a8b3f0b4f66493da1eb4c142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25ff9261486b3662858c1ea8efd3e3f8cfa110514c8d14005fd8d6531490af3`

```dockerfile
```

-	Layers:
	-	`sha256:05bc13f10421bb2b381abeab3af4d31a118c67522d30e7eb3c5c80e256a811d2`  
		Last Modified: Fri, 14 Nov 2025 03:21:22 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1461b0f381d686aa18587480dd2dd70a5fb7c4e47a0282c68241f46b15693d98`  
		Last Modified: Fri, 14 Nov 2025 03:21:23 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json
