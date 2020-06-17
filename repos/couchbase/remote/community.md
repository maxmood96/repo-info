## `couchbase:community`

```console
$ docker pull couchbase@sha256:8c20c3907b77db98f19b68c32ab910c1cd2cec66f203065798383e67eb66da9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:f4399ddacc4dc0b0b4a4bbd60bf50c23bd75e2721f361623774d5ed9fbeea9c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367262652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eacc1bbf53d197f1fe919fd3ee54e51e27884432b36dd8090677dd183ed198e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 02:17:49 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Wed, 17 Jun 2020 02:18:08 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 17 Jun 2020 02:18:08 GMT
ARG CB_VERSION=6.5.1
# Wed, 17 Jun 2020 02:18:08 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Wed, 17 Jun 2020 02:21:23 GMT
ARG CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb
# Wed, 17 Jun 2020 02:21:23 GMT
ARG CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7
# Wed, 17 Jun 2020 02:21:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 17 Jun 2020 02:21:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 17 Jun 2020 02:22:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Wed, 17 Jun 2020 02:22:24 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 17 Jun 2020 02:22:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN chown -R couchbase:couchbase /etc/service
# Wed, 17 Jun 2020 02:22:26 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 17 Jun 2020 02:22:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 17 Jun 2020 02:22:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 17 Jun 2020 02:22:29 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 17 Jun 2020 02:22:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jun 2020 02:22:29 GMT
CMD ["couchbase-server"]
# Wed, 17 Jun 2020 02:22:30 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 17 Jun 2020 02:22:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ed1564efbf96a9ca1500eab90f863e8b0dae5f2a372246d5d8ed737d617809`  
		Last Modified: Wed, 17 Jun 2020 02:22:48 GMT  
		Size: 5.8 MB (5827457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1a4e58da0c27bf60d3b78991b2ec913d0c54a2e5804ea75ad1571f1c5525c6`  
		Last Modified: Wed, 17 Jun 2020 02:25:57 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc42a572eade2899fa9e8e1875c86e7c65a71935ce9fb1988dbd8b11ec8e18b`  
		Last Modified: Wed, 17 Jun 2020 02:27:00 GMT  
		Size: 317.0 MB (316991090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7c1dc192444963c02d4254fe3b5e5e5fb189c5e38b9847ef5782df918b38e8`  
		Last Modified: Wed, 17 Jun 2020 02:25:57 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc87fed05e6b7d73b4ac3984cce0dc04fd50ff74ef7eef8298db2bc3f6e701`  
		Last Modified: Wed, 17 Jun 2020 02:25:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10bb3cafd77bd2eb46f27113cf0eaa20e3f758c1220317527d0b59d1f5921c4`  
		Last Modified: Wed, 17 Jun 2020 02:25:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b41861c2497c8c14b44641671437945892d00e00a0fd7eba11873313cddbbb5`  
		Last Modified: Wed, 17 Jun 2020 02:25:56 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0815ad15f90ba15f61ab0fa959ca93f73c97911bc5a4e65178b253a0c6afb3`  
		Last Modified: Wed, 17 Jun 2020 02:25:56 GMT  
		Size: 118.1 KB (118069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a81c24d9da6a6194df81eb31600554dbe5bc63fe6cf1b962f304ed348f2e1f5`  
		Last Modified: Wed, 17 Jun 2020 02:25:56 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
