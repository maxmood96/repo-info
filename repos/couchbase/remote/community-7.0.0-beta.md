## `couchbase:community-7.0.0-beta`

```console
$ docker pull couchbase@sha256:9fc483c0e7ab4d1cd8f3c7e2de9593ea4bd3241b4e5fd75daea89b25644f9cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:e7599ad435031793e4bc9ab10e3d40ce36156163e7dfbfaacc33c0aca8c06605
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427396782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a13a210580aac6951aba2c6fbdcc43f0568ac7647ab8cd8258b5a0e5e9964b1`
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
# Wed, 25 Nov 2020 22:44:44 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb
# Wed, 25 Nov 2020 22:44:45 GMT
ARG CB_SHA256=7b2c5ec52ee2dd3d9e3af6943324cc0dfede0455bbc4e9c3839f4f76786ab900
# Wed, 25 Nov 2020 22:44:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 25 Nov 2020 22:44:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=7b2c5ec52ee2dd3d9e3af6943324cc0dfede0455bbc4e9c3839f4f76786ab900 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 25 Nov 2020 22:45:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=7b2c5ec52ee2dd3d9e3af6943324cc0dfede0455bbc4e9c3839f4f76786ab900 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Wed, 25 Nov 2020 22:45:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=7b2c5ec52ee2dd3d9e3af6943324cc0dfede0455bbc4e9c3839f4f76786ab900 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 25 Nov 2020 22:45:30 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 25 Nov 2020 22:45:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=7b2c5ec52ee2dd3d9e3af6943324cc0dfede0455bbc4e9c3839f4f76786ab900 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Wed, 25 Nov 2020 22:45:32 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 25 Nov 2020 22:45:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=7b2c5ec52ee2dd3d9e3af6943324cc0dfede0455bbc4e9c3839f4f76786ab900 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 25 Nov 2020 22:45:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=7b2c5ec52ee2dd3d9e3af6943324cc0dfede0455bbc4e9c3839f4f76786ab900 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 25 Nov 2020 22:45:34 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 25 Nov 2020 22:45:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 25 Nov 2020 22:45:34 GMT
CMD ["couchbase-server"]
# Wed, 25 Nov 2020 22:45:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 25 Nov 2020 22:45:35 GMT
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
	-	`sha256:9b4c284dd72e07b46432e395333a1036066331df4e46a3cbfe398f089f85392d`  
		Last Modified: Wed, 25 Nov 2020 22:49:58 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94efa96c53855dd8c49bfd3e2382c0a75166334a0e2006ab467fae454e3ce1c5`  
		Last Modified: Wed, 25 Nov 2020 22:50:50 GMT  
		Size: 392.4 MB (392424463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d36fc3a3d00a0de3c99550787a29419ae43620bf754b6c1b5494712499a549`  
		Last Modified: Wed, 25 Nov 2020 22:49:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798b56cbee895477a9f445a14a051da9966da846e0018c272537ceddcea3eca3`  
		Last Modified: Wed, 25 Nov 2020 22:49:58 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10af39b459dfde310226660dc1eaa69cbcec8016a8d450eeda701b5c5ccae0d3`  
		Last Modified: Wed, 25 Nov 2020 22:49:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cde8ffff11e80f8e80827ca78046bf463adac734a67fe4f210da4c80526460`  
		Last Modified: Wed, 25 Nov 2020 22:49:57 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a990acb6d5532f7928d5a1f93ca84629d236c60a646f5bd2eb03e476d704cc`  
		Last Modified: Wed, 25 Nov 2020 22:49:57 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5e522290fcb2ba5fd0cb55d5793bbc5acb1ff9963262b9b88fe3996a4e9f4e`  
		Last Modified: Wed, 25 Nov 2020 22:49:57 GMT  
		Size: 125.9 KB (125894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2f2c8191e773202faf64e06dfe99aefac4b06a1ecef8c241b80a82f03da63`  
		Last Modified: Wed, 25 Nov 2020 22:49:56 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
