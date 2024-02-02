## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:e1e0a89e104fd3199fc7aba0004b5008702056a7d087129aa8edec9654406d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:18415c4cbdb61fc0da3c58eead4d78525dff2ee655155109aa61cde2bdb92faf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.0 MB (670029391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbb0f5f6965e30ec7917749c4de1fab9b1e5e297d971c35bef9eeb725426a81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:25:59 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Dec 2023 10:26:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 16 Dec 2023 10:26:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:26:18 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Sat, 16 Dec 2023 10:26:18 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Sat, 16 Dec 2023 10:26:18 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Sat, 16 Dec 2023 10:26:18 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 16 Dec 2023 10:26:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Dec 2023 10:26:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Dec 2023 10:27:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:27:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Dec 2023 10:27:40 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Sat, 16 Dec 2023 10:27:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Dec 2023 10:27:41 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Dec 2023 10:27:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Dec 2023 10:27:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 16 Dec 2023 10:27:42 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Sat, 16 Dec 2023 10:27:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Dec 2023 10:27:42 GMT
CMD ["couchbase-server"]
# Sat, 16 Dec 2023 10:27:42 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 16 Dec 2023 10:27:42 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78735bf4de6f426e7422bf3d534899d82db0f0d2d66034d6db341ce8d26f0b2`  
		Last Modified: Sat, 16 Dec 2023 10:35:19 GMT  
		Size: 6.3 MB (6286008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de84f8aa811274c19311a984e5405ac2a61a5227477fe24ec3fbe305f97cf89`  
		Last Modified: Sat, 16 Dec 2023 10:35:17 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e041a4b9d588c08b72d8f7f657e4ce93467fcd9cc539126b43484ab1fe9e28`  
		Last Modified: Sat, 16 Dec 2023 10:36:12 GMT  
		Size: 635.2 MB (635154999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9164d43e9daf583b22402ce0651a77e6c21552b2521860a0d998cf102362612`  
		Last Modified: Sat, 16 Dec 2023 10:35:17 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b90a6de88b7882e89a2584cb53f3c93dcca0c1eb69ad8f184163e59380e33`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ec37b4f6e10362278fd677e1e15d6f434617739b005fdbcccae021278f3701`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4513a22f09dd3d7fe1df2c2a9a17deb0aab7d12e935ebfa6df33c1c2fffa049b`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98488eff588073c8b3ca3cbdb24074de5ad27a496b39903482f0b4dacd8b898`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804c21d7cb8de5ef4419d5b801ab528eeb39863ae8cce22b694174a8f3185fdb`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:77507ba22135c21f1682946a8ee17a3cd9d8b4a0ef3e03b268bb74c2046a6bd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615931274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae965c1c56c35662e92a8f45c27dd3be972db3199bd2cb81a5d3fd465a21146`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:33:30 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 02 Feb 2024 01:33:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 02 Feb 2024 01:33:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 02 Feb 2024 01:33:55 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Fri, 02 Feb 2024 01:33:55 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Fri, 02 Feb 2024 01:33:55 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb
# Fri, 02 Feb 2024 01:33:55 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 02 Feb 2024 01:33:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 02 Feb 2024 01:33:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 02 Feb 2024 01:35:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c675d9e2a355cca833c9c12f85585e92a4d1cd95858d79e958b507f9ba1a4349            ;;          'amd64')            CB_SHA256=0f5edf6c011df25e172ae54c6bbe5f83be6a3c24e4e23b25e77d5079262c30ca            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 02 Feb 2024 01:35:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 02 Feb 2024 01:35:10 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 02 Feb 2024 01:35:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 02 Feb 2024 01:35:11 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 02 Feb 2024 01:35:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 02 Feb 2024 01:35:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 02 Feb 2024 01:35:11 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 02 Feb 2024 01:35:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 01:35:12 GMT
CMD ["couchbase-server"]
# Fri, 02 Feb 2024 01:35:12 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Fri, 02 Feb 2024 01:35:12 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747381025e958c41554b8b195053d166fdd604e312c6843f58551c90afd0b5e0`  
		Last Modified: Fri, 02 Feb 2024 01:38:35 GMT  
		Size: 6.1 MB (6112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8f193d75c162586507af0df111597952f22b537ed7b95d6ce89bf20ba699d`  
		Last Modified: Fri, 02 Feb 2024 01:38:34 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4662f50f0510f5f8ad22134abb7a577196575f7ec9aceb259ca1f41db0149df`  
		Last Modified: Fri, 02 Feb 2024 01:39:15 GMT  
		Size: 582.6 MB (582609778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be40297aad9e93344707288721a26ddf725cccfb2ac8d1a66fe7b3527ef5858`  
		Last Modified: Fri, 02 Feb 2024 01:38:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9660f2c986c6fcfab8724bfe605b78bf35af66ed1abb7115aee2df7f51c758`  
		Last Modified: Fri, 02 Feb 2024 01:38:32 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f8ee94c98070db1ebaa7ad2888726105328d17de5407d4666fe4c41eb30d2a`  
		Last Modified: Fri, 02 Feb 2024 01:38:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e581f5505688bc4ca92f089e7ce2cfdb8bf6f87a46ddaf7c6f31ab79bb78e8`  
		Last Modified: Fri, 02 Feb 2024 01:38:32 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9b42bb3bdd7af076a23362657b88834afedbc58c8df7725b1f31e1ce36bd1f`  
		Last Modified: Fri, 02 Feb 2024 01:38:32 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66986a112a197a3ede22bc6aab2d645989172f044a291bf57b04873c9f4625f`  
		Last Modified: Fri, 02 Feb 2024 01:38:32 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
