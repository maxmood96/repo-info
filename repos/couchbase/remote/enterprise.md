## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:00512a2c71734c56e9d030d4f597c6492c23dce53a67af9e0b7fedf6a62124c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:a46ea3d6665ebd05bb0e69d573cccf15ea8f9dae61d5b09432b8138c5023d3c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515338711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8558296d6ab2cd70f82d248d092cfd414508bc35ac6957f370e2b30af1a8542`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:05:29 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Tue, 07 Jul 2020 00:05:48 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jul 2020 00:05:48 GMT
ARG CB_VERSION=6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66
# Tue, 07 Jul 2020 00:05:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Jul 2020 00:05:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jul 2020 00:06:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Tue, 07 Jul 2020 00:06:44 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 07 Jul 2020 00:06:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chown -R couchbase:couchbase /etc/service
# Tue, 07 Jul 2020 00:06:45 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:06:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jul 2020 00:06:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 07 Jul 2020 00:06:46 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 07 Jul 2020 00:06:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jul 2020 00:06:47 GMT
CMD ["couchbase-server"]
# Tue, 07 Jul 2020 00:06:47 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jul 2020 00:06:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebedec0f7e959d19fb95ec05e13ccabd602c2e061c9aa8f416ccdacf87cb13e`  
		Last Modified: Tue, 07 Jul 2020 00:09:19 GMT  
		Size: 5.8 MB (5827589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ea011ae57cb06279eae6675423177a2de8d465637ef6509d65650ea69c5c8c`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2674567f79a2dd39fe8337f2828752cbf1b1877f3f9a359d0def3efe07a3ba80`  
		Last Modified: Tue, 07 Jul 2020 00:10:13 GMT  
		Size: 465.0 MB (465013145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b8605d612679f4e85e472820876451131383ae9b3db814068b2c5b26fe622f`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb8ebc86176e4d41a3dc0b70e4d8a46d2cebe65b686aa25b86e8b1b64b3aa5a`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33546706af73de9efb3cd7944da396e6caf2145aab8950980d8cacdef14dd525`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e850ef94972bc259aef0c336964ec90cb3827c50aff2ead3a0d4bca430a545fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff30952419971219f8991def47d455efbe53e64a56a261d485290a23c8f1e3fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 118.1 KB (118068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042d7117c7d6000c005d2cb0d0748a4d7397e42d52de8aa974accf0e139a9e0`  
		Last Modified: Tue, 07 Jul 2020 00:09:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
