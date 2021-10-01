## `couchbase:community`

```console
$ docker pull couchbase@sha256:25dcad26e1f636991900c66883821eb992e048a23111dbc1e2871eee8d21714e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:1e932d9da69584a4447352c74fc39a483c7dbb1c8ef5b61d57a563f66fa81b5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.1 MB (422108836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c2d9fd2adf73ea168a84b506f81accd98b22abb3992b53addc83b6b5897182`
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
# Fri, 01 Oct 2021 02:43:33 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb
# Fri, 01 Oct 2021 02:43:33 GMT
ARG CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277
# Fri, 01 Oct 2021 02:43:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 01 Oct 2021 02:43:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 01 Oct 2021 02:44:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:44:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 01 Oct 2021 02:44:25 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 01 Oct 2021 02:44:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 01 Oct 2021 02:44:27 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 01 Oct 2021 02:44:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 01 Oct 2021 02:44:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.1-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.1 CB_SHA256=1e20fbac5a10573c999f20f313f89bb1f40848f66f6eabb853731f5853c23277 CB_VERSION=7.0.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 01 Oct 2021 02:44:29 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 01 Oct 2021 02:44:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 02:44:30 GMT
CMD ["couchbase-server"]
# Fri, 01 Oct 2021 02:44:30 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 01 Oct 2021 02:44:30 GMT
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
	-	`sha256:d3fee784dcb4da06afc558c0024271564f6b53b4478ab5d65bba51fdf530d443`  
		Last Modified: Fri, 01 Oct 2021 02:51:25 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bcf82535e1026694a3a7d6096c71c1a561eee67be2d9485016fa7630188104`  
		Last Modified: Fri, 01 Oct 2021 02:52:15 GMT  
		Size: 387.1 MB (387147063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b620074e2d8ee2e1291767e39da66a50c92ee16d9c4b01a1f9a880c52a4d073`  
		Last Modified: Fri, 01 Oct 2021 02:51:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b8a8fb636a239836a0ee704182025e455a01798c706156c1cf96492c36de62`  
		Last Modified: Fri, 01 Oct 2021 02:51:25 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c085abdbd18d4a180767b0bb6d422992cbff1bbf1e0d9bc49abc0ececf6366f`  
		Last Modified: Fri, 01 Oct 2021 02:51:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79d31952c6af1b3c05798f14692bf01983508dbbdc8860f686ecfb136d7ec81`  
		Last Modified: Fri, 01 Oct 2021 02:51:23 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b743a0253de9b81e22c7c0ce77bca9ffb7f52aea5ebcc42fe00c0c574f6b59f9`  
		Last Modified: Fri, 01 Oct 2021 02:51:23 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654b628d33be94134859e10d598d093fe725dc6ab4f3afd4af61a94a30081796`  
		Last Modified: Fri, 01 Oct 2021 02:51:23 GMT  
		Size: 125.9 KB (125896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aff8896502518a00c3c52edd93f580b02bbc16757ebca279ac458d2ab8ce828`  
		Last Modified: Fri, 01 Oct 2021 02:51:23 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
