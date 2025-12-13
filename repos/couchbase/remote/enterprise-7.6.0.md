## `couchbase:enterprise-7.6.0`

```console
$ docker pull couchbase@sha256:6e0d044f51cdcdecb90e1ae09c6810da849826af9dc56ee6630bdebe10006a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:05ef64f8d0abc9324847292df73887f083c7f56e50d283528af92b0a36a3c18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.8 MB (759814987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bfb8c3c215512abf773467b813288d6a6e889c4d29ff8266bdd521a3a9f1376`
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
# Thu, 13 Nov 2025 23:15:40 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 13 Nov 2025 23:15:40 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 13 Nov 2025 23:15:40 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Thu, 13 Nov 2025 23:15:40 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 13 Nov 2025 23:15:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 13 Nov 2025 23:15:40 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 13 Nov 2025 23:16:48 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 13 Nov 2025 23:16:48 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 13 Nov 2025 23:16:48 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 13 Nov 2025 23:16:48 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 13 Nov 2025 23:16:48 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:16:48 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 13 Nov 2025 23:16:49 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 13 Nov 2025 23:16:49 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:16:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:16:49 GMT
CMD ["couchbase-server"]
# Thu, 13 Nov 2025 23:16:49 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 13 Nov 2025 23:16:49 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da87ad361d1da7fce10433add475b05135b5bf327e7540e74444cf7def222a68`  
		Last Modified: Thu, 13 Nov 2025 23:18:05 GMT  
		Size: 39.3 MB (39299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742d3c6b54942dfd8f06d042436101c472866e3f4c576630b1d8b862664441de`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 926.8 KB (926818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9766a8e1a7cf887f36a3dcf41b635fc00db5b18dc5dd3f3e95255ec8453a2`  
		Last Modified: Thu, 13 Nov 2025 23:18:04 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0358542210335966e63887bb1e2793737918ee4f3b08db0dc8737b5840c840e4`  
		Last Modified: Fri, 14 Nov 2025 03:33:24 GMT  
		Size: 690.0 MB (690047136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73f75b1848a293b5d941f3e5a6902058f01d2ccf386cba2fc8a4a2a6658aac6`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf40c001658c3722a17eabbda9eb07f3d619e74e0f01e5e96427547214ee206`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254a9aee5fbb859f6d194413387372cc518339fa6c4927879291d0c03a0f533`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a52905f4e0a30a96b34143b31f8871bc92e91e1749570b0428ec43a6d29b8e`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86ad3e2b00012948633095fad18854423d3060637a2647e502bc8a7c27c6e33`  
		Last Modified: Thu, 13 Nov 2025 23:18:02 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523be17380cdcf53a85f4b0e76146cb1b37d63c1391e80c79d9f1ac5a142e9c6`  
		Last Modified: Thu, 13 Nov 2025 23:17:18 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:65f6d8d4ea1015543d184c18feeb1f8839f89cc468ecf3e12e40621fcac474e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1f8a5bd921255132b99d9fdff3e4cf29fac5e83d90bcd97bfc1e9ccc03ab3a`

```dockerfile
```

-	Layers:
	-	`sha256:07ab2309d91e3e38d961f85f47e09fd761c17dfc7c3bb7275ecef3cff7409c7c`  
		Last Modified: Fri, 14 Nov 2025 03:32:38 GMT  
		Size: 37.5 KB (37522 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:f95d2fb5f9d96ab106231becb04eaa84818bcfa7267c66e5c5e532ca0dad94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.9 MB (731944819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d4a1fe0590e1e78b0e8961a1abda7b7f1fbc231552401dc69e7e8c3ba69d51`
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
# Thu, 13 Nov 2025 23:16:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 13 Nov 2025 23:16:37 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 13 Nov 2025 23:16:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Nov 2025 23:16:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 13 Nov 2025 23:17:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 13 Nov 2025 23:17:01 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 13 Nov 2025 23:17:01 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Thu, 13 Nov 2025 23:17:01 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 13 Nov 2025 23:17:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 13 Nov 2025 23:17:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 13 Nov 2025 23:18:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 13 Nov 2025 23:18:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 13 Nov 2025 23:18:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 13 Nov 2025 23:18:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 13 Nov 2025 23:18:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:18:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 13 Nov 2025 23:18:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 13 Nov 2025 23:18:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:18:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:18:02 GMT
CMD ["couchbase-server"]
# Thu, 13 Nov 2025 23:18:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 13 Nov 2025 23:18:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8142ffd362e6c263641143a727ba86a4d2f7715ef10e07ec24bfd95cb0ef4b`  
		Last Modified: Thu, 13 Nov 2025 23:19:17 GMT  
		Size: 38.9 MB (38872279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f26e38c540609a440a0de253d00d17a4c913c062b8bdcba389ae7d89c14a8`  
		Last Modified: Thu, 13 Nov 2025 23:19:12 GMT  
		Size: 775.2 KB (775215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430cd7555e9489edd3ceb9e1fe1b678e06cb7f776450315803339eb5d04795cf`  
		Last Modified: Thu, 13 Nov 2025 23:19:12 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5572ffd267b9cf3590244f49d9bf85440020184f7ac6e871b70a1bba94e78c`  
		Last Modified: Fri, 14 Nov 2025 03:33:20 GMT  
		Size: 664.9 MB (664908269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52c955d75520e3259ba491d99f3af465fb31efe511635eec132db15bc4fed02`  
		Last Modified: Thu, 13 Nov 2025 23:19:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0c46e98a00921df9ebcf0b0fbad7de431383149f1af20104c12a2f5fa74aab`  
		Last Modified: Thu, 13 Nov 2025 23:19:12 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dab9a5dd76266b667a9b0d5b30757f5ce6982c4404b15c1b327c138977838bd`  
		Last Modified: Thu, 13 Nov 2025 23:19:12 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9758e6563f2f65fa4a3c8500de886e528d5bb551fccaa6321473eae841462c02`  
		Last Modified: Thu, 13 Nov 2025 23:19:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0799e46b83f08aedd09c67e774c5ce66f5ecf1834a4d91b5dbf956a441840ed1`  
		Last Modified: Thu, 13 Nov 2025 23:19:12 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483eda1f028ce15f60173ac976826d32558ea860c3f03fbb3456675cedc22d4b`  
		Last Modified: Thu, 13 Nov 2025 23:19:12 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:c1036f2ced78fa630507e12c2b78da9d7a7281ceeb8c58df6fd9af604b4164bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5f0ea37910eb1af690923bc7790acc6a225e3bfab4ff3136702f9f9dac1253`

```dockerfile
```

-	Layers:
	-	`sha256:c78ec2dee609d83aa231467f216a08decb9bc586fa250214e3ab59fa312749d7`  
		Last Modified: Fri, 14 Nov 2025 03:32:41 GMT  
		Size: 37.7 KB (37707 bytes)  
		MIME: application/vnd.in-toto+json
