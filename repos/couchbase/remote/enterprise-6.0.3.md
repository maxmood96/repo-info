## `couchbase:enterprise-6.0.3`

```console
$ docker pull couchbase@sha256:a038a021838245ad03b205c20819a1c4a172391f71c543c372de01b7162870ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:416d6c38a585cf54a94da8488b5765e1fff8e15f0f435eceee22e4038f42efe4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.9 MB (465900534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae2e82909bcfa2602a49ef3714ddca1808aa40e7468ff089a69cbf9952ecb27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Mon, 03 May 2021 21:29:19 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 03 May 2021 21:31:22 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 03 May 2021 21:31:23 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Mon, 03 May 2021 21:38:41 GMT
ARG CB_VERSION=6.0.3
# Mon, 03 May 2021 21:38:42 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Mon, 03 May 2021 21:38:42 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb
# Mon, 03 May 2021 21:38:42 GMT
ARG CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382
# Mon, 03 May 2021 21:38:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 03 May 2021 21:38:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 03 May 2021 21:39:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 03 May 2021 21:39:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 03 May 2021 21:39:52 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Mon, 03 May 2021 21:39:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Mon, 03 May 2021 21:39:53 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 03 May 2021 21:39:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 03 May 2021 21:39:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Mon, 03 May 2021 21:39:55 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Mon, 03 May 2021 21:39:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 May 2021 21:39:55 GMT
CMD ["couchbase-server"]
# Mon, 03 May 2021 21:39:56 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Mon, 03 May 2021 21:39:56 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a5e3b266c9cede3a2db2b05b38059ce28348de3265d3361af2cecd8c3b785`  
		Last Modified: Mon, 03 May 2021 21:49:21 GMT  
		Size: 15.9 MB (15923990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b7a466899d0d77228f1a71bf00869b2ba0f5d1c50be62f0640c58cd1d4c065`  
		Last Modified: Mon, 03 May 2021 21:49:15 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28dc10cfe5c3e678b028106e9ba0004892c2c5c199fd80062e1ebedf17fa017`  
		Last Modified: Mon, 03 May 2021 21:56:08 GMT  
		Size: 2.0 KB (1971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b95d95540957f2730833511b6dc194cf2d7c847ce413f2d584476a4b2f2f988`  
		Last Modified: Mon, 03 May 2021 21:56:50 GMT  
		Size: 423.1 MB (423148429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb3f10e251ede8bc05b4f28dcb07fa0008c95a61a899b9ecdcd1ba79b99e87e`  
		Last Modified: Mon, 03 May 2021 21:56:08 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7edf000641cb043022963ea1cac64736443c1f944730f066aff9586debccd`  
		Last Modified: Mon, 03 May 2021 21:56:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4721735be05f5a634fcd21b1e4d40022387ee3e2ae62fae9d3b7da639f459cb9`  
		Last Modified: Mon, 03 May 2021 21:56:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c37fa412b7b22aea5cee0ce1e93668e040ae10b7b3e1621b73fc894fcaa48`  
		Last Modified: Mon, 03 May 2021 21:56:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b44befd8be82bdf8285f356a76cc70ab1dbf7795544f6aad2fdcdb4f3c5895`  
		Last Modified: Mon, 03 May 2021 21:56:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13124361f3438162b98be3032eeacfeac19ee0fcb271dd01ce180a45321ae0ab`  
		Last Modified: Mon, 03 May 2021 21:56:06 GMT  
		Size: 125.6 KB (125564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e990904e21d013a3a2369ab9539601fc54f66da2d26a223f1bd0ea44d7eaeb`  
		Last Modified: Mon, 03 May 2021 21:56:05 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
