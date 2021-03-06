## `couchbase:enterprise-6.6.1`

```console
$ docker pull couchbase@sha256:0e6c5afdb09418924d07e1675837b82fe6168a1d02dd5f75812a693af19ade0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:e6453787c735d23ded5504f1a7fce55e95399867e6e2a6287c726ee9110b7eba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.4 MB (544422547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077655b95dda98ce27e330dc07290eff2f269fd45331a27c9d971d0f3ab46aa6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Fri, 05 Mar 2021 23:21:18 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Fri, 05 Mar 2021 23:21:51 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 05 Mar 2021 23:21:52 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 05 Mar 2021 23:21:53 GMT
ARG CB_VERSION=6.6.1
# Fri, 05 Mar 2021 23:21:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1
# Fri, 05 Mar 2021 23:21:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb
# Fri, 05 Mar 2021 23:21:53 GMT
ARG CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9
# Fri, 05 Mar 2021 23:21:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 05 Mar 2021 23:21:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 05 Mar 2021 23:22:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 05 Mar 2021 23:22:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 05 Mar 2021 23:22:45 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 05 Mar 2021 23:22:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chown -R couchbase:couchbase /etc/service
# Fri, 05 Mar 2021 23:22:47 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 05 Mar 2021 23:22:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 05 Mar 2021 23:22:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 05 Mar 2021 23:22:49 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 05 Mar 2021 23:22:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Mar 2021 23:22:49 GMT
CMD ["couchbase-server"]
# Fri, 05 Mar 2021 23:22:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 05 Mar 2021 23:22:49 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5898a8dc0081c6bc55e45b06eeb478718117d9b9e07f1b0bc0540f0c6f4b75fb`  
		Last Modified: Sat, 06 Mar 2021 06:47:20 GMT  
		Size: 5.8 MB (5833934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916116bb82f85763fa4d126bef2416aa666a51cd4af4901f2fe301bf09aa61a5`  
		Last Modified: Sat, 06 Mar 2021 06:47:18 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997b43eee325ba9e125b4fe9b1cc5fd40732a165ba3b4d1fa7800f680ed327ab`  
		Last Modified: Sat, 06 Mar 2021 06:48:17 GMT  
		Size: 492.5 MB (492502216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f6a6746074d2b9378f7e20a7db1287ea80d6ce913db9b5472d56ffa5396a34`  
		Last Modified: Sat, 06 Mar 2021 06:47:17 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a73bbb3e8e09652e989f9a72df280ad044dff002ffc8608fe9533fc04a0b48`  
		Last Modified: Sat, 06 Mar 2021 06:47:17 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fa1e0cbe3e2bf04160fa39a785bf01841c506dea37f77f19cc3126a0e415c7`  
		Last Modified: Sat, 06 Mar 2021 06:47:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034022485c80c67fae060607df5dfc33b2daedc0900d4a7f806df6c6ed0e7469`  
		Last Modified: Sat, 06 Mar 2021 06:47:15 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bde3204c6d5fbd8fc56fe770bf2bbee57bd6c6a3ae812b39ec7fb6344210425`  
		Last Modified: Sat, 06 Mar 2021 06:47:15 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a21edcf8773c2ccee6b42f5a2dcf5df8f839f0fdd7fa6bfca29522d6b1cd26`  
		Last Modified: Sat, 06 Mar 2021 06:47:15 GMT  
		Size: 118.1 KB (118075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02a75919f4d80228fdcf264800cbc9659caf46428171c11e4e87abff19da544`  
		Last Modified: Sat, 06 Mar 2021 06:47:15 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
