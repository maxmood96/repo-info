## `couchbase:enterprise-7.0.0-beta`

```console
$ docker pull couchbase@sha256:67d94ef8715cad17529acf07c7c20fe49c536486dadec58ca26e38b6e7f5402b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:fb7b1e1ac088ffea201a07d4e864f92da1022825d357f0da39ba9351643eea92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616178271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0f9a8bda529d3f71fdb63969aebce497f7a45903153e1f88c860a604d678bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:26 GMT
ADD file:4f15c4475fbafb3fe335e415e3ea1ac416c34af911fcdfe273c5759438aa8eb4 in / 
# Wed, 25 Nov 2020 22:25:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 22:42:43 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Wed, 25 Nov 2020 22:43:07 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 25 Nov 2020 22:43:09 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 25 Nov 2020 22:43:09 GMT
ARG CB_VERSION=7.0.0-beta
# Wed, 25 Nov 2020 22:43:09 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Wed, 25 Nov 2020 22:43:09 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb
# Wed, 25 Nov 2020 22:43:09 GMT
ARG CB_SHA256=b345bb3f81332fe93e87966426f3b53205486fbe4902991a57566381a7ad217b
# Wed, 25 Nov 2020 22:43:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 25 Nov 2020 22:43:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=b345bb3f81332fe93e87966426f3b53205486fbe4902991a57566381a7ad217b CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 25 Nov 2020 22:44:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=b345bb3f81332fe93e87966426f3b53205486fbe4902991a57566381a7ad217b CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Wed, 25 Nov 2020 22:44:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=b345bb3f81332fe93e87966426f3b53205486fbe4902991a57566381a7ad217b CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 25 Nov 2020 22:44:18 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 25 Nov 2020 22:44:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=b345bb3f81332fe93e87966426f3b53205486fbe4902991a57566381a7ad217b CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Wed, 25 Nov 2020 22:44:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 25 Nov 2020 22:44:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=b345bb3f81332fe93e87966426f3b53205486fbe4902991a57566381a7ad217b CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 25 Nov 2020 22:44:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=b345bb3f81332fe93e87966426f3b53205486fbe4902991a57566381a7ad217b CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 25 Nov 2020 22:44:21 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 25 Nov 2020 22:44:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Nov 2020 22:44:25 GMT
CMD ["couchbase-server"]
# Wed, 25 Nov 2020 22:44:27 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 25 Nov 2020 22:44:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:da7391352a9bb76b292a568c066aa4c3cbae8d494e6a3c68e3c596d34f7c75f8`  
		Last Modified: Fri, 06 Nov 2020 15:20:07 GMT  
		Size: 28.6 MB (28563271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14428a6d4bcdba49a64127900a0691fb00a3f329aced25eb77e3b65646638f8d`  
		Last Modified: Wed, 25 Nov 2020 22:26:39 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d948710f21ad82dce71743b1654b45acb5c059cf5c19da491582cef6f2601`  
		Last Modified: Wed, 25 Nov 2020 22:26:40 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36518e5bf0b3ea7259ad8552c0ab71f6fec5f5958ca4a37b08c294935011bf81`  
		Last Modified: Wed, 25 Nov 2020 22:48:32 GMT  
		Size: 6.3 MB (6277930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a43d9de12c32eb33b0357fb6a7f09a56472a028a53fc2757f933aee6dcf301a`  
		Last Modified: Wed, 25 Nov 2020 22:48:28 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c00c723483048bb743dfdb2b9d5a5f65d3f50ce29dfa6d5614f1e8b0ddeea0`  
		Last Modified: Wed, 25 Nov 2020 22:48:28 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fe59b99b103f498c937a6bba03bd3898b550b3aad70bb5a6b45700a8f532ec`  
		Last Modified: Wed, 25 Nov 2020 22:49:43 GMT  
		Size: 581.2 MB (581205963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11877b53f57000ae1b7b80a927d684e27e14df19b3e221ced6d29e92c7c85bef`  
		Last Modified: Wed, 25 Nov 2020 22:48:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fcbdca0f02a035ef7d99bf1d40b622ec822010601402343b7c20acc441446e`  
		Last Modified: Wed, 25 Nov 2020 22:48:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25be7735ff122ab48e409fde8d615c81e30659026bc8c891934ddbc5be2dba3c`  
		Last Modified: Wed, 25 Nov 2020 22:48:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71defbaf072a4d45c1f8363b1ba767bc112af513220b1d375e11f00f844788be`  
		Last Modified: Wed, 25 Nov 2020 22:48:26 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ee26262d7def9b589207865fbb5ab091f7f528c9f69ebeaeba43aa06041d3`  
		Last Modified: Wed, 25 Nov 2020 22:48:27 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0705dba5b3104277760901a5d8a1832cbef9bff8d060f9ad5e67368eb4d269`  
		Last Modified: Wed, 25 Nov 2020 22:48:26 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b1f8438095de7a920363803f85ae452fe281fd6b0a3650bc1b70292ada7e83`  
		Last Modified: Wed, 25 Nov 2020 22:48:26 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
