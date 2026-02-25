## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:255268d2a5f42b8c38d373864a4ba72956d91e14a3361019706bfad2f7c039ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:62775f106f8dac81e102b098d65ff85bced00936418c9689ec995c4ae081579a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119327710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822ae8137edf72418a2e8940ae5d9ee9a540ba42089758cf7f152633aaa9a9a2`
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
# Wed, 25 Feb 2026 17:33:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:33:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:33:07 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:33:07 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:33:07 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9542c760bea8712a7b1c7320237ab218944b72df43f69ed08641fae1d8c8e62`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 6.7 MB (6671516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d8ef7fd2a07ba4c6d17512223b9003f3fb95a0e816d58cfa268a72e52e6d8`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e48d156f776b0a2da1758df77ebd46edfd1fad75d9263c2bf8f372f1512b67`  
		Last Modified: Wed, 25 Feb 2026 17:33:25 GMT  
		Size: 82.9 MB (82924266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e350c598a24824dc923bbf46cda0ef4bdae4f038af8eff88c8b6e962fd570`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8897b1c30e1f42aea23a38708759ab99d46124513222b00c6d6278b834abc`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:39aad74b5cdb36ffcb31ad7ea28355818840cb560280535fa0ed9dba8a68571a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f8912a005531705bde9206c7cfbd729fba8b6021a5f966c0686b7f69a19610`

```dockerfile
```

-	Layers:
	-	`sha256:f7820589c3db8a4e9719fe6e0ee548b36c99b3d514cf136bf12da97fb3735d1c`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 2.3 MB (2310571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5e75a1973c652afdc1e55fee67cc715982acaf272ee16200297d6a2a256194`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6b45900e2ab53d82ae88dbbfcd757def6fe76ba93369743f2fd317b6a8e17846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110130123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c5a1135218b678758c5822631868dabc3016114cad2e110d78f5678ae85e98`
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
# Wed, 25 Feb 2026 17:44:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:44:15 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:44:21 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:44:21 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:44:21 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1600a9c64eb260873cf108122e4cdf204f8272ba853903f05a1c8ce4928cc9b`  
		Last Modified: Wed, 25 Feb 2026 17:44:35 GMT  
		Size: 6.7 MB (6681454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8f741a77a6ec6590221f763db0c06a439f2b3a4f0234d2eeec7b43a90ae1b`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc615a32cd32e801400994677df8f107cfa4f9e57facaed86ebf5028095ccde`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 74.6 MB (74579225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b5c05caaac19df93120744391be11a6fb6fa2dcc0caa05e0ae634e4aa8bcb`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f395b8f9fbee60a71ca0db75d66de3ba21d8c72bc0b8a822efe23579e83020b`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8134d33f6efa7eeb3dd051b4647f98e2707d239233aca84041ba7e3ad027e527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893aff8378f9a605d056fb94eae68f81a8a0bf94be432174cf0acdf9d7631c86`

```dockerfile
```

-	Layers:
	-	`sha256:69b0b59299b0eda121a960ef36b94d23f04a3deb935dafcb63268337c659235c`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 2.3 MB (2311653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9501d98ec72095cee13f3d9bc289f16f36f85c63d56c997e3930db1d51c228c3`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json
