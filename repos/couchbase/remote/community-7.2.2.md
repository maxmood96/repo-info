## `couchbase:community-7.2.2`

```console
$ docker pull couchbase@sha256:b9e830090347e0f942f9cba852141330dc73692f2704862856acac5ae1c7ade8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:f94e98d2afc0a20ce122a51ef769f751ba0f472b4e0cac32e7b3fe0e31cba9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360341736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956f56f53d941bf0391db4ebfe36e5f5dc56a9ea12ad43ba70d6be83cf8e0a67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 25 Sep 2023 18:22:30 GMT
ARG RELEASE
# Mon, 25 Sep 2023 18:22:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 25 Sep 2023 18:22:30 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 25 Sep 2023 18:22:30 GMT
CMD ["/bin/bash"]
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 25 Sep 2023 18:22:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Sep 2023 18:22:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 18:22:30 GMT
CMD ["couchbase-server"]
# Mon, 25 Sep 2023 18:22:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 25 Sep 2023 18:22:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3ec0891edfe72628d17d0587ba03566bc9ad56c0a8e1c63fb6840a1ecf1254`  
		Last Modified: Tue, 25 Mar 2025 18:26:09 GMT  
		Size: 6.3 MB (6289461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984063a92d478b23382f6cb1971468f4522dc0ba9f663f35c275e2aa563cd411`  
		Last Modified: Tue, 25 Mar 2025 18:26:09 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2cffeec482f341415d02807a8f7a99377d2588ff401914879fdf2f191d97f0`  
		Last Modified: Tue, 25 Mar 2025 18:26:14 GMT  
		Size: 326.5 MB (326536906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7822fb98a9319369d1dad1f4db60a65a2b574302e4c6312b9bb7128ebb11cfd`  
		Last Modified: Tue, 25 Mar 2025 18:26:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f930871f81256fc3221133b674e2589c213b6ae9efe98ef4888cfc2bc60111`  
		Last Modified: Tue, 25 Mar 2025 18:26:10 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefcb87ce99c9329e2cdce17e8ba39346b642104f50c4b59b4942a7e8ed98b63`  
		Last Modified: Tue, 25 Mar 2025 18:26:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef6d8adc66708097caf479c884a0b725ab2adae291e0d2bff92a53d2a6ba2a1`  
		Last Modified: Tue, 25 Mar 2025 18:26:10 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4621b0957ad9ccfd5270c888c9b6fa5613d91bf26827e8a7c59115ffd0cd23a8`  
		Last Modified: Tue, 25 Mar 2025 18:26:11 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17414a0a72de4aefcbb2ee6178c33addf273162d02c2a8aa4c2abc27edaf0d`  
		Last Modified: Tue, 25 Mar 2025 18:26:11 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:a38da6809889f1938bff74e4c22c52f57fb74824654f85d034b25f16d4586f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e5e9b92bc78668b75a93c61e23e4d2c4f81ee04990b3deeb624eb3be46f47d`

```dockerfile
```

-	Layers:
	-	`sha256:23945897d874b2a2bab62ba9ef71b2eb679aff42796e55b3de573ddc488d5dde`  
		Last Modified: Tue, 25 Mar 2025 18:26:09 GMT  
		Size: 31.5 KB (31499 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:de82c44ab0dd6b8fcbd8c8d61052b0d837f6bbf0eb94072bf2aa942cad94a3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336801117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e72c161192fb4ac88fb0e06ec0ea1bed634a59c4dadf55d3ba35e503bb4d82f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 25 Sep 2023 18:22:30 GMT
ARG RELEASE
# Mon, 25 Sep 2023 18:22:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 25 Sep 2023 18:22:30 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Mon, 25 Sep 2023 18:22:30 GMT
CMD ["/bin/bash"]
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 25 Sep 2023 18:22:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Sep 2023 18:22:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 18:22:30 GMT
CMD ["couchbase-server"]
# Mon, 25 Sep 2023 18:22:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 25 Sep 2023 18:22:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7adba9b0542e93699c52971597bd4014b2c549e408406c9fac91d57426d185`  
		Last Modified: Tue, 25 Mar 2025 18:55:40 GMT  
		Size: 6.1 MB (6119257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdde954d60a248aad50cf33605f3d01be95927fca7ce9c5cdcdc61782c185041`  
		Last Modified: Tue, 25 Mar 2025 18:55:39 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87adb34f6ed8fbf6806f673bec0a2034f2885733bb25e0ad28d45ba7777216d7`  
		Last Modified: Tue, 25 Mar 2025 18:55:48 GMT  
		Size: 304.7 MB (304703715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771c95e1febf9e3fa860cf1b86ee3a8da9275ccaf3b5fe616e0bc7c668acd15a`  
		Last Modified: Tue, 25 Mar 2025 18:55:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5338ef1d678d5c9e524aaf65dea11d001ab1ccd5ed789b4b5b700acd877bd0bb`  
		Last Modified: Tue, 25 Mar 2025 18:55:40 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fa4b2d758163b05c2539527e31d2a74e79269753e53fa59944cace3c15d251`  
		Last Modified: Tue, 25 Mar 2025 18:55:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f458211c895a68aa5beb66ca0adbfebc9b6de0f8402e96ba90fc30ecd54c4726`  
		Last Modified: Tue, 25 Mar 2025 18:55:41 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab6972b63e4008c7df873ab9e4ad33357ffeb5d460b6fb68e4a468f715b646`  
		Last Modified: Tue, 25 Mar 2025 18:55:41 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca765b769f531cc3239c5878b7ea51f511c2b73be1bce28f987392695025b7a`  
		Last Modified: Tue, 25 Mar 2025 18:55:41 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:c9a376600cceb0130408f3f3b1b717730b034222490a9ae89fef22b067c76b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120385246d857a42c491d9ab49c83d721a607876ec9e149f890a2efc27369294`

```dockerfile
```

-	Layers:
	-	`sha256:2985d8d7d3aba133550ef1248da5a5387dd8b2fc2ff434550b6195783fba09b7`  
		Last Modified: Tue, 25 Mar 2025 18:55:39 GMT  
		Size: 31.7 KB (31655 bytes)  
		MIME: application/vnd.in-toto+json
