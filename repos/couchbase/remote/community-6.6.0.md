## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:4ba1de8c6fb880f5d7b99d713a3314e600ce9c3638ae844505d09d2eda0d123a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:f31f8dac3e452b223d5e6f5ef0463a6677d9e6ecd29318f498953bb49cfad105
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371369603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91876cdf9a3c516ec4f0dc96d19625181f50dc02c7e034ee37fc16838858cdf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 22:45:39 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Wed, 25 Nov 2020 22:46:11 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 25 Nov 2020 22:46:12 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 25 Nov 2020 22:46:13 GMT
ARG CB_VERSION=6.6.0
# Wed, 25 Nov 2020 22:46:13 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Wed, 25 Nov 2020 22:47:25 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb
# Wed, 25 Nov 2020 22:47:25 GMT
ARG CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e
# Wed, 25 Nov 2020 22:47:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 25 Nov 2020 22:47:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 25 Nov 2020 22:48:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Wed, 25 Nov 2020 22:48:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 25 Nov 2020 22:48:09 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 25 Nov 2020 22:48:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chown -R couchbase:couchbase /etc/service
# Wed, 25 Nov 2020 22:48:11 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 25 Nov 2020 22:48:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 25 Nov 2020 22:48:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 25 Nov 2020 22:48:13 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 25 Nov 2020 22:48:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Nov 2020 22:48:13 GMT
CMD ["couchbase-server"]
# Wed, 25 Nov 2020 22:48:13 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 25 Nov 2020 22:48:14 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b76493b3caecb904171853015f3fc5289aa41102eb601ca305e308a0c029a7a`  
		Last Modified: Wed, 25 Nov 2020 22:50:57 GMT  
		Size: 5.8 MB (5834346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f0ce3dc9a387216c00866898412832b5c2783e48992c356a9af018ccd249d3`  
		Last Modified: Wed, 25 Nov 2020 22:52:12 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1c7b6348acbc1f2f7cdbd6390a0e3ac36ed232c86d4be6ba87866a7dbea2c3`  
		Last Modified: Wed, 25 Nov 2020 22:52:54 GMT  
		Size: 319.6 MB (319572975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea110ea3e040868c421fc42b048a33fee24f2715e41cbf8e49c85da774d6bc14`  
		Last Modified: Wed, 25 Nov 2020 22:52:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a07649780e353e60fe9f9bb6b6a78c35f414bfa4845b2f56f14fd49b967668d`  
		Last Modified: Wed, 25 Nov 2020 22:52:12 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1323b9c7bc2ec882f4fc3c4bc08c90a28d16e97d76c1245be6213086e9956f`  
		Last Modified: Wed, 25 Nov 2020 22:52:10 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b822fc07d7f54725cbb0ca47f35bb97e6fa59651bbaa689c5ae012fb2b87f53`  
		Last Modified: Wed, 25 Nov 2020 22:52:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc851f6d84f9953686ef187cac217f6c60444509ca4529fddf30cb12ddd6acdf`  
		Last Modified: Wed, 25 Nov 2020 22:52:10 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162030f9c55dec456d44b858afc331715aebcfa251c949f8bd13ba5686205e5`  
		Last Modified: Wed, 25 Nov 2020 22:52:10 GMT  
		Size: 118.1 KB (118072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53edd4ed8088122cdb7fc911c735b990688cc9ddef37df6904f7ec92d40279c`  
		Last Modified: Wed, 25 Nov 2020 22:52:10 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
