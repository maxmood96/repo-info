## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:0452079f02f4d13fe3fbb74df3df9aefc902f58242c1b423a4d2cfb57346e199
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:88655683b666037d4d999619f0bf89959411fccf709ec5acd4e730ddcd0112b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119310544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b838c638c71c34d958e76f4eb357de3a965a3f81555e378155705660629c1f`
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
# Wed, 17 Dec 2025 23:54:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:54:04 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:54:04 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:54:04 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:54:04 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:54:04 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:54:04 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9dea577090dac77be07b9cc74c6237c4d4a29e624c7253d32ae21d6f196ae8`  
		Last Modified: Wed, 17 Dec 2025 23:54:31 GMT  
		Size: 6.7 MB (6666136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7260fb8b9949df8a568a2ab08ec327f75e8de23a1c7832b91a8b59a9eeac2`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 3.7 KB (3659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394211902e5963e29110b161e250c43839f38bbd8bf032f1f5ef5f2f518c03bf`  
		Last Modified: Wed, 17 Dec 2025 23:54:37 GMT  
		Size: 82.9 MB (82915390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27765a5b9cf865533049b2b3be0a97ae30367882b22cc708748594b5230d0c1`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de81e7d91528b57cc4c9461a0bd36737cecd98c4fdf6f346abfec658c7a6f6f5`  
		Last Modified: Wed, 17 Dec 2025 23:54:30 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a6632fbd2a97ccd27b651f4454a24353669d4e980fa305fe066f4ef9e086b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9020c2dd74bccec277cd1c5f5bbab2296e81432aa76e46a9ef5db211e8af7c1`

```dockerfile
```

-	Layers:
	-	`sha256:8253ae625ade4876b9ae4480b1fff70214e61d8395a8d4453134212328c6620c`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77fe49c85f11dbbbd310dbb808989a7dd67d8b6db212d8b5d2f9a8bd97947934`  
		Last Modified: Thu, 18 Dec 2025 00:20:37 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a30cb2b6575a0b2523585b72d3eb7ea49ba05abab0e43f2cc4e949fc23f833c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110019558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a45979608e2b37df510a125528eae572058c793c79eae7abd4ca0e7a14f3792`
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
# Wed, 17 Dec 2025 23:54:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 17 Dec 2025 23:54:56 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_VERSION=3.8.0
# Wed, 17 Dec 2025 23:55:02 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
USER influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 17 Dec 2025 23:55:02 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 17 Dec 2025 23:55:02 GMT
ENV LOG_FILTER=info
# Wed, 17 Dec 2025 23:55:02 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 17 Dec 2025 23:55:02 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 23:55:02 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ed597af36e20c4e341347d9aae17df8f44181f0198d35ae4104b1fa8301f5`  
		Last Modified: Wed, 17 Dec 2025 23:55:32 GMT  
		Size: 6.7 MB (6676586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386868f6cc91a80987c4eb312890d52e0551569d3d9f59e90df2d87577c907e5`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525e1f297447837d6c81237bfc442d0980ecb9b40ce037ec9e8fa289c41f07ff`  
		Last Modified: Wed, 17 Dec 2025 23:55:36 GMT  
		Size: 74.5 MB (74476691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ceae49e12bfe8d10edf42dc95afcd410bb8bb9967d0c7fb621c7443dc58fd0`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdcc23b7614d8487daf0da2c16fe1a93557dbc9746db244c5aeae1943a39a5f`  
		Last Modified: Wed, 17 Dec 2025 23:55:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:873150c7b0d9db1020675db32a25bdb111e7fcb72a9187c83ee6bdeb894a888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf92ef1265a6d4fedb6780ffe8e5099731b2a6b03a5767327e9b7b11564c5cbc`

```dockerfile
```

-	Layers:
	-	`sha256:2addf4befe7a325f7f12fe579dacba5749a6a51ffd81e4d600a3a89acbb076b7`  
		Last Modified: Thu, 18 Dec 2025 00:20:42 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd287962a95203141b8d424e36a291c7eb4855f3aef923fcb730c2a1ad6bc72`  
		Last Modified: Thu, 18 Dec 2025 00:20:43 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json
