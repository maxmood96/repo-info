## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:fff26339d00a58c0002394a5ac4cc8f017fd40dcce583341158174af7ecee208
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:be6f6517972058256c36855dbc51e18323474638d3e2eb71e4d1449736e9e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162328805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a774deeeea9c1ca0aafccddcbc663572481821c633a109fdc9e68fe3731430`
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
# Fri, 10 Apr 2026 16:54:23 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 10 Apr 2026 16:54:23 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 10 Apr 2026 16:54:31 GMT
ENV INFLUXDB_VERSION=3.9.1
# Fri, 10 Apr 2026 16:54:31 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 10 Apr 2026 16:54:31 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 10 Apr 2026 16:54:31 GMT
USER influxdb3
# Fri, 10 Apr 2026 16:54:31 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 10 Apr 2026 16:54:31 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 10 Apr 2026 16:54:31 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 10 Apr 2026 16:54:31 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 10 Apr 2026 16:54:31 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 10 Apr 2026 16:54:31 GMT
ENV LOG_FILTER=info
# Fri, 10 Apr 2026 16:54:31 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 10 Apr 2026 16:54:31 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 10 Apr 2026 16:54:31 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc35ba16633ccd46619efc035bb93e9e0a5b165a1e6324cae5461e98796a8d53`  
		Last Modified: Fri, 10 Apr 2026 16:54:50 GMT  
		Size: 9.1 MB (9076490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230a8ceb03da629fab9aa91f967a2261d66038a970928d40f160486f5db7b70e`  
		Last Modified: Fri, 10 Apr 2026 16:54:50 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4b685ec9a187819c2b157bf2f6d83947385de1e959ad5ce31c4bc65f33378b`  
		Last Modified: Fri, 10 Apr 2026 16:54:52 GMT  
		Size: 123.5 MB (123514532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378055154ec206e65237b4393071c090977a796435c8f3c634219fb744cee33b`  
		Last Modified: Fri, 10 Apr 2026 16:54:50 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c59089d51e7b82d467ae3a7947f2b938a212ba619018448ef2f84a27f1cefdf`  
		Last Modified: Fri, 10 Apr 2026 16:54:51 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:21209f522745777116a457da5402334474c5b31f83587133bc67a2c36a41809a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee131cc4cf9276e801fe5b00fa7b85f3f2547b0563fa8efb7034ded982de2486`

```dockerfile
```

-	Layers:
	-	`sha256:6edc7416799d89eed5addfeb7f7d569b10f8933317b1ded2d6394b70c61e3366`  
		Last Modified: Fri, 10 Apr 2026 16:54:50 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b5f627a16ee84667dcfee89110a2adbd3017d57379844d8485cedf209b4d1a`  
		Last Modified: Fri, 10 Apr 2026 16:54:49 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:559a56e0c7441071b60322dafc9d8296cd70ec9a1aaff8d1e67726ad391cad10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152970969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13670aa5f350669534b9e93ab946137a5753a9f8b153036d30030eda2bfd0d6b`
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
# Fri, 10 Apr 2026 16:54:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Fri, 10 Apr 2026 16:54:14 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Fri, 10 Apr 2026 16:54:56 GMT
ENV INFLUXDB_VERSION=3.9.1
# Fri, 10 Apr 2026 16:54:56 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Fri, 10 Apr 2026 16:54:56 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Fri, 10 Apr 2026 16:54:56 GMT
USER influxdb3
# Fri, 10 Apr 2026 16:54:56 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Fri, 10 Apr 2026 16:54:56 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Fri, 10 Apr 2026 16:54:56 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Fri, 10 Apr 2026 16:54:56 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Fri, 10 Apr 2026 16:54:56 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Fri, 10 Apr 2026 16:54:56 GMT
ENV LOG_FILTER=info
# Fri, 10 Apr 2026 16:54:56 GMT
EXPOSE map[8181/tcp:{}]
# Fri, 10 Apr 2026 16:54:56 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Fri, 10 Apr 2026 16:54:56 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0260a15472681e4fdacf2ea43f4039917e2518194494e5a2138f616554d97a7`  
		Last Modified: Fri, 10 Apr 2026 16:54:38 GMT  
		Size: 8.9 MB (8896389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2432039e1f18b6a669104f1be001609d67f2aa8c0f8793303c77e0d6a89fdf`  
		Last Modified: Fri, 10 Apr 2026 16:54:38 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5422e774bc3caa88f7eb668d39a0aefcc73422537d3c2969960e03f3c11e495e`  
		Last Modified: Fri, 10 Apr 2026 16:55:17 GMT  
		Size: 115.2 MB (115196185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c042ccc486499678be824b3858b61ad7589529744ca41400e46a4698324e9ebd`  
		Last Modified: Fri, 10 Apr 2026 16:55:14 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993f78e98f4da2310a308f80f1bc7aa6ded5c407592e19733e5772e9a6325376`  
		Last Modified: Fri, 10 Apr 2026 16:55:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:548ba3d89aac0235fab92b527eae8b967c7878f30168713b9558e2bffe4e055f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502253966c08bf492e7712aaca5f4405cea4ccee81ea65ebca6ba0a14b13c1e2`

```dockerfile
```

-	Layers:
	-	`sha256:ffd12c5b28a62643ff01eb65e6d27fd813e613d4e8bd9bff544a6ad48454b3ef`  
		Last Modified: Fri, 10 Apr 2026 16:55:14 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8dce65cbe8a3534614406057c92385174942f69d4f4b1eafdb07d7b28383477`  
		Last Modified: Fri, 10 Apr 2026 16:55:13 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json
