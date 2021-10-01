## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:fdc30c24c6a03cccbd47dbc064360c8ccbcee087d3e22733f5cfe264001470a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:b549e0f5178a59d92377334a30e2cd6a3b5c60f84ee25dfbcf6430a90c354b19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 MB (632989728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3347b401c475a23e893f7d821824efe059ca46075d018e3c236d68808478f9ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:41:23 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 01 Oct 2021 02:41:49 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:41:50 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 01 Oct 2021 02:41:50 GMT
ARG CB_VERSION=7.0.1
# Fri, 01 Oct 2021 02:41:51 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1
# Fri, 01 Oct 2021 02:41:51 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.1-ubuntu20.04_amd64.deb
# Fri, 01 Oct 2021 02:41:51 GMT
ARG CB_SHA256=65b93029008271d47ec1a8b14194c604c461a2766f51252e25206cfcb7869b61
# Fri, 01 Oct 2021 02:41:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 01 Oct 2021 02:41:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=65b93029008271d47ec1a8b14194c604c461a2766f51252e25206cfcb7869b61 CB_VERSION=7.0.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 01 Oct 2021 02:43:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=65b93029008271d47ec1a8b14194c604c461a2766f51252e25206cfcb7869b61 CB_VERSION=7.0.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:43:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=65b93029008271d47ec1a8b14194c604c461a2766f51252e25206cfcb7869b61 CB_VERSION=7.0.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 01 Oct 2021 02:43:11 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 01 Oct 2021 02:43:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=65b93029008271d47ec1a8b14194c604c461a2766f51252e25206cfcb7869b61 CB_VERSION=7.0.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 01 Oct 2021 02:43:12 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 01 Oct 2021 02:43:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=65b93029008271d47ec1a8b14194c604c461a2766f51252e25206cfcb7869b61 CB_VERSION=7.0.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 01 Oct 2021 02:43:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=65b93029008271d47ec1a8b14194c604c461a2766f51252e25206cfcb7869b61 CB_VERSION=7.0.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 01 Oct 2021 02:43:14 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 01 Oct 2021 02:43:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 02:43:14 GMT
CMD ["couchbase-server"]
# Fri, 01 Oct 2021 02:43:15 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 01 Oct 2021 02:43:15 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613d9cf3c7de3b660067509bdefdbe2edc5d448de2122399663ad4f10564ff7`  
		Last Modified: Fri, 01 Oct 2021 02:49:55 GMT  
		Size: 6.3 MB (6262599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6d1844f56aa2609795f15f46bc684d4d477f33fc1c0a486595f0449d80d14`  
		Last Modified: Fri, 01 Oct 2021 02:49:50 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac42b0499b76bb5138aadf101d6daae53ca0ba6600cbd9748a80502facd8265`  
		Last Modified: Fri, 01 Oct 2021 02:49:50 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f989388386ccef595927eb55cd3e66143fbe2d2aa41fadb3ea9aca5c57f9239b`  
		Last Modified: Fri, 01 Oct 2021 02:51:06 GMT  
		Size: 598.0 MB (598027964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce038e7b79a9b043733e7b88d831e2f36bdaa1297ebf5ad8dad18edac7284d00`  
		Last Modified: Fri, 01 Oct 2021 02:49:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a8be79ee93495787c3ce1ed48faf9e9f05f03dd397d0dcf08a53facaed0cf`  
		Last Modified: Fri, 01 Oct 2021 02:49:50 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4353012a94c13fcfae569fc66668553aa4abb39f49318f0f4bfe263c8532a`  
		Last Modified: Fri, 01 Oct 2021 02:49:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743055564b2713d4559700e95a98bb4e21ff0d7d4a09354e43b8ac57a8c714a0`  
		Last Modified: Fri, 01 Oct 2021 02:49:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc59de1034fdf768ae2f8e9831ab2814dbd5cb8803472919b2e2c06612220cc`  
		Last Modified: Fri, 01 Oct 2021 02:49:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a83d46963197d6d696a5f71a286bd0df88b51aa349c7bbede0532d051ee499`  
		Last Modified: Fri, 01 Oct 2021 02:49:48 GMT  
		Size: 125.9 KB (125889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0feca3548859843f73376251f8ac2531b1e4e520a3f1c99917fcc33625ba817a`  
		Last Modified: Fri, 01 Oct 2021 02:49:48 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
