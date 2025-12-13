## `couchbase:community-7.2.0`

```console
$ docker pull couchbase@sha256:d433a7e0259d2659b1b94c1d467d24dbc48550dfa90d63e8f2db7e4c009be7d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:9fc2952f1a3556dfd156ca140049293257f228d631d6e050571712384a36504e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.8 MB (391844286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e6cad81b578a1570b9024c46557446e881838d0bfc2684f15fa5017e7c3fcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:15:15 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 13 Nov 2025 23:15:15 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 13 Nov 2025 23:15:15 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Nov 2025 23:15:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 13 Nov 2025 23:15:39 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 13 Nov 2025 23:15:39 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 13 Nov 2025 23:15:39 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Thu, 13 Nov 2025 23:15:39 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 13 Nov 2025 23:15:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 13 Nov 2025 23:19:33 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 13 Nov 2025 23:20:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 13 Nov 2025 23:20:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 13 Nov 2025 23:20:07 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 13 Nov 2025 23:20:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 13 Nov 2025 23:20:07 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:20:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 13 Nov 2025 23:20:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 13 Nov 2025 23:20:07 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:20:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:07 GMT
CMD ["couchbase-server"]
# Thu, 13 Nov 2025 23:20:07 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 13 Nov 2025 23:20:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488269fd52db3078eb2c9903ed2569a63ef454acd0930d004623e0e60d1553dc`  
		Last Modified: Thu, 13 Nov 2025 23:17:50 GMT  
		Size: 39.3 MB (39298932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2cb751dec0d1371c4a7ccc0686967468959f7e1938eff78c7132614e9922c`  
		Last Modified: Thu, 13 Nov 2025 23:17:45 GMT  
		Size: 926.7 KB (926720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991e318170fb7d8e4754e57722ab3aac9c67891d4f34a12e1cfb34a5071604ab`  
		Last Modified: Thu, 13 Nov 2025 23:21:04 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2093b686ac93c4521f2c4f611216a288bb4e3f114adfee67696f8833d9a67e5`  
		Last Modified: Fri, 14 Nov 2025 03:34:37 GMT  
		Size: 322.1 MB (322076650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435d1cfb2d5757526686348e1007b9af08d940361488cc94bdd94f8ec6bfcddb`  
		Last Modified: Thu, 13 Nov 2025 23:21:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e692f5f87c99822100d1be63df7fad21c1c0a21d9ae5bc5cde06bc19050b59b`  
		Last Modified: Thu, 13 Nov 2025 23:21:04 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066930dd892cbdd0bec17516dd7e4ceb69c8206c92bae168e58f555682fc619b`  
		Last Modified: Thu, 13 Nov 2025 23:21:03 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0669035cadab3fad284c2b638747703f7dc386b4c40832a49642e3a764e59f`  
		Last Modified: Thu, 13 Nov 2025 23:21:03 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c0eefd079d6c9a26a2131bb0c451046b3f9746a40250473ea7cd22bf5c31ca`  
		Last Modified: Thu, 13 Nov 2025 23:21:03 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaaff88eab37746187593478368e9825fccbb7f02146d0c0e027237fa34bd8e`  
		Last Modified: Thu, 13 Nov 2025 23:21:03 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:c314622d6163e35a503d7aa1addf24a70a65b05c735f27dfdbb609cffb6e224d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457fe305374ca8cd48a09ceecbfc9281c0d66679039a195d1e934ed7bd462a2c`

```dockerfile
```

-	Layers:
	-	`sha256:783d42fa0d7550f6f34257a7ecacd3562d5d369ae513d3d2e504614c064996d6`  
		Last Modified: Fri, 14 Nov 2025 03:33:59 GMT  
		Size: 37.2 KB (37209 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:f44575d9ff30e82d14636a4c4b0b12a48518c45f04c021261568fa54149282d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.2 MB (369161616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3a7be716a6b381d6322bd68d08d4585aa77e9ee86858c26e851a76df2641ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:19:38 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 13 Nov 2025 23:19:38 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 13 Nov 2025 23:19:38 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Nov 2025 23:19:38 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 13 Nov 2025 23:20:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 13 Nov 2025 23:20:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 13 Nov 2025 23:20:06 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Thu, 13 Nov 2025 23:20:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 13 Nov 2025 23:20:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 13 Nov 2025 23:20:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 13 Nov 2025 23:20:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 13 Nov 2025 23:20:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 13 Nov 2025 23:20:37 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 13 Nov 2025 23:20:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 13 Nov 2025 23:20:37 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:20:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 13 Nov 2025 23:20:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 13 Nov 2025 23:20:37 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:20:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:20:37 GMT
CMD ["couchbase-server"]
# Thu, 13 Nov 2025 23:20:37 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 13 Nov 2025 23:20:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2842472a34677a1e17d6d6372088e4eaa290650759e91b8fe9b4576d5fca06`  
		Last Modified: Thu, 13 Nov 2025 23:21:24 GMT  
		Size: 38.9 MB (38872202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5228c3801d2b0ae938ef3fb0afda2bc45e5997cc7e3bf8c7c3ef5e073ac0613c`  
		Last Modified: Thu, 13 Nov 2025 23:21:20 GMT  
		Size: 775.3 KB (775261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bddf14370715a56a3aeb65502e4132014e36569bf351485aa6972603a173b6d`  
		Last Modified: Thu, 13 Nov 2025 23:21:20 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f6459efd9e960692184ac976082588996fcec3c815f59feb2bf4a826beab9c`  
		Last Modified: Fri, 14 Nov 2025 03:34:22 GMT  
		Size: 302.1 MB (302125095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8f7ac4a0deb27048457f312de3d0ecec88ee385f051a3ecc4700344c866b25`  
		Last Modified: Thu, 13 Nov 2025 23:21:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe5f7cd38d3e3724644f40b8c1b47a83e846a86ba19a23d808dc5ace412aa8`  
		Last Modified: Thu, 13 Nov 2025 23:21:21 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5367902f12e70f6927a17008fa5ccc6dcca1c61cbe3313fdba372aea0ff64a99`  
		Last Modified: Thu, 13 Nov 2025 23:21:21 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415053cabd51f3a6864e677354d0400de377a413f66674d6cddc1dd27df92d6`  
		Last Modified: Thu, 13 Nov 2025 23:21:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7952a35e74e9b576be97bac87ff8b63a83f35c020f634736c496a47374160d26`  
		Last Modified: Thu, 13 Nov 2025 23:21:21 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a36c4a6c74e0360f5d28c8f12928bfa3621d618ebe02840a808dacffaf8695`  
		Last Modified: Thu, 13 Nov 2025 23:21:22 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:fd590ffbf3339c0ebabbbd6f47862c3fd990a7469104d87ced9f1dfcdec3b39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c926dc5c11e582e4754f0bb282bb0cd9720ba4c7682ca5216b01580e5b8380`

```dockerfile
```

-	Layers:
	-	`sha256:f952ecd9c1b6027b15b17480992e3c912be1876aac4c47121d6b7b9f7b848348`  
		Last Modified: Fri, 14 Nov 2025 03:34:02 GMT  
		Size: 37.4 KB (37382 bytes)  
		MIME: application/vnd.in-toto+json
