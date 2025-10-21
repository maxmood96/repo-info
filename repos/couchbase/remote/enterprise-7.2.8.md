## `couchbase:enterprise-7.2.8`

```console
$ docker pull couchbase@sha256:03e6e52d7bff38338e520857af1d0a35ffb710fe6c231e1528404d2f6139dde8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.8` - linux; amd64

```console
$ docker pull couchbase@sha256:e9e65ba2c373af6a853e7e5aa0ecf1c8f6ff2ba6816c5fe03c6085436707d201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.0 MB (701966462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3a9f9d0946009b4644115941909e280343e70e24bcaf13d9d2189c2e387fb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 02 Sep 2025 18:23:14 GMT
ARG RELEASE
# Tue, 02 Sep 2025 18:23:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Sep 2025 18:23:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Sep 2025 18:23:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 02 Sep 2025 18:23:14 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 02 Sep 2025 18:23:14 GMT
CMD ["/bin/bash"]
# Tue, 02 Sep 2025 18:23:14 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 02 Sep 2025 18:23:14 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 02 Sep 2025 18:23:14 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8
# Tue, 02 Sep 2025 18:23:14 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb
# Tue, 02 Sep 2025 18:23:14 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 02 Sep 2025 18:23:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=09e11da52bc7aac2ecd12c33b7983f72cddb33b247d837cc6f3590483c45ad1c            ;;          'amd64')            CB_SHA256=ce04775b8070a5c810060abd80db286aa050fe082eba6890ed387f730ebfea8a            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Sep 2025 18:23:14 GMT
CMD ["couchbase-server"]
# Tue, 02 Sep 2025 18:23:14 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 02 Sep 2025 18:23:14 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08726b8225067c05c80f4b695468cac6185c4b0d8ae83fe936b6d354704c653d`  
		Last Modified: Tue, 21 Oct 2025 00:10:26 GMT  
		Size: 44.5 MB (44485807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8163e72312f80b5a581f685c0bc867b8b2b27511700def4fea273af16aada736`  
		Last Modified: Tue, 21 Oct 2025 00:10:17 GMT  
		Size: 878.1 KB (878073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c38f39875a2babc48126ed6ab0c0bb4375532b74943a4268ccf15e467c033ee`  
		Last Modified: Tue, 21 Oct 2025 00:11:51 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e2b95e56bf3f49cb1358e6d69827e3cdbeb93ce9536bfa5002d3d9c7e8b90e`  
		Last Modified: Tue, 21 Oct 2025 02:32:49 GMT  
		Size: 626.9 MB (626872455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994a4f2e3cfcc2077a1396fc69352aefcb33fa64afbc38a166cc04f24304400`  
		Last Modified: Tue, 21 Oct 2025 00:11:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665631f8e95ecef6f09fec9f3c409a892521328bfcc8e9be863308f57cf5b88`  
		Last Modified: Tue, 21 Oct 2025 00:11:51 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e79bb8810561985bc9d3bd707b43a74da72c64b6f4c776deca2223cb997b7ef`  
		Last Modified: Tue, 21 Oct 2025 00:11:51 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca9d1a3a01768e72e546e03ccb646b547e8b972dbf7e0c8aae457cf3b3971f3`  
		Last Modified: Tue, 21 Oct 2025 00:11:51 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b29eb6f5bebf48763bb241d27bec5eb948d2ee3cb033b12a6ea9da3124aaa1d`  
		Last Modified: Tue, 21 Oct 2025 00:11:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df63405c8bbb411fae973e03b31036b0b01e93d3fc7e5796fe0624ba8dcade45`  
		Last Modified: Tue, 21 Oct 2025 00:11:51 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.8` - unknown; unknown

```console
$ docker pull couchbase@sha256:8a2d0162afbf957c38c5b3b23438dcd14646a84b74984c066a79e007ee2d9f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3bbff2489e91db89c384b505c64af98d0d136ab4d66cc301306b442106ad42`

```dockerfile
```

-	Layers:
	-	`sha256:4649dc1a2f7599d7e78ec840ce90fe4c92093714b1b0e8a2e39b7dab25052262`  
		Last Modified: Tue, 21 Oct 2025 02:31:25 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.8` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:2e35e0b6458b653612755b712eee096909dd12091dad3417bb125870823f83a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.3 MB (677296660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b17e835c33d99ba26e8203daf1374126720e9e0fe14fee6d7208eec7bfca70e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 02 Sep 2025 18:23:14 GMT
ARG RELEASE
# Tue, 02 Sep 2025 18:23:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 02 Sep 2025 18:23:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 02 Sep 2025 18:23:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 02 Sep 2025 18:23:14 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 02 Sep 2025 18:23:14 GMT
CMD ["/bin/bash"]
# Tue, 02 Sep 2025 18:23:14 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 02 Sep 2025 18:23:14 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 02 Sep 2025 18:23:14 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8
# Tue, 02 Sep 2025 18:23:14 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb
# Tue, 02 Sep 2025 18:23:14 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 02 Sep 2025 18:23:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=09e11da52bc7aac2ecd12c33b7983f72cddb33b247d837cc6f3590483c45ad1c            ;;          'amd64')            CB_SHA256=ce04775b8070a5c810060abd80db286aa050fe082eba6890ed387f730ebfea8a            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.8 CB_PACKAGE=couchbase-server-enterprise_7.2.8-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 02 Sep 2025 18:23:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Sep 2025 18:23:14 GMT
CMD ["couchbase-server"]
# Tue, 02 Sep 2025 18:23:14 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 02 Sep 2025 18:23:14 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce597d9231c2b2fd28e453307fae8eb26db66a418796e5098de2fbd21888f759`  
		Last Modified: Tue, 21 Oct 2025 00:09:54 GMT  
		Size: 44.3 MB (44302649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c3a5990b9043b1bc77a49401dd00b60640beb103eb812e76eed3091a9b593a`  
		Last Modified: Tue, 21 Oct 2025 00:09:49 GMT  
		Size: 765.1 KB (765129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99366659b6abf7e1f37d36d6ff75e4ddfc94effb5c299ca2ae1da07ce917e1d4`  
		Last Modified: Tue, 21 Oct 2025 00:11:24 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27debb2f4f7eab31866c1c7f90d277200e8920f7d8b97d73acd1969b004afa7`  
		Last Modified: Tue, 21 Oct 2025 02:32:30 GMT  
		Size: 603.4 MB (603360195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082d8f1906b96b428fb57cdca4ccf1d207ee00710a6bd1c86bf2d838de699a9b`  
		Last Modified: Tue, 21 Oct 2025 00:11:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a625b1dd40cb4d9f02bfe882ddd8c51562709ca5e1c16758e787354bb29aa0f2`  
		Last Modified: Tue, 21 Oct 2025 00:11:24 GMT  
		Size: 812.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980736e0ca3e4e5f80d7f83dd922bf0883d6e537edc2da7698d82dba4cfc9731`  
		Last Modified: Tue, 21 Oct 2025 00:11:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1021e1318474e3b3574dea2556cc0be0123c311e804b4c72cd68e7c20d70aa0`  
		Last Modified: Tue, 21 Oct 2025 00:11:24 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45431eb3eec67d24b4a348df4759d2bb46ceb99fb28e7333ed18a574c1026993`  
		Last Modified: Tue, 21 Oct 2025 00:11:24 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d4601e583dbaec77dab1fdb249535c3c60efa8bd6b949c8f738b2bc9118386`  
		Last Modified: Tue, 21 Oct 2025 00:11:24 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.8` - unknown; unknown

```console
$ docker pull couchbase@sha256:c14e1f58c7ff95fef49236dec626bde6136ec5c952d7221c961981ac88020bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcbe98fdbb2503f75311a96fa0ae007ee5e27e1f70128d9670019391cd16c77`

```dockerfile
```

-	Layers:
	-	`sha256:136bd0ea323f89f711a3ee85a0b1eb604b07772c90b0a472d38215db98e6ae73`  
		Last Modified: Tue, 21 Oct 2025 02:31:28 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json
