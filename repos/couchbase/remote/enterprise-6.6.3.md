## `couchbase:enterprise-6.6.3`

```console
$ docker pull couchbase@sha256:0a9040b3f500519b3256487296c2b5186bda1b33c7930ad62a4a062355e69ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.6.3` - linux; amd64

```console
$ docker pull couchbase@sha256:19b1f05c0846d5e92dd0f9b9b0f97024590dfa38778643db3fcc4d33884de567
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.3 MB (537347963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb21fee92cdbe599d8833382ec853d8f37ba8dfabf63c4f9205b57c9deb3b97a`
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
# Fri, 01 Oct 2021 02:44:44 GMT
ARG CB_VERSION=6.6.3
# Fri, 01 Oct 2021 02:44:44 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3
# Fri, 01 Oct 2021 02:44:45 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb
# Fri, 01 Oct 2021 02:44:45 GMT
ARG CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa
# Fri, 01 Oct 2021 02:44:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 01 Oct 2021 02:44:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 01 Oct 2021 02:45:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:45:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 01 Oct 2021 02:45:59 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 01 Oct 2021 02:46:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 01 Oct 2021 02:46:00 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 01 Oct 2021 02:46:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 01 Oct 2021 02:46:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 01 Oct 2021 02:46:03 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 01 Oct 2021 02:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 02:46:03 GMT
CMD ["couchbase-server"]
# Fri, 01 Oct 2021 02:46:04 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 01 Oct 2021 02:46:04 GMT
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
	-	`sha256:7fc33147c66db1d3697268da5e8b4b32cd54a92de7e417f44e69e918d92774d2`  
		Last Modified: Fri, 01 Oct 2021 02:52:28 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001862f323d685a15f2d06d87e3645887de5c3662100b2c231a9d8491d74c7f4`  
		Last Modified: Fri, 01 Oct 2021 02:53:21 GMT  
		Size: 502.4 MB (502386197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9bcc94edf115c249fffc45f1420d1d2c249b6ad09008d4dc2cc802c9691357`  
		Last Modified: Fri, 01 Oct 2021 02:52:27 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca455deb1355072dd4099adf1be7430589cb4f52574e45e73792e95eb5fbf25e`  
		Last Modified: Fri, 01 Oct 2021 02:52:27 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a553b26c3f295aa040a82a5bbdd3d89d9d5b668158605546f82f8066509d0c8`  
		Last Modified: Fri, 01 Oct 2021 02:52:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239d49d19653accfab5ef39e289499bb9be76e2df1b26a241b49dd3efa3a81d2`  
		Last Modified: Fri, 01 Oct 2021 02:52:25 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ca9b12dc76380f027a0c1a38bf9320dfaa32785c1816adbb8daffd4b19d231`  
		Last Modified: Fri, 01 Oct 2021 02:52:25 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca7af8aedceefe4b261b1e7538fa0164f92419f62eb5ca90cb529d0ce64c5c7`  
		Last Modified: Fri, 01 Oct 2021 02:52:25 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d647b107e10d75436440b28500c4995fae206686454beb2702aace827a824a7f`  
		Last Modified: Fri, 01 Oct 2021 02:52:25 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
