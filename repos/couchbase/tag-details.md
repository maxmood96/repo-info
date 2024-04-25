<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:7.0.5`](#couchbase705)
-	[`couchbase:7.1.6`](#couchbase716)
-	[`couchbase:7.2.5`](#couchbase725)
-	[`couchbase:7.6.1`](#couchbase761)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-7.0.2`](#couchbasecommunity-702)
-	[`couchbase:community-7.1.1`](#couchbasecommunity-711)
-	[`couchbase:community-7.2.4`](#couchbasecommunity-724)
-	[`couchbase:community-7.6.1`](#couchbasecommunity-761)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-7.0.5`](#couchbaseenterprise-705)
-	[`couchbase:enterprise-7.1.6`](#couchbaseenterprise-716)
-	[`couchbase:enterprise-7.2.5`](#couchbaseenterprise-725)
-	[`couchbase:enterprise-7.6.1`](#couchbaseenterprise-761)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:7.0.5`

```console
$ docker pull couchbase@sha256:3485bb06b22d42803de0eb56fd35fcdf6772acab9bcf66d7f838f2fa28bf10d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:7.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:efab41d8b70dbf1ab0bdac3146be29230f8b2c31ac22fd04f2e805bfbaf53572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.7 MB (616705467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c797f8b300d809376605d3cb1533cdc39d55a83ab55a9e86a7d228532d2362f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:48:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5
# Tue, 16 Apr 2024 04:48:49 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb
# Tue, 16 Apr 2024 04:48:49 GMT
ARG CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea
# Tue, 16 Apr 2024 04:48:49 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:48:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:48:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:50:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:50:04 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 04:50:05 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:50:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:50:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:50:06 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 04:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:50:06 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:50:06 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:50:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2539cc6714d28ae08856da9a1375e679890fea343b120abb8b5ad0d44be436`  
		Last Modified: Tue, 16 Apr 2024 04:53:50 GMT  
		Size: 6.3 MB (6286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e300a40474735d3e4dd215ab1ffb4572611a70ccce1c7de29378314c1b012c1`  
		Last Modified: Tue, 16 Apr 2024 04:57:35 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362e4873e4ff14a6376c605480886544f83a01c71937fb043773e03650e4c7a`  
		Last Modified: Tue, 16 Apr 2024 04:58:30 GMT  
		Size: 581.8 MB (581829953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8783efece9f0eb8f96f4044b8eb986edf115576dd5b7df6ca2ac12e7cef982b3`  
		Last Modified: Tue, 16 Apr 2024 04:57:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987e434c35466f3273009f91523ce1ceaa74f9664b89df12855a01a5860c3d9`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8b054ba3c1870f58ab5c76e33d67d61fcbe4abc1687bc842c83ce23db06513`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39352bcf77d263ce4d593200e68ddf97e19c1caa90c5fc76680803867e3b2105`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501e3a27ebeb4a76bf012503d912b1c897fe2c6ccc893dd328d603fd5201812`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48f36e7ba5b483a531df7a7f3a32f81cafe359789eaca45d75c74530843f4ff`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.1.6`

```console
$ docker pull couchbase@sha256:6b057fd6e5b3328736eb66f04ca9a00aa429a9f1e54badb81897f2700288a031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.1.6` - linux; amd64

```console
$ docker pull couchbase@sha256:4c812ed1e60d9f424e2dc394e0e69f10aee6bb2fd753caf918d8353d71b64e1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.0 MB (652023382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f40536f2fc61bfd047326255ccee239ecd869e808eb8c592b4560ec219b54e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:46:11 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Tue, 16 Apr 2024 04:46:11 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:46:11 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:46:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:46:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:47:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:47:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:47:31 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:47:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 04:47:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:47:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:47:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:47:32 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 04:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:47:33 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:47:33 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:47:33 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2539cc6714d28ae08856da9a1375e679890fea343b120abb8b5ad0d44be436`  
		Last Modified: Tue, 16 Apr 2024 04:53:50 GMT  
		Size: 6.3 MB (6286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de27bf474791f4838b95d1e9df0760e45d664cea6d0be50adc3c6bcdb88fa09d`  
		Last Modified: Tue, 16 Apr 2024 04:55:44 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c09bc767d9349d7a4821734cd0f3f541f23ec07d5dd90de2a1628432553f19`  
		Last Modified: Tue, 16 Apr 2024 04:56:40 GMT  
		Size: 617.1 MB (617147861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2bc163d643487b1c65e838c43871f921b9a753852177ba6cfb162b36cb036e`  
		Last Modified: Tue, 16 Apr 2024 04:55:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0e508e0fe5d9ee3ac6edd740938681a9e3477e0167ac7e8a87e56a33f6e66e`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 745.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d522f04a9aa527c28206d72467435dc4189be9a1fbc7e8d7537ab9bf41ac40f3`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be49c3886edf3eb54f8d9adb99d8b9461d9c1815cb4540efa014d873abbc18`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1378631c28c11ec2326222524fd695b4ddf5d0feb9cca410b70ce90710dba981`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2cc64b78533624d9c689059875cf98a05208e11a1bbcf73fc9b9820ed66ecd`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.1.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:b5918273452f7476d9126b64a01e59f10c78e11629e22df48a13efdf05715317
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.6 MB (622645424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c08463535e86a72ec75873b003194db8f48e879296911f9af0d6944b6e8da8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:22:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:24:26 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Tue, 16 Apr 2024 03:24:26 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:24:26 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:24:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:24:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:25:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:25:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:25:36 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:25:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 03:25:36 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:25:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:25:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:25:37 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 03:25:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:25:38 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:25:38 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:25:38 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc63a620f1ecf9579c760cf290f09f23af0305d47d3bb6f3cbcaf31145979bb8`  
		Last Modified: Tue, 16 Apr 2024 03:28:32 GMT  
		Size: 6.1 MB (6110804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb6a2b048134d934f7ae7455f485d0618e4d741599cc5da7dc720fa7d4fa7ea`  
		Last Modified: Tue, 16 Apr 2024 03:29:57 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0475936cd5e1a71d183cd309be55db1438ec9732a6dc922b696f7d45506b809c`  
		Last Modified: Tue, 16 Apr 2024 03:30:37 GMT  
		Size: 589.3 MB (589325278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a22915dc26ebcad4be666d4a3225dd4a1f111157da68655bbbc1c794c3547cb`  
		Last Modified: Tue, 16 Apr 2024 03:29:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10e79084f8cb9f37683e84b1a572bfb2e47affb34a1ef05a4a6bc069c80468a`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b05f1a4aa3a47b1668369d48fcd4c65aa2ce076b2344d7a9432a4964a098f5`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9f7052f4d09ccc89fa9a86586da4ffe99cbdfb022b615f2fd439910f910529`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d18565aa5295992120b18436727334a97b352ff6fa4c50c04074589a04931d`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5804046ac2041bc67551e84ab308a8559056f1b25faccf288598475d157b207`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.2.5`

```console
$ docker pull couchbase@sha256:c2440765beab91a46ea9d944d0d02f789b11b8c756fbc5feae4a036e9c9dc970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.2.5` - linux; amd64

```console
$ docker pull couchbase@sha256:9d5f00a9ec6436c107bedfd30b7c80e9ffa88dd320f7598423b0324fc37f1816
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.2 MB (644222759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0949150a2eb0a12d7366e0ce528fb870db3721f917d524d825e887eeefd36710`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:40:16 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:40:58 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 25 Apr 2024 01:28:12 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 25 Apr 2024 01:28:13 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 01:28:13 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 01:28:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 01:28:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 01:29:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 01:29:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 01:29:38 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 01:29:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 25 Apr 2024 01:29:39 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 01:29:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 01:29:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 01:29:40 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 25 Apr 2024 01:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 01:29:40 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 01:29:40 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 01:29:40 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd3db21ebd06129580fcbeb1a7c1a8b4de2a102d38a2618a00a8037f4b97498`  
		Last Modified: Tue, 16 Apr 2024 04:51:38 GMT  
		Size: 6.2 MB (6186299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e98997fd1c5843cfd8861998c579c903a1f6dcc4d008cc6304bbcd2a9c1430c`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.1 MB (1092150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cfe8d94f41ddf50bcf1ba26515674210275309cddc7342102b9ad53071d72b`  
		Last Modified: Thu, 25 Apr 2024 01:30:21 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9b7c93f1b2cf1ae39cbccc83d4d05ffbc848d21f5bf7d1c942896abee92494`  
		Last Modified: Thu, 25 Apr 2024 01:31:15 GMT  
		Size: 608.4 MB (608354724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f04f1439e8af39c0a98eb1196dabf13edb394d68053c054c34f06667ebd9226`  
		Last Modified: Thu, 25 Apr 2024 01:30:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd7bffa7f738d29066267e490c1e2c0f7b3e49de9c776b49d09d055fc5c2f52`  
		Last Modified: Thu, 25 Apr 2024 01:30:19 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cae686a9e723a12c5059cb41c8ef28c8ca57f0369b5c47f8d85fd94d6036384`  
		Last Modified: Thu, 25 Apr 2024 01:30:18 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e41c37d8300df4ee7545cfde8299af6b2201b273dec302a27abc8d39ff9e536`  
		Last Modified: Thu, 25 Apr 2024 01:30:18 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627b303f7b18d93ba32f9c1ea717ae0b87498b11061ba1ce483d75ffce63c321`  
		Last Modified: Thu, 25 Apr 2024 01:30:18 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090eaa4a461fbfa3fa271ba91e4b41a704ee4cc80b11b3a78e1e6acb009d8288`  
		Last Modified: Thu, 25 Apr 2024 01:30:18 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.2.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:bee99da783dfe814f89be86857c3b426b017c7fa7b753b05045a3206ba3dd04b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.8 MB (619808577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c4570529f604e0c09f02661e574667c675237dfd7a307f87d463b0d2a9fcad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:19:13 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:19:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 25 Apr 2024 00:09:41 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 25 Apr 2024 00:09:41 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 00:09:41 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 00:09:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 00:09:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 00:10:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 00:10:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 00:10:55 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 00:10:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 25 Apr 2024 00:10:55 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 00:10:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 00:10:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 00:10:56 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 25 Apr 2024 00:10:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 00:10:56 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 00:10:56 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 00:10:56 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11863ef3e894dd6ffa24e5592f86fc52b51e62391229ae4e356dbf4f9f565c4f`  
		Last Modified: Tue, 16 Apr 2024 03:26:52 GMT  
		Size: 6.0 MB (6027895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050cd1760032ad0930988694136c07112902c2fa6d05b175000bfe7fe7e8ae41`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 938.2 KB (938223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83063714dbddc5fbf5d803d8c5336eff69daad667202bda8bef0dc079eb2edf`  
		Last Modified: Thu, 25 Apr 2024 00:11:23 GMT  
		Size: 1.8 KB (1846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9a43b70b2a5720a58763f565ff4288632ad82e4cba8901ad58aaebc489846b`  
		Last Modified: Thu, 25 Apr 2024 00:12:05 GMT  
		Size: 585.6 MB (585632400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367f6e0682b19cb1c81dc0dc3b9312c09e8a6b7056dd73a9b598447ce1d930b8`  
		Last Modified: Thu, 25 Apr 2024 00:11:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51dda503d78d35504aabffe05c0a377d863a95ecc822ce73c8282cd13124acc`  
		Last Modified: Thu, 25 Apr 2024 00:11:22 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573deaea6e0d377f7c2f4a9830daf4f43f629474b042950057de1893ef438b14`  
		Last Modified: Thu, 25 Apr 2024 00:11:21 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ec76e00a535f6cbecae38ea732fef92fc378f70b158004f8cef16a16004a9`  
		Last Modified: Thu, 25 Apr 2024 00:11:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4494f8f6b9f3977c653eacf0bf303d2b8449983868cd7203bb0d2296e6095900`  
		Last Modified: Thu, 25 Apr 2024 00:11:21 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf767162aa984b035c4fd22f1ad3c52bfa38fa51b4f6111c709647bb89b2`  
		Last Modified: Thu, 25 Apr 2024 00:11:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.6.1`

```console
$ docker pull couchbase@sha256:cb5770e190f393c923386dca3c71e29a9e27844298cef14f206333dc03637eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:100cae80fc70fec6482e12b47cf24ca5a9b47e99eefd8f676caaf67e086f0d4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726130679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1256799c47bc88935fc7deac454d87f0d0a01794a09fc37fb2cfbafb33d70016`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:40:16 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:40:58 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:40:59 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:40:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:40:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:42:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:42:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:42:26 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:42:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 04:42:27 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:42:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:42:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:42:28 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 04:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:42:28 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:42:28 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:42:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd3db21ebd06129580fcbeb1a7c1a8b4de2a102d38a2618a00a8037f4b97498`  
		Last Modified: Tue, 16 Apr 2024 04:51:38 GMT  
		Size: 6.2 MB (6186299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e98997fd1c5843cfd8861998c579c903a1f6dcc4d008cc6304bbcd2a9c1430c`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.1 MB (1092150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c039cbe5cfe3b3e44672e2a2d6cab1cad823f888882173f1068d3758dcd757`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56b935084669bdfd3b872fd758b7bbac7a1a6b4866303f939c299596faa9bd2`  
		Last Modified: Tue, 16 Apr 2024 04:52:41 GMT  
		Size: 690.3 MB (690262973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16520dcd69488d59ca335969dadbd0cdc0625c3cee5cf500d5a38a57e9595417`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786fb049c9b0a1768dcf30589d061963fad22c4b0628e6af4fe56a74c757de19`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcb79a54d543e85f23b529085481a77fac30a3b9b58b67f0052fd3816ee81dc`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 729.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b850079650e2bb938b75bf7ac16a360b496f0886fe9293a3d6bf9993968783be`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfafd2f90526ea6f2d0f367585ba614b723a87757c209f0583dd421f92b4e17e`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280c967059329600f12508b225f7319859b0246bac84956afdb45bfd37817c19`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:3c7c6163dec118093b3c1d173b47ae299010c11fba531db05589d8b0c68a7c9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9628cf02ec68b07c5a1e590139f11b9b07910c3bac3aa4f764a9cb1cc582282b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:19:13 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:19:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:19:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:19:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:20:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:21:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:21:01 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:21:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 03:21:02 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:21:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:21:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:21:03 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 03:21:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:21:03 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:21:03 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:21:03 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11863ef3e894dd6ffa24e5592f86fc52b51e62391229ae4e356dbf4f9f565c4f`  
		Last Modified: Tue, 16 Apr 2024 03:26:52 GMT  
		Size: 6.0 MB (6027895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050cd1760032ad0930988694136c07112902c2fa6d05b175000bfe7fe7e8ae41`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 938.2 KB (938223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aacb5568ffaa5e455a84e0a4e3e26c50680d093bf23e5347351233691c5ae17`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811495152e6c0b20a24472561240fa58446e1a4b800378830ffd871e8fe9ea1a`  
		Last Modified: Tue, 16 Apr 2024 03:27:37 GMT  
		Size: 665.1 MB (665134412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00635e297efd98909d1f1e76d4fcba4ae15072c025032ab4bf34918aca6482`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a27cb8eaa05c9a2ac24d5f60222785903edaaef8b2aac75c23c9da896f069`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4151ecc05ff245c9960139bc679a16d43f39a95f6357a5dbd83ad1612054879d`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 727.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e259246b1be5ddfb73a64b064b5fa48332422b4eba041891f764cc5b9b22e`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ef10a6faeba6a8342963d0edfdc92bc2d63b7e9628b641e07d0319098084f0`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabab6402e5358b1050646bd4d720f60a9fe2aabb528ee30ca91ec295af515a6`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:44b8ce2bcfb80563f2a142099c882a9f3f0516bdfabb670fa0ca5f0ed474ac83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:d81336e2380e0e6a4754d7f1dadd176f539daeb245703a64518af7809d976620
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385922952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece6f2a68274488b90310d998cb6992604064099b7eff1c194199295b139de91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:40:16 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:40:58 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 04:42:35 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:42:35 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:42:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:42:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:43:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:43:25 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:43:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 04:43:26 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:43:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:43:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:43:27 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 04:43:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:43:27 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:43:27 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:43:27 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd3db21ebd06129580fcbeb1a7c1a8b4de2a102d38a2618a00a8037f4b97498`  
		Last Modified: Tue, 16 Apr 2024 04:51:38 GMT  
		Size: 6.2 MB (6186299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e98997fd1c5843cfd8861998c579c903a1f6dcc4d008cc6304bbcd2a9c1430c`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.1 MB (1092150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8166fc3537fa4d881fbc6d4c1ea56bb291e0b641f2c4e2d3041e73c6ce2dcc`  
		Last Modified: Tue, 16 Apr 2024 04:52:56 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a87d4f249795d52cbfc7096ff6c0271132cb6dd77409de195e07ce0292d97e1`  
		Last Modified: Tue, 16 Apr 2024 04:53:38 GMT  
		Size: 350.1 MB (350055249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57caa49d110e6b928dd721367ccb5994179cdd33d372cf09d1af654dfd49497`  
		Last Modified: Tue, 16 Apr 2024 04:52:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736c6798182a660c26a4ca0d8b0916011f1eeb84a0da6ad1fbc755aed9c61734`  
		Last Modified: Tue, 16 Apr 2024 04:52:54 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8226c99d58bfe0912fd2ea6d06574e41a6d97731ad7e3974be2b2ec43bda3c7c`  
		Last Modified: Tue, 16 Apr 2024 04:52:55 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13eabeba1b2bf7f44ce384a746c99ab4861e83a9b3c0e6afaad652080f61b4de`  
		Last Modified: Tue, 16 Apr 2024 04:52:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37051295175f43e4822add9a41d8f64c9fb270d332916966aa7e04e0ddf0f1e1`  
		Last Modified: Tue, 16 Apr 2024 04:52:54 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6568c4c822d1f0a0ffb81cefb51b80be8188279e9a182f5cb2592820cfad7b52`  
		Last Modified: Tue, 16 Apr 2024 04:52:54 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:69549a2ec3de24455cac9a694ac6f9ff74d55f14785c4f88e8bf765881617aa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367767970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f48a8ecb40ac6e6afd4365d685b48f1c7a75f105a16c82b4212df095daffbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:19:13 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:19:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 03:21:17 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:21:17 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:21:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:21:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:21:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:22:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:22:02 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:22:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 03:22:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:22:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:22:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:22:04 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 03:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:22:04 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:22:04 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:22:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11863ef3e894dd6ffa24e5592f86fc52b51e62391229ae4e356dbf4f9f565c4f`  
		Last Modified: Tue, 16 Apr 2024 03:26:52 GMT  
		Size: 6.0 MB (6027895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050cd1760032ad0930988694136c07112902c2fa6d05b175000bfe7fe7e8ae41`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 938.2 KB (938223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1da51bcdc61f69943ae37b39dbe437c08b49cf442dc34e92b3fb51806066c2`  
		Last Modified: Tue, 16 Apr 2024 03:27:52 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f5953723e88dcc8bf7500f20bc2a69383045b80484d521120f2f240ba60939`  
		Last Modified: Tue, 16 Apr 2024 03:28:21 GMT  
		Size: 333.6 MB (333592108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c146994ee34ff0ce90827e0aa56b326e33443657578fd8dd028d7405d7c37b`  
		Last Modified: Tue, 16 Apr 2024 03:27:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0550e546386bf516846b61c3d53de8e3baf1d1f8ada0adc8917045610cb4869`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f1f70fa8ad847efc8befbd198421514d6dcd1046f321108963ee579fc93ed`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 728.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f7729fa51b580e193e72c17264ec0dffbf11cc79ffe3e78f154666962c5237`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1e37bdb95e4d75054d5ac94fd067f417b6b8a37a9ddbb7ef79ace81e1a44cb`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03590bd811827aa9264803266c094566248e3242e05c37eba419e763cc5a2c0`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:8d77253c89f6e2ed0df3c93c585acbac7d7c89c95341de35dab5cea904693f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:b201af6362d2df9085134253def2e64109a8737f08b6b6067315a7966c1ba98a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429074418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327fb37fa4c0465ded03013936c560c2405dba5d9db52ba941d0d475482a8b0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:50:23 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:50:24 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Tue, 16 Apr 2024 04:50:24 GMT
ARG CB_VERSION=7.0.2
# Tue, 16 Apr 2024 04:50:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Tue, 16 Apr 2024 04:50:24 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Tue, 16 Apr 2024 04:50:24 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Tue, 16 Apr 2024 04:50:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:50:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:51:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:51:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:51:11 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:51:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 04:51:12 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:51:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:51:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 16 Apr 2024 04:51:13 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 16 Apr 2024 04:51:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:51:13 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:51:13 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 16 Apr 2024 04:51:14 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a1cb988904c25647648362e6c8e68e69349f0f3edb39808ae9c64ccabc6a7b`  
		Last Modified: Tue, 16 Apr 2024 04:58:45 GMT  
		Size: 6.3 MB (6294045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a96e305e5833592be9f95ffeb993b2258cf28b68635431bc3153e77aa9f65bd`  
		Last Modified: Tue, 16 Apr 2024 04:58:42 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacf3a0b8b5fe5856789740fb7eca6c2f9f004403ee5b077d0b489eaf91a97ea`  
		Last Modified: Tue, 16 Apr 2024 04:58:42 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7841470a8d24f967fdb2d43b46a3e43bfa68b479706ed68648c4685622a4ae67`  
		Last Modified: Tue, 16 Apr 2024 04:59:26 GMT  
		Size: 394.1 MB (394061876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2819169d0e0c38db3d8bad9935410cf43c13e9c8fe65a590a4d267a11970d857`  
		Last Modified: Tue, 16 Apr 2024 04:58:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f654bcb637d40adab65e6e96aef422b75d33b92ea31e199385fe14200d755779`  
		Last Modified: Tue, 16 Apr 2024 04:58:42 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc88615f4cdd8fb981941eb1947d4e21647048644661c441f85518818fab256`  
		Last Modified: Tue, 16 Apr 2024 04:58:40 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4629fe8bd3289b655c3e4e2b99ee2b54462414aff5001cc4b3a4817cdac66b17`  
		Last Modified: Tue, 16 Apr 2024 04:58:40 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29806ddc6f565c5ec57fa00ce532dd1803a12878b3543bdbc845e8ad294322e1`  
		Last Modified: Tue, 16 Apr 2024 04:58:40 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c233b3ec01b08e8a8453721af6f451f5a5f7ea4b1a93df9a66fd4d8eeb1e59`  
		Last Modified: Tue, 16 Apr 2024 04:58:40 GMT  
		Size: 129.5 KB (129512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a8df134646b8c2e38c0a523244f3569f45455d89fb006213401f1f8509a80`  
		Last Modified: Tue, 16 Apr 2024 04:58:40 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.1.1`

```console
$ docker pull couchbase@sha256:4d896095ca414add09fdebd22ae4fef538c7bd586df0b08620524b8d7c392b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.1.1` - linux; amd64

```console
$ docker pull couchbase@sha256:164d01207333a8f6543d73ea05067ce1750ad0a287d708ab5fbca331f572d968
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.7 MB (346675310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7180ffa0d51b8e27624e6a2ee157995b2ead00455a362654e590ae84b24586`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:47:50 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Tue, 16 Apr 2024 04:47:50 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:47:50 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:47:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:47:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:48:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:48:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:48:35 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:48:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 04:48:36 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:48:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:48:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:48:37 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 04:48:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:48:37 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:48:37 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 16 Apr 2024 04:48:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2539cc6714d28ae08856da9a1375e679890fea343b120abb8b5ad0d44be436`  
		Last Modified: Tue, 16 Apr 2024 04:53:50 GMT  
		Size: 6.3 MB (6286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36b08374643315aa0da83c1666605e050572b8bd822d378c90fb1f063eeba0a`  
		Last Modified: Tue, 16 Apr 2024 04:56:51 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba969eeff9a854bb31343d622aa7cbdd14ac2763dc4820f7f50f7a568f6e99ee`  
		Last Modified: Tue, 16 Apr 2024 04:57:26 GMT  
		Size: 311.8 MB (311799791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051e0e87fe61728ac09e2011c5cbc49008d2f70f68567dba9fb02275e1c3346f`  
		Last Modified: Tue, 16 Apr 2024 04:56:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468e65d3abecab433212b90487f124a42aa830b136cec6beefb2ee8bf2d15603`  
		Last Modified: Tue, 16 Apr 2024 04:56:49 GMT  
		Size: 745.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697713f73bf3de208f5463d0b00842ad6cc5d950ad621692e2ba67c7f88b78c7`  
		Last Modified: Tue, 16 Apr 2024 04:56:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9625445bf00dff982bf5b5d18dd31aaf69cb8bc336217a77da15b35cf85fdffa`  
		Last Modified: Tue, 16 Apr 2024 04:56:49 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231b785394508c76faf977c1e1c2630da70b09aa2cd05b67bf2d279297c23c3f`  
		Last Modified: Tue, 16 Apr 2024 04:56:49 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee56b1b01f287234ec2f2d167cbe48a17d16db47214a96eb4c485a151405110`  
		Last Modified: Tue, 16 Apr 2024 04:56:49 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.1.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:5eb29ce36f244ef8de6f03448c8915fec6015183bb8aecf97a459d692527a733
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327346275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d8558f4d600f8a188818ecb40b9db545938cbb1011d453b88ad48167661de0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:22:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:25:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Tue, 16 Apr 2024 03:25:49 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:25:49 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:25:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:25:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:26:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:26:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:26:28 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:26:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 03:26:28 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:26:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:26:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:26:29 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 03:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:26:30 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:26:30 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 16 Apr 2024 03:26:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc63a620f1ecf9579c760cf290f09f23af0305d47d3bb6f3cbcaf31145979bb8`  
		Last Modified: Tue, 16 Apr 2024 03:28:32 GMT  
		Size: 6.1 MB (6110804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e084335ef92cc3af8c8f11ed74597a00149aee7f65e269dcbff2623e9571a8`  
		Last Modified: Tue, 16 Apr 2024 03:30:48 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d674c568e7d9fe13ba454ccbb9df0049e4705b72de627889225b79ce0c8d2460`  
		Last Modified: Tue, 16 Apr 2024 03:31:13 GMT  
		Size: 294.0 MB (294026127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f198ff666933f434adf2e1193bac45d9021dcea08138347a8ae0e9c2db47338`  
		Last Modified: Tue, 16 Apr 2024 03:30:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee32a3317832108cbf6b3662904124e1ff8699ffb6891e186d95702c7add2aa`  
		Last Modified: Tue, 16 Apr 2024 03:30:46 GMT  
		Size: 737.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790fdb70bcc168d9c4a264d712cbd700d2ffa4f9f1e196b71afeb619f54a6075`  
		Last Modified: Tue, 16 Apr 2024 03:30:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29f940101411071ff479ef3ccf5ec637f4b3ed3a0673ddfbb7b32aeb08d77ac`  
		Last Modified: Tue, 16 Apr 2024 03:30:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50485a744d4cf8e7b0e2ec59172b97f23ee9fa263ff945d67197f52d585d7805`  
		Last Modified: Tue, 16 Apr 2024 03:30:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db392f66718d461ca08874f7baab6f73b3944b750fa9793a3bc79a3dad82083`  
		Last Modified: Tue, 16 Apr 2024 03:30:46 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:39aeb1fc6682376b9f7e13d7a930da62d34b6d085ec00269be1578900c8e59fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:8b81c1de29e88ab7a892795bb0c0acf3d4dde47e57a950cfe65fe1ec8a576c69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366179068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d975012e4cd066b6877beb901560f81416e0823408aa8ec9042529cf2f2fecb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:43:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Tue, 16 Apr 2024 04:45:12 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:45:12 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:45:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:45:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:45:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:46:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:46:00 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:46:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 04:46:01 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:46:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:46:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:46:02 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 04:46:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:46:02 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:46:02 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:46:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2539cc6714d28ae08856da9a1375e679890fea343b120abb8b5ad0d44be436`  
		Last Modified: Tue, 16 Apr 2024 04:53:50 GMT  
		Size: 6.3 MB (6286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4e64d3ea9a80ae3df4b1b89f482245ee66fbdc6676cd34ad07b16fafd9c77a`  
		Last Modified: Tue, 16 Apr 2024 04:54:57 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee721e9b8b904e3a5770d5ba6a28c77677cc411e7d7547d4b2f3125f116852e`  
		Last Modified: Tue, 16 Apr 2024 04:55:35 GMT  
		Size: 331.3 MB (331303556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89869ac2f527e1b77a0b2b4c23c509503ab59a7e1daf2799754efda6e004315c`  
		Last Modified: Tue, 16 Apr 2024 04:54:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacb3b66dce06d60aa94f29601495366cdf3ef06e464d13d81b2879a88a9015`  
		Last Modified: Tue, 16 Apr 2024 04:54:56 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921e3eef11e8d4e7c5a271a2015b460e5c9a2eb568eab05056ddc180e6e1e72`  
		Last Modified: Tue, 16 Apr 2024 04:54:56 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c5898c69a407a45c0bbf5feb22ce4301858998e28683ec17065f33dce90517`  
		Last Modified: Tue, 16 Apr 2024 04:54:56 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a0dfa4df2b71627cf8883a507e2ace0fd705c44d1e0fa0acb8f9eb7997c06a`  
		Last Modified: Tue, 16 Apr 2024 04:54:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846ba9d073ffeca17d7d66ece1ff5a9e81397a4fd604f495f093cb05f4be4402`  
		Last Modified: Tue, 16 Apr 2024 04:54:56 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:e4243a10162c315666543630a57bfa4ae217d114e196cefa9a5aec479c513a03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346401233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d68ab1d27bc7f520ee5ff9f85ac43d200e681f3d0e7bdda9fc80528f29d559`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:22:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:22:22 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Tue, 16 Apr 2024 03:23:37 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:23:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:23:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:23:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:24:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:24:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:24:20 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:24:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 03:24:20 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:24:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:24:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:24:21 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 03:24:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:24:21 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:24:21 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:24:21 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc63a620f1ecf9579c760cf290f09f23af0305d47d3bb6f3cbcaf31145979bb8`  
		Last Modified: Tue, 16 Apr 2024 03:28:32 GMT  
		Size: 6.1 MB (6110804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef40843589dbf6293a0d24ed4b5d1e06c9d2cddc8eb834dc90a6cfdf344313`  
		Last Modified: Tue, 16 Apr 2024 03:29:22 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0dde2a05d4fe5b7dc13e7e4d55154255600cb11bd94e9e4e959c7f0ce54917`  
		Last Modified: Tue, 16 Apr 2024 03:29:49 GMT  
		Size: 313.1 MB (313081085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc6a8adec27ae9228d6374faf8e222a36d3d94346d41a228f0c2204d6986268`  
		Last Modified: Tue, 16 Apr 2024 03:29:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6a3c1a2cdbdb50baf979262dd705efafc50347431ace3c36f51ffea217a32`  
		Last Modified: Tue, 16 Apr 2024 03:29:20 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb32e280daba7b3df0d7bcc4343c3a6cc31bb3bdd6654699dac2d6030702870`  
		Last Modified: Tue, 16 Apr 2024 03:29:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d0924a656ddce523f2f819d4adad074a1451e257faf4c7ae5bfa857de490b3`  
		Last Modified: Tue, 16 Apr 2024 03:29:20 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca0e54a39c0eee1fb5d1062fb6dd1059c52f683cda59a32c9d9e34debfa0396`  
		Last Modified: Tue, 16 Apr 2024 03:29:20 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e871b2b9e3c4b6b26d9d1e1e61cb77c4c0e74bcb6dd4b7ac5b9a4db0a971f0d8`  
		Last Modified: Tue, 16 Apr 2024 03:29:20 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.6.1`

```console
$ docker pull couchbase@sha256:44b8ce2bcfb80563f2a142099c882a9f3f0516bdfabb670fa0ca5f0ed474ac83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:d81336e2380e0e6a4754d7f1dadd176f539daeb245703a64518af7809d976620
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385922952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece6f2a68274488b90310d998cb6992604064099b7eff1c194199295b139de91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:40:16 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:40:58 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 04:42:35 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:42:35 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:42:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:42:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:43:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:43:25 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:43:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 04:43:26 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:43:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:43:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:43:27 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 04:43:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:43:27 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:43:27 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:43:27 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd3db21ebd06129580fcbeb1a7c1a8b4de2a102d38a2618a00a8037f4b97498`  
		Last Modified: Tue, 16 Apr 2024 04:51:38 GMT  
		Size: 6.2 MB (6186299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e98997fd1c5843cfd8861998c579c903a1f6dcc4d008cc6304bbcd2a9c1430c`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.1 MB (1092150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8166fc3537fa4d881fbc6d4c1ea56bb291e0b641f2c4e2d3041e73c6ce2dcc`  
		Last Modified: Tue, 16 Apr 2024 04:52:56 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a87d4f249795d52cbfc7096ff6c0271132cb6dd77409de195e07ce0292d97e1`  
		Last Modified: Tue, 16 Apr 2024 04:53:38 GMT  
		Size: 350.1 MB (350055249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57caa49d110e6b928dd721367ccb5994179cdd33d372cf09d1af654dfd49497`  
		Last Modified: Tue, 16 Apr 2024 04:52:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736c6798182a660c26a4ca0d8b0916011f1eeb84a0da6ad1fbc755aed9c61734`  
		Last Modified: Tue, 16 Apr 2024 04:52:54 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8226c99d58bfe0912fd2ea6d06574e41a6d97731ad7e3974be2b2ec43bda3c7c`  
		Last Modified: Tue, 16 Apr 2024 04:52:55 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13eabeba1b2bf7f44ce384a746c99ab4861e83a9b3c0e6afaad652080f61b4de`  
		Last Modified: Tue, 16 Apr 2024 04:52:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37051295175f43e4822add9a41d8f64c9fb270d332916966aa7e04e0ddf0f1e1`  
		Last Modified: Tue, 16 Apr 2024 04:52:54 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6568c4c822d1f0a0ffb81cefb51b80be8188279e9a182f5cb2592820cfad7b52`  
		Last Modified: Tue, 16 Apr 2024 04:52:54 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:69549a2ec3de24455cac9a694ac6f9ff74d55f14785c4f88e8bf765881617aa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367767970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f48a8ecb40ac6e6afd4365d685b48f1c7a75f105a16c82b4212df095daffbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:19:13 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:19:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 03:21:17 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:21:17 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:21:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:21:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:21:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:22:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:22:02 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:22:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 03:22:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:22:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:22:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:22:04 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 03:22:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:22:04 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:22:04 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:22:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11863ef3e894dd6ffa24e5592f86fc52b51e62391229ae4e356dbf4f9f565c4f`  
		Last Modified: Tue, 16 Apr 2024 03:26:52 GMT  
		Size: 6.0 MB (6027895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050cd1760032ad0930988694136c07112902c2fa6d05b175000bfe7fe7e8ae41`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 938.2 KB (938223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1da51bcdc61f69943ae37b39dbe437c08b49cf442dc34e92b3fb51806066c2`  
		Last Modified: Tue, 16 Apr 2024 03:27:52 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f5953723e88dcc8bf7500f20bc2a69383045b80484d521120f2f240ba60939`  
		Last Modified: Tue, 16 Apr 2024 03:28:21 GMT  
		Size: 333.6 MB (333592108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c146994ee34ff0ce90827e0aa56b326e33443657578fd8dd028d7405d7c37b`  
		Last Modified: Tue, 16 Apr 2024 03:27:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0550e546386bf516846b61c3d53de8e3baf1d1f8ada0adc8917045610cb4869`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5f1f70fa8ad847efc8befbd198421514d6dcd1046f321108963ee579fc93ed`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 728.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f7729fa51b580e193e72c17264ec0dffbf11cc79ffe3e78f154666962c5237`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1e37bdb95e4d75054d5ac94fd067f417b6b8a37a9ddbb7ef79ace81e1a44cb`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03590bd811827aa9264803266c094566248e3242e05c37eba419e763cc5a2c0`  
		Last Modified: Tue, 16 Apr 2024 03:27:50 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:cb5770e190f393c923386dca3c71e29a9e27844298cef14f206333dc03637eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:100cae80fc70fec6482e12b47cf24ca5a9b47e99eefd8f676caaf67e086f0d4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726130679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1256799c47bc88935fc7deac454d87f0d0a01794a09fc37fb2cfbafb33d70016`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:40:16 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:40:58 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:40:59 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:40:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:40:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:42:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:42:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:42:26 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:42:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 04:42:27 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:42:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:42:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:42:28 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 04:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:42:28 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:42:28 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:42:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd3db21ebd06129580fcbeb1a7c1a8b4de2a102d38a2618a00a8037f4b97498`  
		Last Modified: Tue, 16 Apr 2024 04:51:38 GMT  
		Size: 6.2 MB (6186299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e98997fd1c5843cfd8861998c579c903a1f6dcc4d008cc6304bbcd2a9c1430c`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.1 MB (1092150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c039cbe5cfe3b3e44672e2a2d6cab1cad823f888882173f1068d3758dcd757`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56b935084669bdfd3b872fd758b7bbac7a1a6b4866303f939c299596faa9bd2`  
		Last Modified: Tue, 16 Apr 2024 04:52:41 GMT  
		Size: 690.3 MB (690262973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16520dcd69488d59ca335969dadbd0cdc0625c3cee5cf500d5a38a57e9595417`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786fb049c9b0a1768dcf30589d061963fad22c4b0628e6af4fe56a74c757de19`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcb79a54d543e85f23b529085481a77fac30a3b9b58b67f0052fd3816ee81dc`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 729.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b850079650e2bb938b75bf7ac16a360b496f0886fe9293a3d6bf9993968783be`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfafd2f90526ea6f2d0f367585ba614b723a87757c209f0583dd421f92b4e17e`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280c967059329600f12508b225f7319859b0246bac84956afdb45bfd37817c19`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:3c7c6163dec118093b3c1d173b47ae299010c11fba531db05589d8b0c68a7c9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9628cf02ec68b07c5a1e590139f11b9b07910c3bac3aa4f764a9cb1cc582282b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:19:13 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:19:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:19:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:19:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:20:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:21:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:21:01 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:21:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 03:21:02 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:21:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:21:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:21:03 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 03:21:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:21:03 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:21:03 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:21:03 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11863ef3e894dd6ffa24e5592f86fc52b51e62391229ae4e356dbf4f9f565c4f`  
		Last Modified: Tue, 16 Apr 2024 03:26:52 GMT  
		Size: 6.0 MB (6027895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050cd1760032ad0930988694136c07112902c2fa6d05b175000bfe7fe7e8ae41`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 938.2 KB (938223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aacb5568ffaa5e455a84e0a4e3e26c50680d093bf23e5347351233691c5ae17`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811495152e6c0b20a24472561240fa58446e1a4b800378830ffd871e8fe9ea1a`  
		Last Modified: Tue, 16 Apr 2024 03:27:37 GMT  
		Size: 665.1 MB (665134412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00635e297efd98909d1f1e76d4fcba4ae15072c025032ab4bf34918aca6482`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a27cb8eaa05c9a2ac24d5f60222785903edaaef8b2aac75c23c9da896f069`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4151ecc05ff245c9960139bc679a16d43f39a95f6357a5dbd83ad1612054879d`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 727.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e259246b1be5ddfb73a64b064b5fa48332422b4eba041891f764cc5b9b22e`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ef10a6faeba6a8342963d0edfdc92bc2d63b7e9628b641e07d0319098084f0`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabab6402e5358b1050646bd4d720f60a9fe2aabb528ee30ca91ec295af515a6`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.0.5`

```console
$ docker pull couchbase@sha256:3485bb06b22d42803de0eb56fd35fcdf6772acab9bcf66d7f838f2fa28bf10d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:efab41d8b70dbf1ab0bdac3146be29230f8b2c31ac22fd04f2e805bfbaf53572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.7 MB (616705467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c797f8b300d809376605d3cb1533cdc39d55a83ab55a9e86a7d228532d2362f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:48:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5
# Tue, 16 Apr 2024 04:48:49 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb
# Tue, 16 Apr 2024 04:48:49 GMT
ARG CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea
# Tue, 16 Apr 2024 04:48:49 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:48:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:48:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:50:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:50:04 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 04:50:05 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:50:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:50:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:50:06 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 04:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:50:06 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:50:06 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:50:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2539cc6714d28ae08856da9a1375e679890fea343b120abb8b5ad0d44be436`  
		Last Modified: Tue, 16 Apr 2024 04:53:50 GMT  
		Size: 6.3 MB (6286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e300a40474735d3e4dd215ab1ffb4572611a70ccce1c7de29378314c1b012c1`  
		Last Modified: Tue, 16 Apr 2024 04:57:35 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0362e4873e4ff14a6376c605480886544f83a01c71937fb043773e03650e4c7a`  
		Last Modified: Tue, 16 Apr 2024 04:58:30 GMT  
		Size: 581.8 MB (581829953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8783efece9f0eb8f96f4044b8eb986edf115576dd5b7df6ca2ac12e7cef982b3`  
		Last Modified: Tue, 16 Apr 2024 04:57:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987e434c35466f3273009f91523ce1ceaa74f9664b89df12855a01a5860c3d9`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8b054ba3c1870f58ab5c76e33d67d61fcbe4abc1687bc842c83ce23db06513`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39352bcf77d263ce4d593200e68ddf97e19c1caa90c5fc76680803867e3b2105`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501e3a27ebeb4a76bf012503d912b1c897fe2c6ccc893dd328d603fd5201812`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48f36e7ba5b483a531df7a7f3a32f81cafe359789eaca45d75c74530843f4ff`  
		Last Modified: Tue, 16 Apr 2024 04:57:33 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.1.6`

```console
$ docker pull couchbase@sha256:6b057fd6e5b3328736eb66f04ca9a00aa429a9f1e54badb81897f2700288a031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.1.6` - linux; amd64

```console
$ docker pull couchbase@sha256:4c812ed1e60d9f424e2dc394e0e69f10aee6bb2fd753caf918d8353d71b64e1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.0 MB (652023382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f40536f2fc61bfd047326255ccee239ecd869e808eb8c592b4560ec219b54e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:46:11 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Tue, 16 Apr 2024 04:46:11 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:46:11 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:46:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:46:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:47:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:47:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:47:31 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:47:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 04:47:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:47:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:47:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:47:32 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 04:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:47:33 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:47:33 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:47:33 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2539cc6714d28ae08856da9a1375e679890fea343b120abb8b5ad0d44be436`  
		Last Modified: Tue, 16 Apr 2024 04:53:50 GMT  
		Size: 6.3 MB (6286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de27bf474791f4838b95d1e9df0760e45d664cea6d0be50adc3c6bcdb88fa09d`  
		Last Modified: Tue, 16 Apr 2024 04:55:44 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c09bc767d9349d7a4821734cd0f3f541f23ec07d5dd90de2a1628432553f19`  
		Last Modified: Tue, 16 Apr 2024 04:56:40 GMT  
		Size: 617.1 MB (617147861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2bc163d643487b1c65e838c43871f921b9a753852177ba6cfb162b36cb036e`  
		Last Modified: Tue, 16 Apr 2024 04:55:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0e508e0fe5d9ee3ac6edd740938681a9e3477e0167ac7e8a87e56a33f6e66e`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 745.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d522f04a9aa527c28206d72467435dc4189be9a1fbc7e8d7537ab9bf41ac40f3`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be49c3886edf3eb54f8d9adb99d8b9461d9c1815cb4540efa014d873abbc18`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1378631c28c11ec2326222524fd695b4ddf5d0feb9cca410b70ce90710dba981`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2cc64b78533624d9c689059875cf98a05208e11a1bbcf73fc9b9820ed66ecd`  
		Last Modified: Tue, 16 Apr 2024 04:55:42 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.1.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:b5918273452f7476d9126b64a01e59f10c78e11629e22df48a13efdf05715317
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.6 MB (622645424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c08463535e86a72ec75873b003194db8f48e879296911f9af0d6944b6e8da8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:22:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:24:26 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Tue, 16 Apr 2024 03:24:26 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:24:26 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:24:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:24:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:25:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:25:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:25:36 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:25:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 03:25:36 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:25:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:25:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:25:37 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 03:25:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:25:38 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:25:38 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:25:38 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc63a620f1ecf9579c760cf290f09f23af0305d47d3bb6f3cbcaf31145979bb8`  
		Last Modified: Tue, 16 Apr 2024 03:28:32 GMT  
		Size: 6.1 MB (6110804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb6a2b048134d934f7ae7455f485d0618e4d741599cc5da7dc720fa7d4fa7ea`  
		Last Modified: Tue, 16 Apr 2024 03:29:57 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0475936cd5e1a71d183cd309be55db1438ec9732a6dc922b696f7d45506b809c`  
		Last Modified: Tue, 16 Apr 2024 03:30:37 GMT  
		Size: 589.3 MB (589325278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a22915dc26ebcad4be666d4a3225dd4a1f111157da68655bbbc1c794c3547cb`  
		Last Modified: Tue, 16 Apr 2024 03:29:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10e79084f8cb9f37683e84b1a572bfb2e47affb34a1ef05a4a6bc069c80468a`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b05f1a4aa3a47b1668369d48fcd4c65aa2ce076b2344d7a9432a4964a098f5`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9f7052f4d09ccc89fa9a86586da4ffe99cbdfb022b615f2fd439910f910529`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d18565aa5295992120b18436727334a97b352ff6fa4c50c04074589a04931d`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5804046ac2041bc67551e84ab308a8559056f1b25faccf288598475d157b207`  
		Last Modified: Tue, 16 Apr 2024 03:29:55 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.2.5`

```console
$ docker pull couchbase@sha256:c2440765beab91a46ea9d944d0d02f789b11b8c756fbc5feae4a036e9c9dc970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.2.5` - linux; amd64

```console
$ docker pull couchbase@sha256:9d5f00a9ec6436c107bedfd30b7c80e9ffa88dd320f7598423b0324fc37f1816
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.2 MB (644222759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0949150a2eb0a12d7366e0ce528fb870db3721f917d524d825e887eeefd36710`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:40:16 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:40:58 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 25 Apr 2024 01:28:12 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 25 Apr 2024 01:28:13 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 01:28:13 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 01:28:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 01:28:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 01:29:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 01:29:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 01:29:38 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 01:29:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 25 Apr 2024 01:29:39 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 01:29:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 01:29:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 01:29:40 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 25 Apr 2024 01:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 01:29:40 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 01:29:40 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 01:29:40 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd3db21ebd06129580fcbeb1a7c1a8b4de2a102d38a2618a00a8037f4b97498`  
		Last Modified: Tue, 16 Apr 2024 04:51:38 GMT  
		Size: 6.2 MB (6186299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e98997fd1c5843cfd8861998c579c903a1f6dcc4d008cc6304bbcd2a9c1430c`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.1 MB (1092150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cfe8d94f41ddf50bcf1ba26515674210275309cddc7342102b9ad53071d72b`  
		Last Modified: Thu, 25 Apr 2024 01:30:21 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9b7c93f1b2cf1ae39cbccc83d4d05ffbc848d21f5bf7d1c942896abee92494`  
		Last Modified: Thu, 25 Apr 2024 01:31:15 GMT  
		Size: 608.4 MB (608354724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f04f1439e8af39c0a98eb1196dabf13edb394d68053c054c34f06667ebd9226`  
		Last Modified: Thu, 25 Apr 2024 01:30:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd7bffa7f738d29066267e490c1e2c0f7b3e49de9c776b49d09d055fc5c2f52`  
		Last Modified: Thu, 25 Apr 2024 01:30:19 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cae686a9e723a12c5059cb41c8ef28c8ca57f0369b5c47f8d85fd94d6036384`  
		Last Modified: Thu, 25 Apr 2024 01:30:18 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e41c37d8300df4ee7545cfde8299af6b2201b273dec302a27abc8d39ff9e536`  
		Last Modified: Thu, 25 Apr 2024 01:30:18 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627b303f7b18d93ba32f9c1ea717ae0b87498b11061ba1ce483d75ffce63c321`  
		Last Modified: Thu, 25 Apr 2024 01:30:18 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090eaa4a461fbfa3fa271ba91e4b41a704ee4cc80b11b3a78e1e6acb009d8288`  
		Last Modified: Thu, 25 Apr 2024 01:30:18 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.2.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:bee99da783dfe814f89be86857c3b426b017c7fa7b753b05045a3206ba3dd04b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.8 MB (619808577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c4570529f604e0c09f02661e574667c675237dfd7a307f87d463b0d2a9fcad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:19:13 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:19:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 25 Apr 2024 00:09:41 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 25 Apr 2024 00:09:41 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 00:09:41 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 00:09:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 00:09:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 00:10:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 00:10:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 00:10:55 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 00:10:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 25 Apr 2024 00:10:55 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 00:10:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 00:10:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 00:10:56 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 25 Apr 2024 00:10:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 00:10:56 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 00:10:56 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 00:10:56 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11863ef3e894dd6ffa24e5592f86fc52b51e62391229ae4e356dbf4f9f565c4f`  
		Last Modified: Tue, 16 Apr 2024 03:26:52 GMT  
		Size: 6.0 MB (6027895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050cd1760032ad0930988694136c07112902c2fa6d05b175000bfe7fe7e8ae41`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 938.2 KB (938223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83063714dbddc5fbf5d803d8c5336eff69daad667202bda8bef0dc079eb2edf`  
		Last Modified: Thu, 25 Apr 2024 00:11:23 GMT  
		Size: 1.8 KB (1846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9a43b70b2a5720a58763f565ff4288632ad82e4cba8901ad58aaebc489846b`  
		Last Modified: Thu, 25 Apr 2024 00:12:05 GMT  
		Size: 585.6 MB (585632400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367f6e0682b19cb1c81dc0dc3b9312c09e8a6b7056dd73a9b598447ce1d930b8`  
		Last Modified: Thu, 25 Apr 2024 00:11:23 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51dda503d78d35504aabffe05c0a377d863a95ecc822ce73c8282cd13124acc`  
		Last Modified: Thu, 25 Apr 2024 00:11:22 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573deaea6e0d377f7c2f4a9830daf4f43f629474b042950057de1893ef438b14`  
		Last Modified: Thu, 25 Apr 2024 00:11:21 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ec76e00a535f6cbecae38ea732fef92fc378f70b158004f8cef16a16004a9`  
		Last Modified: Thu, 25 Apr 2024 00:11:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4494f8f6b9f3977c653eacf0bf303d2b8449983868cd7203bb0d2296e6095900`  
		Last Modified: Thu, 25 Apr 2024 00:11:21 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf767162aa984b035c4fd22f1ad3c52bfa38fa51b4f6111c709647bb89b2`  
		Last Modified: Thu, 25 Apr 2024 00:11:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.6.1`

```console
$ docker pull couchbase@sha256:cb5770e190f393c923386dca3c71e29a9e27844298cef14f206333dc03637eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:100cae80fc70fec6482e12b47cf24ca5a9b47e99eefd8f676caaf67e086f0d4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726130679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1256799c47bc88935fc7deac454d87f0d0a01794a09fc37fb2cfbafb33d70016`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:40:16 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:40:58 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:40:59 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:40:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:40:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:42:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:42:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:42:26 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:42:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 04:42:27 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:42:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:42:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:42:28 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 04:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:42:28 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:42:28 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:42:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd3db21ebd06129580fcbeb1a7c1a8b4de2a102d38a2618a00a8037f4b97498`  
		Last Modified: Tue, 16 Apr 2024 04:51:38 GMT  
		Size: 6.2 MB (6186299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e98997fd1c5843cfd8861998c579c903a1f6dcc4d008cc6304bbcd2a9c1430c`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.1 MB (1092150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c039cbe5cfe3b3e44672e2a2d6cab1cad823f888882173f1068d3758dcd757`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56b935084669bdfd3b872fd758b7bbac7a1a6b4866303f939c299596faa9bd2`  
		Last Modified: Tue, 16 Apr 2024 04:52:41 GMT  
		Size: 690.3 MB (690262973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16520dcd69488d59ca335969dadbd0cdc0625c3cee5cf500d5a38a57e9595417`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786fb049c9b0a1768dcf30589d061963fad22c4b0628e6af4fe56a74c757de19`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcb79a54d543e85f23b529085481a77fac30a3b9b58b67f0052fd3816ee81dc`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 729.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b850079650e2bb938b75bf7ac16a360b496f0886fe9293a3d6bf9993968783be`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfafd2f90526ea6f2d0f367585ba614b723a87757c209f0583dd421f92b4e17e`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280c967059329600f12508b225f7319859b0246bac84956afdb45bfd37817c19`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:3c7c6163dec118093b3c1d173b47ae299010c11fba531db05589d8b0c68a7c9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9628cf02ec68b07c5a1e590139f11b9b07910c3bac3aa4f764a9cb1cc582282b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:19:13 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:19:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:19:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:19:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:20:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:21:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:21:01 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:21:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 03:21:02 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:21:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:21:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:21:03 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 03:21:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:21:03 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:21:03 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:21:03 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11863ef3e894dd6ffa24e5592f86fc52b51e62391229ae4e356dbf4f9f565c4f`  
		Last Modified: Tue, 16 Apr 2024 03:26:52 GMT  
		Size: 6.0 MB (6027895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050cd1760032ad0930988694136c07112902c2fa6d05b175000bfe7fe7e8ae41`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 938.2 KB (938223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aacb5568ffaa5e455a84e0a4e3e26c50680d093bf23e5347351233691c5ae17`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811495152e6c0b20a24472561240fa58446e1a4b800378830ffd871e8fe9ea1a`  
		Last Modified: Tue, 16 Apr 2024 03:27:37 GMT  
		Size: 665.1 MB (665134412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00635e297efd98909d1f1e76d4fcba4ae15072c025032ab4bf34918aca6482`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a27cb8eaa05c9a2ac24d5f60222785903edaaef8b2aac75c23c9da896f069`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4151ecc05ff245c9960139bc679a16d43f39a95f6357a5dbd83ad1612054879d`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 727.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e259246b1be5ddfb73a64b064b5fa48332422b4eba041891f764cc5b9b22e`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ef10a6faeba6a8342963d0edfdc92bc2d63b7e9628b641e07d0319098084f0`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabab6402e5358b1050646bd4d720f60a9fe2aabb528ee30ca91ec295af515a6`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:cb5770e190f393c923386dca3c71e29a9e27844298cef14f206333dc03637eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:100cae80fc70fec6482e12b47cf24ca5a9b47e99eefd8f676caaf67e086f0d4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726130679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1256799c47bc88935fc7deac454d87f0d0a01794a09fc37fb2cfbafb33d70016`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:40:16 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:40:58 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 04:40:58 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:40:59 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:40:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:40:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:42:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:42:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:42:26 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:42:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 04:42:27 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:42:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:42:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:42:28 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 04:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:42:28 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:42:28 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:42:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd3db21ebd06129580fcbeb1a7c1a8b4de2a102d38a2618a00a8037f4b97498`  
		Last Modified: Tue, 16 Apr 2024 04:51:38 GMT  
		Size: 6.2 MB (6186299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e98997fd1c5843cfd8861998c579c903a1f6dcc4d008cc6304bbcd2a9c1430c`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.1 MB (1092150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c039cbe5cfe3b3e44672e2a2d6cab1cad823f888882173f1068d3758dcd757`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56b935084669bdfd3b872fd758b7bbac7a1a6b4866303f939c299596faa9bd2`  
		Last Modified: Tue, 16 Apr 2024 04:52:41 GMT  
		Size: 690.3 MB (690262973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16520dcd69488d59ca335969dadbd0cdc0625c3cee5cf500d5a38a57e9595417`  
		Last Modified: Tue, 16 Apr 2024 04:51:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786fb049c9b0a1768dcf30589d061963fad22c4b0628e6af4fe56a74c757de19`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bcb79a54d543e85f23b529085481a77fac30a3b9b58b67f0052fd3816ee81dc`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 729.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b850079650e2bb938b75bf7ac16a360b496f0886fe9293a3d6bf9993968783be`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfafd2f90526ea6f2d0f367585ba614b723a87757c209f0583dd421f92b4e17e`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280c967059329600f12508b225f7319859b0246bac84956afdb45bfd37817c19`  
		Last Modified: Tue, 16 Apr 2024 04:51:35 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:latest` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:3c7c6163dec118093b3c1d173b47ae299010c11fba531db05589d8b0c68a7c9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699310269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9628cf02ec68b07c5a1e590139f11b9b07910c3bac3aa4f764a9cb1cc582282b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:19:13 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:19:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:19:46 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:19:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:19:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:20:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:21:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:21:01 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:21:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Tue, 16 Apr 2024 03:21:02 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:21:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:21:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:21:03 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Tue, 16 Apr 2024 03:21:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:21:03 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:21:03 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:21:03 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11863ef3e894dd6ffa24e5592f86fc52b51e62391229ae4e356dbf4f9f565c4f`  
		Last Modified: Tue, 16 Apr 2024 03:26:52 GMT  
		Size: 6.0 MB (6027895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050cd1760032ad0930988694136c07112902c2fa6d05b175000bfe7fe7e8ae41`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 938.2 KB (938223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aacb5568ffaa5e455a84e0a4e3e26c50680d093bf23e5347351233691c5ae17`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811495152e6c0b20a24472561240fa58446e1a4b800378830ffd871e8fe9ea1a`  
		Last Modified: Tue, 16 Apr 2024 03:27:37 GMT  
		Size: 665.1 MB (665134412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00635e297efd98909d1f1e76d4fcba4ae15072c025032ab4bf34918aca6482`  
		Last Modified: Tue, 16 Apr 2024 03:26:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6a27cb8eaa05c9a2ac24d5f60222785903edaaef8b2aac75c23c9da896f069`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4151ecc05ff245c9960139bc679a16d43f39a95f6357a5dbd83ad1612054879d`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 727.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0e259246b1be5ddfb73a64b064b5fa48332422b4eba041891f764cc5b9b22e`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ef10a6faeba6a8342963d0edfdc92bc2d63b7e9628b641e07d0319098084f0`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabab6402e5358b1050646bd4d720f60a9fe2aabb528ee30ca91ec295af515a6`  
		Last Modified: Tue, 16 Apr 2024 03:26:49 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
