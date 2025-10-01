## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:a6ffd19f9c1cec90c00e83b60e1882c17d91235dae70b397d0f12ff7e4dc2f6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

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

### `influxdb:3-enterprise` - unknown; unknown

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

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:49b06572ed51033ab384673ac640e7efb021dc7ea64244077c0eaece0ac7e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.9 MB (111864713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bff344b48f080250935ce5d2295f18d545a3573179f7e245805604e9439b16`
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
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
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
	-	`sha256:63986cf6045810298066b4a7dd264d5d2c4422ffbf792a0414c4a3e642d30233`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 6.7 MB (6676493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d79724c215b55fae9017081e43d63d95ab2d5a85837f4314a4a92798e224e7`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fe097ce79f895e72472cdda7d81b7899b9bdc0d6456fb32b9e8642bda053f8`  
		Last Modified: Wed, 24 Sep 2025 20:42:22 GMT  
		Size: 76.3 MB (76322772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d19e7c3caecb655f5bb0efae2e98421f664d7dab14dab4a26f7944a1978869`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8ea903490ced720b738540ced6dcb212a180c4737fa8ff6b79455d3ff80e52`  
		Last Modified: Wed, 24 Sep 2025 20:42:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:d79dee4273d7b3f5e8d2bd0c0217b54004298bfb1f00b3547b4a00be30077962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee20f57b35fecbed61eb6d90c344087dcf6df70773eae21e59ec4c1195378f6f`

```dockerfile
```

-	Layers:
	-	`sha256:38671e81d3c25beb088deb3fb376c7077da8de731cf5336e28ca1d665461228f`  
		Last Modified: Thu, 25 Sep 2025 02:22:33 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b53831b7bc512d53a7b7be3c225fa3602fcb7e1e9f344bd1e5b920d4380b1d`  
		Last Modified: Thu, 25 Sep 2025 02:22:34 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json
