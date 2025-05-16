## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:268a2553b83bc434f37017e1b8faf2084e8578ce0adaf7ff48f90c856361a640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0831d74c4536fcf32559efc45387d3c9e86b73298e03eca7365e511205594ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc6e48be2b2670b9aa821717cbc52bdf388a660d63e36b64e81844f3a811ef2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae520f817f8cab06dd90a7dd53cf0f5913b476bbf6ffb463664d14028482b4c`  
		Last Modified: Fri, 16 May 2025 19:10:15 GMT  
		Size: 6.7 MB (6663469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f5f6b5a16642b2e7d600a78ccdb14667d4b733c7c67e70d0a34452a74c4b5b`  
		Last Modified: Fri, 16 May 2025 19:10:06 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d09603a0a7affbe9365e383b9441ffe05ca55e340cded8251f267a5f909ced`  
		Last Modified: Fri, 16 May 2025 19:09:37 GMT  
		Size: 63.6 MB (63616620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddb6ae1b11404986ad7cab5ef50d3f063229042eb15b212c2e6df5a7f633995`  
		Last Modified: Fri, 16 May 2025 19:10:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96604f7f2839a5948435ec73b7302b4ed49d6b55846cd167beabfe1c67f07189`  
		Last Modified: Fri, 16 May 2025 19:10:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:5d2b290f04c945829b3e9bb07ef592aa47b41e0ee615ebd1e868c9f1765b0f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096fedc4b5d1bdc4329142f4db5c21abc14647db78b832289ce5f15457adf15c`

```dockerfile
```

-	Layers:
	-	`sha256:9a19028d33d179c531cdff08009d86f0f5345b13ab2665008b0c8d9a89339fd0`  
		Last Modified: Fri, 16 May 2025 20:20:39 GMT  
		Size: 2.2 MB (2203288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f59d10de0920ee5c0b5c0354cc5381868cf5aae0c9c0884d39e6742e41165d3`  
		Last Modified: Fri, 16 May 2025 20:20:40 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:86c3040da8a31671b4a8723820f1fd058dd6daaf4e104ae676cdd35a6c1bfc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92545538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d4c0472559b432bd42cf220d9af4838c7a6b9e1db0478075582fc04529da76`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 16 May 2025 17:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 16 May 2025 17:01:08 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_VERSION=3.0.3
# Fri, 16 May 2025 17:01:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 16 May 2025 17:01:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 16 May 2025 17:01:08 GMT
USER influxdb3
# Fri, 16 May 2025 17:01:08 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 16 May 2025 17:01:08 GMT
ENV LOG_FILTER=info
# Fri, 16 May 2025 17:01:08 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 16 May 2025 17:01:08 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 16 May 2025 17:01:08 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d3ffcca3dea02f4c8adcd31729621ed8d7e4b7531c23b8cac9775f570b5085`  
		Last Modified: Thu, 08 May 2025 17:41:14 GMT  
		Size: 6.7 MB (6674461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f74b4aeea550ca1632e75aa80f8fa8a2ccff90a4138e9f7d1c3d8333e53e3e`  
		Last Modified: Thu, 08 May 2025 17:41:13 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8e9105883f39dc1d6116059355f136f26bf486bf75708411cba6b55f073c60`  
		Last Modified: Fri, 16 May 2025 19:10:26 GMT  
		Size: 57.0 MB (57020072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8104228122b89805d5c0dc89a695746c7aca0dd1ef6c3b9d43ca679aa0e66ada`  
		Last Modified: Fri, 16 May 2025 19:10:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1db856ab0eb66e0cda8f05e476554e03272928b30687b330db9c0b95718e05`  
		Last Modified: Fri, 16 May 2025 19:10:09 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:bf122adb7f665faeabcaa74c5faa11d6b3858be55e644c790a846648ce95ff1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2222291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50ade38012f71c2132eb2363f019fd69211c4b0e9f4f862ba0f78d615b0097b`

```dockerfile
```

-	Layers:
	-	`sha256:75efb097e69e31f377df0f8ecfd45207e2aae47de9bc46fb465060a2c099729c`  
		Last Modified: Fri, 16 May 2025 20:20:43 GMT  
		Size: 2.2 MB (2204370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3b555aecfe9bc0b48dde231eb7f206df331fe649a5179b17a3c63dd969899e`  
		Last Modified: Fri, 16 May 2025 20:20:43 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json
