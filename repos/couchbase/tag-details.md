<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.0.5`](#couchbase605)
-	[`couchbase:6.6.3`](#couchbase663)
-	[`couchbase:7.0.1`](#couchbase701)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.6.0`](#couchbasecommunity-660)
-	[`couchbase:community-7.0.1`](#couchbasecommunity-701)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.0.5`](#couchbaseenterprise-605)
-	[`couchbase:enterprise-6.6.3`](#couchbaseenterprise-663)
-	[`couchbase:enterprise-7.0.1`](#couchbaseenterprise-701)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.0.5`

```console
$ docker pull couchbase@sha256:f7367d3afa61523b212b188b2180489014d9f2fda592d5423db7721c64d8c11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:192ee4cbb0554bdc6fd470dba43e72b21a3fdc31c0d1b803f268b5ac01ede908
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466121342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe105794e8b009d8881de173968dd3e0beaa0cb7b92823d6d0923fca3089adb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:46:10 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 01 Oct 2021 02:48:17 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:48:18 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 01 Oct 2021 02:48:19 GMT
ARG CB_VERSION=6.0.5
# Fri, 01 Oct 2021 02:48:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Fri, 01 Oct 2021 02:48:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Fri, 01 Oct 2021 02:48:19 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Fri, 01 Oct 2021 02:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 01 Oct 2021 02:48:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 01 Oct 2021 02:49:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:49:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 01 Oct 2021 02:49:21 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 01 Oct 2021 02:49:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 01 Oct 2021 02:49:22 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 01 Oct 2021 02:49:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 01 Oct 2021 02:49:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 01 Oct 2021 02:49:24 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 01 Oct 2021 02:49:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 02:49:25 GMT
CMD ["couchbase-server"]
# Fri, 01 Oct 2021 02:49:25 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 01 Oct 2021 02:49:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7533055455fc3b7edab1b7d1a254e5048632115db3ed069e464a9f70b46f9701`  
		Last Modified: Fri, 01 Oct 2021 02:54:27 GMT  
		Size: 15.9 MB (15923249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1101292f94db4a63208276d651c0e7aefbf97c3c251c37fd3ed1589de11b8256`  
		Last Modified: Fri, 01 Oct 2021 02:54:23 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5158df84771ac1ab261a6fc30d9f422d4096eca3399d47d1bd563a998fa8929`  
		Last Modified: Fri, 01 Oct 2021 02:54:22 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48c9e9bde3e55d56cbbc3043140d87c593e1862ac0ef784e25c525f90fb3867`  
		Last Modified: Fri, 01 Oct 2021 02:55:02 GMT  
		Size: 423.4 MB (423362973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0e391c7a9a7cc6b458c7e5bee36ffe1abb7751253533e1d7fb7321c07cbb1a`  
		Last Modified: Fri, 01 Oct 2021 02:54:22 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5547d6ef3793148e40087c50a166c4789e06fd3bc0e804caa204fe87e2b8363`  
		Last Modified: Fri, 01 Oct 2021 02:54:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc4ef267815398c6a0295a86023660d9edaa17a43b72fb485b20b834ed9f395`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2e6c182c0b9532500fd2b68eff31064940290cccbdfcaca3cfdb1ec9fe7809`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8243cd47a1656c57e01fb7d79bd1472b3b9e82f0b8a60ffdef25f2d8b00b4b26`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c87f7b248d9297630c286186f37bb21b3139a825473a75a09b7c88438e429fd`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 125.6 KB (125557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83eb17d4605e78b6b469806e8abcfc577253ea890fe8859206c383f57fbb6ccf`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.6.3`

```console
$ docker pull couchbase@sha256:0a9040b3f500519b3256487296c2b5186bda1b33c7930ad62a4a062355e69ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:6.6.3` - linux; amd64

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

## `couchbase:7.0.1`

```console
$ docker pull couchbase@sha256:fdc30c24c6a03cccbd47dbc064360c8ccbcee087d3e22733f5cfe264001470a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:7.0.1` - linux; amd64

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

## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:aa1d1ecb1c9acf92eb9dba4fd5a3be27732873489ce12f06dcb7505bdad5bd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:f37cccde0714e86e0a3cd0a0c97c4a0a3cf1b03b96889fa8fb0b884e08e69e2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354217687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892ead5439a2e0678c39beac392508fc6ed5db3913320189829c30b1dca40bac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:46:10 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 01 Oct 2021 02:46:44 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:46:45 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 01 Oct 2021 02:46:45 GMT
ARG CB_VERSION=6.6.0
# Fri, 01 Oct 2021 02:46:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Fri, 01 Oct 2021 02:46:46 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb
# Fri, 01 Oct 2021 02:46:46 GMT
ARG CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559
# Fri, 01 Oct 2021 02:46:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 01 Oct 2021 02:46:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 01 Oct 2021 02:47:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:47:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 01 Oct 2021 02:47:37 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 01 Oct 2021 02:47:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 01 Oct 2021 02:47:38 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 01 Oct 2021 02:47:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 01 Oct 2021 02:47:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 01 Oct 2021 02:47:39 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 01 Oct 2021 02:47:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 02:47:40 GMT
CMD ["couchbase-server"]
# Fri, 01 Oct 2021 02:47:40 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 01 Oct 2021 02:47:40 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7178ada3bd73aa22d37d77aa136877737ee4011b10f2b5491bcf219a3a19748c`  
		Last Modified: Fri, 01 Oct 2021 02:53:37 GMT  
		Size: 7.4 MB (7371489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e73dd26d67d7da2e2befe37ab77651e48cd18cf43ed4c858263d9470517a15`  
		Last Modified: Fri, 01 Oct 2021 02:53:34 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c411f8d03c30662fcf56518f0a72d017871e6f25a52a2772060a391c86282ae`  
		Last Modified: Fri, 01 Oct 2021 02:53:34 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f502a2583d022678ba882b83325f622633840be055d51ec59aa773ee12bb67c8`  
		Last Modified: Fri, 01 Oct 2021 02:54:12 GMT  
		Size: 320.0 MB (320018444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a38d674cffc30e7883414b19c151e05c98c969be1e26986fc4f0f9af59398f`  
		Last Modified: Fri, 01 Oct 2021 02:53:34 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd1ce8cfac06dd358c19fb4ad8c4f0d3243934efe2a699612249f0ff92cc540`  
		Last Modified: Fri, 01 Oct 2021 02:53:34 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65037115b1fb0270bd3facc9fbf4b72533b46bc766a7d324d37326e418787ee7`  
		Last Modified: Fri, 01 Oct 2021 02:53:32 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b2f5d17a30c0613666f64eee4029e7c89c43c1c9615747c909f01b1289272e`  
		Last Modified: Fri, 01 Oct 2021 02:53:31 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f75fd1fb20db52b01d1d77c7ef924a48dfd6b0c5549505626ed49af5cc707e`  
		Last Modified: Fri, 01 Oct 2021 02:53:32 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbffe15c5f9ca3a1da255be0641f813436e87681652d18b939e821d4aa5dcacf`  
		Last Modified: Fri, 01 Oct 2021 02:53:32 GMT  
		Size: 118.2 KB (118189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08208822bdae9d3fd0a0a7e9e36574647c9e2048111154fc33f88a3c414c2ef2`  
		Last Modified: Fri, 01 Oct 2021 02:53:31 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.1`

```console
$ docker pull couchbase@sha256:25dcad26e1f636991900c66883821eb992e048a23111dbc1e2871eee8d21714e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.1` - linux; amd64

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

## `couchbase:enterprise-6.0.5`

```console
$ docker pull couchbase@sha256:f7367d3afa61523b212b188b2180489014d9f2fda592d5423db7721c64d8c11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:192ee4cbb0554bdc6fd470dba43e72b21a3fdc31c0d1b803f268b5ac01ede908
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466121342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe105794e8b009d8881de173968dd3e0beaa0cb7b92823d6d0923fca3089adb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:46:10 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 01 Oct 2021 02:48:17 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:48:18 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 01 Oct 2021 02:48:19 GMT
ARG CB_VERSION=6.0.5
# Fri, 01 Oct 2021 02:48:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Fri, 01 Oct 2021 02:48:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Fri, 01 Oct 2021 02:48:19 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Fri, 01 Oct 2021 02:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 01 Oct 2021 02:48:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 01 Oct 2021 02:49:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 01 Oct 2021 02:49:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 01 Oct 2021 02:49:21 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 01 Oct 2021 02:49:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 01 Oct 2021 02:49:22 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 01 Oct 2021 02:49:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 01 Oct 2021 02:49:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 01 Oct 2021 02:49:24 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 01 Oct 2021 02:49:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 02:49:25 GMT
CMD ["couchbase-server"]
# Fri, 01 Oct 2021 02:49:25 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 01 Oct 2021 02:49:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7533055455fc3b7edab1b7d1a254e5048632115db3ed069e464a9f70b46f9701`  
		Last Modified: Fri, 01 Oct 2021 02:54:27 GMT  
		Size: 15.9 MB (15923249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1101292f94db4a63208276d651c0e7aefbf97c3c251c37fd3ed1589de11b8256`  
		Last Modified: Fri, 01 Oct 2021 02:54:23 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5158df84771ac1ab261a6fc30d9f422d4096eca3399d47d1bd563a998fa8929`  
		Last Modified: Fri, 01 Oct 2021 02:54:22 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48c9e9bde3e55d56cbbc3043140d87c593e1862ac0ef784e25c525f90fb3867`  
		Last Modified: Fri, 01 Oct 2021 02:55:02 GMT  
		Size: 423.4 MB (423362973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0e391c7a9a7cc6b458c7e5bee36ffe1abb7751253533e1d7fb7321c07cbb1a`  
		Last Modified: Fri, 01 Oct 2021 02:54:22 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5547d6ef3793148e40087c50a166c4789e06fd3bc0e804caa204fe87e2b8363`  
		Last Modified: Fri, 01 Oct 2021 02:54:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc4ef267815398c6a0295a86023660d9edaa17a43b72fb485b20b834ed9f395`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2e6c182c0b9532500fd2b68eff31064940290cccbdfcaca3cfdb1ec9fe7809`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8243cd47a1656c57e01fb7d79bd1472b3b9e82f0b8a60ffdef25f2d8b00b4b26`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c87f7b248d9297630c286186f37bb21b3139a825473a75a09b7c88438e429fd`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 125.6 KB (125557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83eb17d4605e78b6b469806e8abcfc577253ea890fe8859206c383f57fbb6ccf`  
		Last Modified: Fri, 01 Oct 2021 02:54:20 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `couchbase:enterprise-7.0.1`

```console
$ docker pull couchbase@sha256:fdc30c24c6a03cccbd47dbc064360c8ccbcee087d3e22733f5cfe264001470a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.0.1` - linux; amd64

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

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:fdc30c24c6a03cccbd47dbc064360c8ccbcee087d3e22733f5cfe264001470a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:latest` - linux; amd64

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
