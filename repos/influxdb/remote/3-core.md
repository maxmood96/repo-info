## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:6e5120d42cf9d2c89fbea7f2712d735c595627394d77e9098fc517dc1b8b6069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:34658499f994fc76fcb0702c89fd1d009a47b903ddf77adcfb00687dadd13837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117163034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3fac599ad81630f4f1297869419063a64ab576379fbec5d5413f3d6cd2ec2b`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be18554758c9da4c66c3f1c1aeac0479ec0e8786709fbaddbe8ebb03604fb5f`  
		Last Modified: Tue, 30 Sep 2025 18:07:22 GMT  
		Size: 6.7 MB (6665983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e8ec553336d6206472e5c2bd3b0f8130b47f60cfe6a2551f5920232290a085`  
		Last Modified: Tue, 30 Sep 2025 18:07:20 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e53d9ae17647b951dc8e2179b118946d2da5bd0c9ba131a5d466e622c624d03`  
		Last Modified: Tue, 30 Sep 2025 18:07:34 GMT  
		Size: 80.8 MB (80769477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1804a088e590b5ca9ec1e212dcf213718f6c28b7b952aca1458ccd918181cf1`  
		Last Modified: Tue, 30 Sep 2025 18:07:21 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58321e87c0e6b711794e452f3a8f72860fc233e5dbb1d495b5916f12f3fda0f0`  
		Last Modified: Tue, 30 Sep 2025 18:07:21 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:90018bfcb51677590c07b28c7d0cd8dc3c4cd00514a34661300c58b12b56fa53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2c8b909087c64be29f51d23482907f90fa14f3bdd8bcf7e5791a2f958d884e`

```dockerfile
```

-	Layers:
	-	`sha256:008ea9afd0dd62df0107dbedf81f8c46f1a3efbbf454d4730827595628be45a4`  
		Last Modified: Tue, 30 Sep 2025 20:20:37 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c202cf54e678eca643d7a84442f37170a725410f66ef2ff0d118f051da05f643`  
		Last Modified: Tue, 30 Sep 2025 20:20:38 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:758c1a038d65b404028e569cc9284e00b1c513b50a581a88f9ac16c3a858b331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106588999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452fa4782937755e004b25d81cd21387ee068907e9b99348c35664eefe66b1ae`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=3.4.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 24 Sep 2025 16:08:46 GMT
ENV LOG_FILTER=info
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76772dfef93d9692ae29670bd3c35ef1b32af43be390336ce02735ca2e6ed34c`  
		Last Modified: Wed, 24 Sep 2025 20:42:13 GMT  
		Size: 6.7 MB (6676456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dd47aad406061c9bef9141140aaa9b6759d82a1c241eb78bfd0557b0bbaf3`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0ca37718bb135be92a784b085b083c56d6441e024e170147d526ce62dbeb13`  
		Last Modified: Wed, 24 Sep 2025 20:42:16 GMT  
		Size: 71.0 MB (71047103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf300e1edc90912abd0f245569a70a5e38003d97ee7cc3df20da44178e19697b`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdda608d41ce88b20843112b0fccf8213f3a4cd48021557a305fe7ed9cbe3982`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ff5fe04ac92f2cba5c11a9d0ff4aefd16d2e155c4f6aa52979df3849d07098b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae50fbce074dd9457296eabeb258782360b24d7a45b4ccf9881dd8730f19169d`

```dockerfile
```

-	Layers:
	-	`sha256:16a8560fea8f78d8906afef5d7056ce77ddd281f67ae502ad05fe1f856f3bb5f`  
		Last Modified: Thu, 25 Sep 2025 02:22:25 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c8c699c2ee5bfb443845220e3923cb29f00e1999aaa9b529a9909d9725ca59`  
		Last Modified: Thu, 25 Sep 2025 02:22:26 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json
