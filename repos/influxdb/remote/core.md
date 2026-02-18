## `influxdb:core`

```console
$ docker pull influxdb@sha256:13a654390eccd4b238895b458e1b4a796ada2365123a034df9037cf7a4f4af5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:86fb0faa27e25045697a5ab9fb00db257b28ab45ca0cb16509b41770aa4d39cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119315520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29755ac02d6e91e79a1d49de332ca9632ba8b5e0b3e039ef7f77140f57af840`
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
# Tue, 17 Feb 2026 20:26:43 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Feb 2026 20:26:43 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Feb 2026 20:26:47 GMT
ENV INFLUXDB_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Feb 2026 20:26:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:47 GMT
USER influxdb3
# Tue, 17 Feb 2026 20:26:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Feb 2026 20:26:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Feb 2026 20:26:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Feb 2026 20:26:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Feb 2026 20:26:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Feb 2026 20:26:47 GMT
ENV LOG_FILTER=info
# Tue, 17 Feb 2026 20:26:47 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Feb 2026 20:26:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c41f28f5fdd910c410780c1c4db6cee33910b875cf1e18bdffa15e3e01a44b0`  
		Last Modified: Tue, 17 Feb 2026 20:27:04 GMT  
		Size: 6.7 MB (6669013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da394d7d2a208df9cb55d4eddbf17d1ad5495e3efb321e2b9d4a450b59a1ad`  
		Last Modified: Tue, 17 Feb 2026 20:27:03 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5640df528faf34644b94efcbbdb6096c78d03db5867e1095991c495984dca4`  
		Last Modified: Tue, 17 Feb 2026 20:27:06 GMT  
		Size: 82.9 MB (82914576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325e355c9a8eae6bca031f814769b4cfd12409ac3b7f68bc9f399d09ed9c7eb8`  
		Last Modified: Tue, 17 Feb 2026 20:27:03 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cba355e2ad961f290f7a1061352a0fed369d7946bd6da88d3459718534253e`  
		Last Modified: Tue, 17 Feb 2026 20:27:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:481e7bbf3975d2b2f89f267bd187655c4c7bb0896ea53d8e033e37aae9fe8d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55be7d705a94715d66808c6044cf17ec50153193bd4db5ffdd5227520a3117a`

```dockerfile
```

-	Layers:
	-	`sha256:6ecc882783b5dc78237ca5b18c9b80a537e053ad736abdf4bb5b11ae3e64d427`  
		Last Modified: Tue, 17 Feb 2026 20:27:04 GMT  
		Size: 2.3 MB (2310571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cdc894da6861a768144e3c8fd69db650e6cd33afe8f16bc16e869e5b15e52eb`  
		Last Modified: Tue, 17 Feb 2026 20:27:04 GMT  
		Size: 17.6 KB (17616 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9a3950324cae81a42201f3951246769c68bee07c536470c92e6e22fa9ec5d460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110032568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff11b1f02b6c06f73bacf23e59e0d851c22c48749abde373e13594b60681437`
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
# Tue, 17 Feb 2026 20:25:51 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Feb 2026 20:25:51 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Feb 2026 20:25:57 GMT
ENV INFLUXDB_VERSION=3.8.0
# Tue, 17 Feb 2026 20:25:57 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Feb 2026 20:25:57 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:25:57 GMT
USER influxdb3
# Tue, 17 Feb 2026 20:25:57 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Feb 2026 20:25:57 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Feb 2026 20:25:57 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Feb 2026 20:25:57 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Feb 2026 20:25:57 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Feb 2026 20:25:57 GMT
ENV LOG_FILTER=info
# Tue, 17 Feb 2026 20:25:57 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Feb 2026 20:25:57 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Feb 2026 20:25:57 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511288e41ee026ba32e82e1bfe0fcdeebd504462680906ccf3bca8c8990828c7`  
		Last Modified: Tue, 17 Feb 2026 20:26:12 GMT  
		Size: 6.7 MB (6680332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d489d510d7d747397d69b02d5aa936d307f200cc73ab7ca671de76da670245`  
		Last Modified: Tue, 17 Feb 2026 20:26:11 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe516ffdd73537b8e857f3111e9da89860387aaf76f6021441b9178b445d2cd`  
		Last Modified: Tue, 17 Feb 2026 20:26:13 GMT  
		Size: 74.5 MB (74482795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceb6f43c8a090b26b05410b5ad953eb6d2af634ecc5060921e186af2c309c62`  
		Last Modified: Tue, 17 Feb 2026 20:26:11 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6f18a9fee6f280b2f5ad18c3e783df965b0ba1f6a6270a2d1f2095cde2c354`  
		Last Modified: Tue, 17 Feb 2026 20:26:12 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8709d3bbadeec75416270b5acae8b7f9819454b0971d530be7ef468247fb6e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322c44092f2129776fafb475b2b9c000bf237fef17572660564ebc50b64ae717`

```dockerfile
```

-	Layers:
	-	`sha256:73d42bc848c15897af80b46983c26ba84905754363fad954ae003864b2edb613`  
		Last Modified: Tue, 17 Feb 2026 20:26:11 GMT  
		Size: 2.3 MB (2311653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa11e2d5a604d7d4244fdd1c870614f8af9b4b8bb2e028dd30e9369fe4f7d8ce`  
		Last Modified: Tue, 17 Feb 2026 20:26:11 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json
