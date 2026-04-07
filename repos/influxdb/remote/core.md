## `influxdb:core`

```console
$ docker pull influxdb@sha256:0712f79a7c4e7b3da3f5777fa340bf5a65b165b5a5d44dc6631b6a50663352ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:a376c81200d7ca89c11a8a45e10a671552fde14eb3a74f193b11a33dda1a7d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149137037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5075c02d03480a77553c09088fae18b292a887704c4dad5d79aca3313692a3`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:58:20 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 07 Apr 2026 01:58:20 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 07 Apr 2026 01:58:25 GMT
ENV INFLUXDB_VERSION=3.9.0
# Tue, 07 Apr 2026 01:58:25 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 07 Apr 2026 01:58:25 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:58:25 GMT
USER influxdb3
# Tue, 07 Apr 2026 01:58:25 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 07 Apr 2026 01:58:25 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 07 Apr 2026 01:58:25 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 07 Apr 2026 01:58:25 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 07 Apr 2026 01:58:25 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 07 Apr 2026 01:58:25 GMT
ENV LOG_FILTER=info
# Tue, 07 Apr 2026 01:58:25 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 07 Apr 2026 01:58:25 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:25 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5ad7b3968459438956b216dd5c879f403416f050c7d8fce6d3bd7967946150`  
		Last Modified: Tue, 07 Apr 2026 01:58:43 GMT  
		Size: 6.7 MB (6671794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204cb8824bb1d461b813de06285748182f31bec742d569871c187f3fc5e04d0e`  
		Last Modified: Tue, 07 Apr 2026 01:58:43 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11e8715976555a0c76229b8713b7989df84e70aeb08878045841d84cfbfd776`  
		Last Modified: Tue, 07 Apr 2026 01:58:45 GMT  
		Size: 112.7 MB (112727461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8038859b81ed37a0ca5d7fca7b6fb0f3f13440cc3828b65b9cc67f1d906174e`  
		Last Modified: Tue, 07 Apr 2026 01:58:43 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ae236dac262f1a6495c0ca09c06cf4176d04ae5c6616100d825f55433b1d68`  
		Last Modified: Tue, 07 Apr 2026 01:58:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1086e2a6d3e915660fb845a107aeb53ebb1675ff3c77e1355fe6a84c5d537024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048e4710d695bd94dfb7633f6623fef72c124ad611f569838ec29c44b4c75cdd`

```dockerfile
```

-	Layers:
	-	`sha256:47edabb0b2fa76b42c49c5cc6b7bb572ea66e00654c1d4cb319a4d9768870d0d`  
		Last Modified: Tue, 07 Apr 2026 01:58:43 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:282eff99e7c29a63dc6bb591d774afb6da20a767bd6c7d23f0297fe8ed258150`  
		Last Modified: Tue, 07 Apr 2026 01:58:43 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b94d5939258fdc769039b55416f3d4733c30af8d8f00a88dfd39de470f98dd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140121317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9b21cda3b561ec8199533a7ff33e824ff37d3aca47df5f965fcd6ccd9cb8c7`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:02:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 07 Apr 2026 02:02:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 07 Apr 2026 02:02:08 GMT
ENV INFLUXDB_VERSION=3.9.0
# Tue, 07 Apr 2026 02:02:08 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 07 Apr 2026 02:02:08 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:02:08 GMT
USER influxdb3
# Tue, 07 Apr 2026 02:02:09 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 07 Apr 2026 02:02:09 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 07 Apr 2026 02:02:09 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 07 Apr 2026 02:02:09 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 07 Apr 2026 02:02:09 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 07 Apr 2026 02:02:09 GMT
ENV LOG_FILTER=info
# Tue, 07 Apr 2026 02:02:09 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 07 Apr 2026 02:02:09 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 02:02:09 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dd44ed741b48a3bd74bb2446858a2a539d880e0a39631d8d9cd9abce8d79d7`  
		Last Modified: Tue, 07 Apr 2026 02:02:26 GMT  
		Size: 6.7 MB (6681924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12e0b8bfcd9f52c2a62fb62e1e7bb45399098ff17b09d45dfd4fa0d469cb6ff`  
		Last Modified: Tue, 07 Apr 2026 02:02:26 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e96675d75f4f82aa32d7da302a1af0fc309e24e54f6f0de7ecd3237990a7301`  
		Last Modified: Tue, 07 Apr 2026 02:02:29 GMT  
		Size: 104.6 MB (104560995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3781080c1ef2ee81ae3b12bdc93ceb6e0f8c1d038aa969c8e316919ebd8506`  
		Last Modified: Tue, 07 Apr 2026 02:02:26 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcd63ea0fab57a82454f8a6517a0d3f5d62f69d70d96a398002f7ecbd816186`  
		Last Modified: Tue, 07 Apr 2026 02:02:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:b098fdd3c84a2217c18a0cdbfcc63401efdfa95d4e58e74ddaffb12b7ea3ae71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7d6353bb03225bc459d42991b170b05889a566977d43bccfe36635a884e60d`

```dockerfile
```

-	Layers:
	-	`sha256:f2775c1557ae4730c005dea3189f3f0e87cd21326fbe5c8b67437666c5cba61e`  
		Last Modified: Tue, 07 Apr 2026 02:02:26 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da32b5eb5402062626c5c2d097841a46e7ddeecbf6758883cd7229571951acdf`  
		Last Modified: Tue, 07 Apr 2026 02:02:26 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json
