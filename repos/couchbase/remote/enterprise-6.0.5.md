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
