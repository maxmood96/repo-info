## `couchbase:community-7.0.0-beta`

```console
$ docker pull couchbase@sha256:a2bc32811725b7fe540f5642d53d748a79c1dc6553c94cfbf3293b432a87b1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:85faac87565b6a7df0ca725d5dc45ba970242ed74c41ff8fdbaa20ff66de0584
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.7 MB (431741040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed049ca0440cb6b0a8291d4acba995fae9f9c60f7bb0e450b402834f961f07f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 03:55:03 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 04 Mar 2021 03:55:22 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Mar 2021 03:55:23 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_VERSION=7.0.0-beta
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Thu, 04 Mar 2021 03:57:05 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb
# Thu, 04 Mar 2021 03:57:05 GMT
ARG CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991
# Thu, 04 Mar 2021 03:57:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 04 Mar 2021 03:57:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 04 Mar 2021 03:57:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 04 Mar 2021 03:57:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 04 Mar 2021 03:57:57 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 04 Mar 2021 03:57:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Thu, 04 Mar 2021 03:57:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 04 Mar 2021 03:57:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 04 Mar 2021 03:58:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 04 Mar 2021 03:58:01 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 04 Mar 2021 03:58:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Mar 2021 03:58:01 GMT
CMD ["couchbase-server"]
# Thu, 04 Mar 2021 03:58:01 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 04 Mar 2021 03:58:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9554fabf446c196bafd3140fe0a097c18e9f37bbaf3cb5b15933313d851455`  
		Last Modified: Thu, 04 Mar 2021 03:58:33 GMT  
		Size: 6.3 MB (6270368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee35028997dc022a748113806b8b124d8026bb6fe05278a69d0f4f0015edeff0`  
		Last Modified: Thu, 04 Mar 2021 03:58:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac97cfd68ae5267152e20902e4cc08fa0717ad00023059759d04a81af279fde5`  
		Last Modified: Thu, 04 Mar 2021 03:59:58 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a132f9a6b823c1a7298bc813eefe6858742665e722f384cc106b9ced210549ec`  
		Last Modified: Thu, 04 Mar 2021 04:00:50 GMT  
		Size: 396.8 MB (396771769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bb4ac087debbc196fe9531123ae5cfaa58f0abbd4923fbb9f506201178363d`  
		Last Modified: Thu, 04 Mar 2021 03:59:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3b1e50b5d32bdb9a826a6da1fc2a553db224cab0f088fc3e096b7f3c5e1395`  
		Last Modified: Thu, 04 Mar 2021 03:59:57 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127f54f45844b254ee4b8a4496a68364e81866eff9002bd3a65f6b224409d48`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211844bc0f5dfba158ec00b9c77f62f911b2d0a6b18c75d7f68dcead78c56672`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f31c9d95a167db27a0c5180e439073278e0717592c2cc9ad0567bc98bfaed9`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f9621f558fe62fdc941b899732dd67a87a527511c095c3bd3805d166580598`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 125.9 KB (125893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b80e85638811db6df49794e05278d4a21ad0d91cd6d5f33ac225b54570e247`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
