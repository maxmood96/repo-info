## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:c03bef2aeacac5a02487eccddc4b7ef808471533a394d5dffb2744016bb58ec7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:380037170ff327b17942cc5f8dcc1b4efb0f76157547871d94c001d735cbb547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125830206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68b9b0d0f13e077217b0a5de8840003cd9e56d95fb73540618f5832ce2d7df8`
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
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
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
	-	`sha256:0ff7265f391499585cc278183024bed752f407079d183e8223c39ae5f98ea595`  
		Last Modified: Tue, 30 Sep 2025 18:07:25 GMT  
		Size: 9.1 MB (9070594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacdfe0bb6045d05ac0d03b913fceadbb39ed379d7a1ed9363ae699f0bcf1c8e`  
		Last Modified: Tue, 30 Sep 2025 18:07:25 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffcfbfe8c73d127c2f0a8cfc75e39885d1bd1e6d3268d57e106950b1cd48494`  
		Last Modified: Tue, 30 Sep 2025 18:07:36 GMT  
		Size: 87.0 MB (87032039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe13d8ac42bc18043e546de5d7fd44b43f8bfe9ccf15c4585b23fc00f4a72e0`  
		Last Modified: Tue, 30 Sep 2025 18:07:25 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7497bd338536e8bbe1749b25c9e35380859b0a6ceabe601ad50ccb82c58ad1ca`  
		Last Modified: Tue, 30 Sep 2025 18:07:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:c7b38a1c929aace5c8f5c97b6b4b1ad862ae5d6531122659753eb49f454843a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a015475e06f68efa7a6c5a11de4f5033afb3d5e701c131b03b853d9e7fba2169`

```dockerfile
```

-	Layers:
	-	`sha256:0916a676bfdc8638dca3b096daf8e6f1eede62a16969240646559f35ad8bf222`  
		Last Modified: Tue, 30 Sep 2025 20:20:41 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdc107fca4afb250d486fb452edee271568c7f9a768e44fce23313017bf76e2c`  
		Last Modified: Tue, 30 Sep 2025 20:20:42 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3a9e9c337c7b8a52234899f16cc4062a347dfffa3f592c167d4f1f0594422ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116158018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437fd253e929ed01d72edf3842fdb9fb24004ed180631ab05de4d3084a4cf34`
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
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fc7912c1c32d2a69972f80bb2dddb621d0beed4d3fcc7055f14f977a8d5ddd`  
		Last Modified: Wed, 01 Oct 2025 20:21:32 GMT  
		Size: 8.9 MB (8892548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fa5de1147b89f00f20cd21550eefa881ef18868ea3e80e50894917e986683f`  
		Last Modified: Wed, 01 Oct 2025 06:03:32 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91a4436eb3edbe14f292750b33152f54cbe9b538ffbcd231e81821815829ca5`  
		Last Modified: Wed, 01 Oct 2025 20:21:36 GMT  
		Size: 78.4 MB (78400029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06794270f48d653129e93ab604cc4696143aa2203063357411a960e5b39a59d`  
		Last Modified: Wed, 01 Oct 2025 05:53:04 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bf14d6270ccb6194f35833fc10a22d8acfb99106839de7346dd81a6dab97a9`  
		Last Modified: Wed, 01 Oct 2025 05:59:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:c9616f82343e345ed9bfc95e470bac6f36837be6e303949e7e837340d4484ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6697635951ca81e41ec3848a9cdc65d4c0b53f959201a42bd9d119e4bc10996d`

```dockerfile
```

-	Layers:
	-	`sha256:40497fe2f53f6141df0bf67ff06922a59a43cea8dd9f405e71a3781a7cf84a8c`  
		Last Modified: Wed, 01 Oct 2025 20:20:41 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6848261f96f59218cdbfb2d24e5269c0906a42e644da86ce751ba50a760dcc22`  
		Last Modified: Wed, 01 Oct 2025 20:20:41 GMT  
		Size: 17.9 KB (17920 bytes)  
		MIME: application/vnd.in-toto+json
