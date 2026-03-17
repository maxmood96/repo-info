## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:659da4d6af9a37902819986a2fd489b0f6f2ed454e6822ebb7937ca99f2dbf56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0068439a849d0a8a75d5bf31109518822189e0a91205428cc4dabbe07adbecad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128390942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e95f3a3854771047f8c42216606eedeede2dd0e6bd68ff406622594620b048`
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
# Tue, 17 Mar 2026 01:39:16 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:39:17 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB_VERSION=3.8.4
# Tue, 17 Mar 2026 01:39:24 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:39:24 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:39:24 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:39:24 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:39:24 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:24 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896f80de69282718f797c732aadcb5ad7cb525eba98ad4a175031054cf4c4e18`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 6.7 MB (6671643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61664b8c9e70a8f737b8374de8a43c17a6e7ed951ea3405ae356ff8ac1504c2c`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1361daea27f76c6bf56c08ba7564ae65156ecb8e251185ccf018f686904d8a`  
		Last Modified: Tue, 17 Mar 2026 01:39:42 GMT  
		Size: 92.0 MB (91982987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bd0ef6e31704dc021b0a98036ab976fb486d924c03223094882b49fc16927c`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f1bceff72da4ddca28a5cd3c12dfb8fcedcb2836202ab2c5ed2c96f3f2ed8`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ea34b829420e68babbc9e10a485b40864a22cf629cca20295def1c06bc64d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42083b11801171ad943480cd34dc1cefdae0725c8038f3efa8bfec30dcdf30`

```dockerfile
```

-	Layers:
	-	`sha256:26b0a0947e306cff33e0baf6ef78e411ba1dc193e9b5199f2a4c37878542d860`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 2.3 MB (2310635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec22d992ae8949247335d9458549ad1e329d7740a6448e282ca6d1882ab71ab0`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e71c1877459a80a96b782a6700ab975468ed7c160f8b8aba45d54011f06c2bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119034746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f99105f51447acc10566cad4da5c9dd93e87600aea5786c58c1b91b2deba254`
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
# Tue, 17 Mar 2026 01:40:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:40:28 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB_VERSION=3.8.4
# Tue, 17 Mar 2026 01:40:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:40:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:40:35 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:40:35 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:40:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c9b202493abf56134337b459be8acb07328c6f25892605d440c7f265df6a7b`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 6.7 MB (6681738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4286e69af75bf4ff096601e07ac6fe12af7d7bccaa18225bb29036d2f2503c53`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fff946bce4cefe39db32464b13a52437398b2f8c8bbe74de3121fc2127f368`  
		Last Modified: Tue, 17 Mar 2026 01:40:51 GMT  
		Size: 83.5 MB (83478973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c48ae972e761f8f9851eeed70d099301714e48a925d5b45dd64fbe150592c6`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 523.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db91e6bd4f3aac338c3aab1210b06acfb137b4ae2fbf6ef74298b77b4d43a83`  
		Last Modified: Tue, 17 Mar 2026 01:40:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:5606f14d9173824d7f4dc14323f0db97097ef4ec2f886c3399be7055a68782bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a41e5b6195df8732b06f84032c50c76d3ee58f41e79e1fd31787622cbbefdd`

```dockerfile
```

-	Layers:
	-	`sha256:c2ef077fcbcf2aa087d7b258518807849f8bc051379a75b23bfb92e88b51d361`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 2.3 MB (2311717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0071489710411d8fa4dd7b44c485227d6ceac8e7c15cd9cb0ac28ad1b57f52cb`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json
