## `couchbase:enterprise-6.5.0`

```console
$ docker pull couchbase@sha256:7ec8dfc1b4e31f8420e0e4d9e386063d2119ecaec17df72b8ad11cfd88e135d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.5.0` - linux; amd64

```console
$ docker pull couchbase@sha256:82893649987b6ca270470b6e6e93975088c04be49a8d806d05c9b16edfd2be66
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.1 MB (556078055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c58bd9b3016abedb90c416a40cdd6fdcb693dfbf5aa19d57a3a866247c478a1`
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
# Wed, 17 Jun 2020 02:19:53 GMT
ARG CB_VERSION=6.5.0
# Wed, 17 Jun 2020 02:19:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0
# Wed, 17 Jun 2020 02:19:54 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb
# Wed, 17 Jun 2020 02:19:54 GMT
ARG CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b
# Wed, 17 Jun 2020 02:19:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 17 Jun 2020 02:19:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 17 Jun 2020 02:21:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Wed, 17 Jun 2020 02:21:13 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 17 Jun 2020 02:21:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN chown -R couchbase:couchbase /etc/service
# Wed, 17 Jun 2020 02:21:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 17 Jun 2020 02:21:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 17 Jun 2020 02:21:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 17 Jun 2020 02:21:16 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 17 Jun 2020 02:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jun 2020 02:21:17 GMT
CMD ["couchbase-server"]
# Wed, 17 Jun 2020 02:21:17 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 17 Jun 2020 02:21:17 GMT
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
	-	`sha256:c554cdc581011b4f1aa3b8673f4949232b85aa5466103902daa8c295804079bf`  
		Last Modified: Wed, 17 Jun 2020 02:24:30 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc4de48c3386d62ced42476feb3062b3b82cf1e1711a2c9cf4a817997005c24`  
		Last Modified: Wed, 17 Jun 2020 02:25:33 GMT  
		Size: 505.8 MB (505806491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed3738fb661cd195ef92f404113e05067ef1775482a0fb65545f64aeb9e6230`  
		Last Modified: Wed, 17 Jun 2020 02:24:30 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193c20cec420881f398653ec7978c9aaebbf4d82bcf56b127767fab5290f8610`  
		Last Modified: Wed, 17 Jun 2020 02:24:29 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd636397aaf3ae2f4b2ebd7fd3cb61964d3a5e3a364700f0e4baaa88f2cef1fe`  
		Last Modified: Wed, 17 Jun 2020 02:24:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efb1973ad3d08d588be77bab003c8e949785c49d224feafec124c1aa292ef5e`  
		Last Modified: Wed, 17 Jun 2020 02:24:29 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a990564c4435516e433082b8abda6b8685bcb2a57db74b221468fb3de23b5539`  
		Last Modified: Wed, 17 Jun 2020 02:24:29 GMT  
		Size: 118.1 KB (118069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6d1e4321ae99b748b0007554b6c2269a4cafde2f45d8159c768174d47e4870`  
		Last Modified: Wed, 17 Jun 2020 02:24:29 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
