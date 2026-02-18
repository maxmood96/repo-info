## `couchbase:enterprise-7.2.7`

```console
$ docker pull couchbase@sha256:e691441db79797a4144e02a04e7dcd719e8363e91e5ee0fc4937d8bf3243785a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.7` - linux; amd64

```console
$ docker pull couchbase@sha256:c60556289d8b00edeae9d24e7c7cb0014da0955d89772ce7ef50609e6f4b04a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.7 MB (699744821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a335e2458d3b9c5d3503c6044548cf6b3e320dc84e061198f87f8aef971790`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:16:33 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 20:16:33 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 20:16:33 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 20:16:33 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 20:17:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 20:17:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7
# Tue, 17 Feb 2026 20:17:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 20:17:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 20:17:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 20:17:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 17 Feb 2026 20:17:33 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=00115e7e10447a1f2e16aedad43cc33205a30e546e0c881e6dd8703bf8b6acf9            ;;          'amd64')            CB_SHA256=40e45a65a78bf5c9bea0f0d16a1c2e3aab3704aaadd41dccc2d8db2308f30fcd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 20:17:33 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 20:17:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 20:17:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 20:17:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:17:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 20:17:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 20:17:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:17:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:17:34 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 20:17:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 20:17:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fa0f9382736531623f29979c0a87c496c6effef4d2631aa326eba2d2ef3557`  
		Last Modified: Tue, 17 Feb 2026 20:18:18 GMT  
		Size: 43.8 MB (43815577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed597b80acfc0afadec99b187a6c6c892db847ec59a06781e3875d335989c009`  
		Last Modified: Tue, 17 Feb 2026 20:18:17 GMT  
		Size: 2.0 MB (1995317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611ff4bd8b327950b359c11fbc52da54d169c24e066f44179f851d3b6939a02f`  
		Last Modified: Tue, 17 Feb 2026 20:18:16 GMT  
		Size: 3.7 KB (3721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fea87e2a57f0250c9a476544b05bb8dc9eb944ee5c0de157c25b50de9b5dac`  
		Last Modified: Tue, 17 Feb 2026 20:18:28 GMT  
		Size: 624.2 MB (624199405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b0cd48c84ea68371c48a740166e53ff5b460c9ef8b16488454042996d72494`  
		Last Modified: Tue, 17 Feb 2026 20:18:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42daa46a7fc9f22c7e483c1c0497d2dd49288f8d30758f5d58816e192aaf6640`  
		Last Modified: Tue, 17 Feb 2026 20:18:18 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61dd5c84f2a3f89b4cbad60c2b1a779dc31b8332954c0cbc50ba75da26731fd`  
		Last Modified: Tue, 17 Feb 2026 20:18:19 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38c28847c721a006a6f23ec3f4ee00ee2f241e5f61dac6a0af790c6269c54c1`  
		Last Modified: Tue, 17 Feb 2026 20:18:19 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f487b8eb1795c63044d38c88e4ee8f31aa834cda3bde6e78837b333a88a223`  
		Last Modified: Tue, 17 Feb 2026 20:18:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e34105c06a50ab251b31955b40efb57e3b98ea8f32980d7ef6f2bc7dce30921`  
		Last Modified: Tue, 17 Feb 2026 20:18:13 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.7` - unknown; unknown

```console
$ docker pull couchbase@sha256:8da02e65b35601526b055f569b0afba320687f3fac8d6ea3f2d31e9bb1a646d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7f25acf5d7ade82fcbc8ecee64fcb86eb0f048765ddf79f81157b0154ea755`

```dockerfile
```

-	Layers:
	-	`sha256:063c88d9030ec8b2d2171b064b93eed7af159bde4a7b7836900f533aedb09f8e`  
		Last Modified: Tue, 17 Feb 2026 20:18:16 GMT  
		Size: 37.5 KB (37531 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.7` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:53e7161d14ef2c2dc283d0a727c5b656dfdc0f6f0c26be2e8d127b96f57d7d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.2 MB (678178423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aadc6f57132bd916b1c745f7cb734bf80691e0c22714157aa3c44fd65b48b0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:15:52 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 20:15:52 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 20:15:52 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 20:15:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 20:16:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 20:16:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7
# Tue, 17 Feb 2026 20:16:24 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 20:16:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 20:16:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 20:16:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 17 Feb 2026 20:16:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=00115e7e10447a1f2e16aedad43cc33205a30e546e0c881e6dd8703bf8b6acf9            ;;          'amd64')            CB_SHA256=40e45a65a78bf5c9bea0f0d16a1c2e3aab3704aaadd41dccc2d8db2308f30fcd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 20:16:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 20:16:52 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 20:16:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 20:16:52 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:16:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 20:16:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 20:16:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:16:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:16:53 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 20:16:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 20:16:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e822fe618dafd4eadf529f22e489c68b622839e99246771af367f3003315e13`  
		Last Modified: Tue, 17 Feb 2026 20:17:37 GMT  
		Size: 43.6 MB (43630833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bc83a6bd238a0750bf679afc4b67b7a68dc96f88079e54bddc3f338e6995a0`  
		Last Modified: Tue, 17 Feb 2026 20:17:35 GMT  
		Size: 1.8 MB (1832509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60627d615723a7b5a7cb4260a3f499a991b72ba226dcbfb68787d668380e1265`  
		Last Modified: Tue, 17 Feb 2026 20:17:35 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d0b27d655289082e3d0ffffc7b4e0683dd66fc12af17ffed31f104bb1841de`  
		Last Modified: Tue, 17 Feb 2026 20:17:47 GMT  
		Size: 603.8 MB (603843045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5df04f9193965779229115bfa02a32afe4c6de760bc038dbf5789e5b87f549`  
		Last Modified: Tue, 17 Feb 2026 20:17:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b68e0c9af40591a15dbf15a90bde569d55df35a7a7fdc3d3854491463c6850`  
		Last Modified: Tue, 17 Feb 2026 20:17:36 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475bee1f9e0717781c78be9ed1dec504b1ba74378ce32af8594d3db0e2e2d8b4`  
		Last Modified: Tue, 17 Feb 2026 20:17:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88577e67d7e185c7d26bbfb2e5d464131a62b769fedaddcaf9aa4d524fcdbbbf`  
		Last Modified: Tue, 17 Feb 2026 20:17:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae550d2bd4b655e607c138768ea1336502d723e1ebe39f95b68dbb5d505d4350`  
		Last Modified: Tue, 17 Feb 2026 20:17:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a78894dd30bd850f6aa5c1c292c9afb658697ea6b86b2c6768e24936f27e86`  
		Last Modified: Tue, 17 Feb 2026 20:17:38 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.7` - unknown; unknown

```console
$ docker pull couchbase@sha256:4f811ad12095ea6c8875cb3787d52902c26a0a4341e4e07c4314b0f45fde22f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b3ce2ea39f6ebedadbe90e2e46f0b205680461cc5ac06a79db26baf4f11586`

```dockerfile
```

-	Layers:
	-	`sha256:113accbeba11f4934b34548d8ccf241e1c733dad86d040e0790a8d532170716c`  
		Last Modified: Tue, 17 Feb 2026 20:17:35 GMT  
		Size: 37.7 KB (37717 bytes)  
		MIME: application/vnd.in-toto+json
