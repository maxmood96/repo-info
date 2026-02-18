## `couchbase:enterprise-7.6.10`

```console
$ docker pull couchbase@sha256:d3d68b611467f08260e66e6042037684aa58d3e91e43d87f762f6da904a5011d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.10` - linux; amd64

```console
$ docker pull couchbase@sha256:942cade86e9e694404f25cb8232a7de1109f631dc7b375e7d32c43aba755669d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835130907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ac379ae29b4a1851c42793fe015b81e96ed18db0e9a59420c910661964ae4c`
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
# Tue, 17 Feb 2026 21:47:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 21:47:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 21:47:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 21:47:54 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 21:48:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 21:48:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10
# Tue, 17 Feb 2026 21:48:28 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 21:48:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 21:48:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 21:48:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 17 Feb 2026 21:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=680d6833172db7691aa0f9562aa50e044214f97cd8a785b410e828a840ce38bc            ;;          'amd64')            CB_SHA256=80938b3c86eb4cf412d9eb80b6494d96d32ce90555dc8536e0fb44a884f453ef            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 21:48:54 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 21:48:54 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 21:48:54 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 21:48:54 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:48:54 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 21:48:54 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 21:48:54 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 21:48:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:48:54 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 21:48:54 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 21:48:54 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3618dd036c02434a0c1c22af9bdbdcae177c3c88fe4a30ef1e3ee1a8dca98e8`  
		Last Modified: Tue, 17 Feb 2026 21:49:57 GMT  
		Size: 43.8 MB (43815795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149e101c2f9baa7177871514cdb7ff45d8eeaa0f17d496d03337fa7af55e9224`  
		Last Modified: Tue, 17 Feb 2026 21:49:54 GMT  
		Size: 2.0 MB (1995322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cef50933f43cabdb39c7aa422024027a8f035aa8a84fa85ee14dbd182145c`  
		Last Modified: Tue, 17 Feb 2026 21:49:54 GMT  
		Size: 3.7 KB (3719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48948dd12ffb4007c4da32990380986151a76666ff2490a61f6ed87b3876611c`  
		Last Modified: Tue, 17 Feb 2026 21:50:14 GMT  
		Size: 759.6 MB (759585193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0ea22fdd183810cd79edd4e2e3f55750d0e5c6624dd269e1126baa813c681b`  
		Last Modified: Tue, 17 Feb 2026 21:49:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99200cf94b86c4f1f85c0466acb39d5be86ed74edb1686664941fb7b1437e4a0`  
		Last Modified: Tue, 17 Feb 2026 21:49:56 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ce9435271cd8adda5b7879d946f1e161be0366484da1a852a69b1e57e95478`  
		Last Modified: Tue, 17 Feb 2026 21:49:57 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3ba663ce51025af3ccdda9dba051bb0755fab93f47427a99af7623bfc6e56d`  
		Last Modified: Tue, 17 Feb 2026 21:49:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f519bba12ea36a7c8acf5dcfd709aed0897fcd4f003ed11454e2ac348d5fbb66`  
		Last Modified: Tue, 17 Feb 2026 21:49:59 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd281888e0740fd907d7fe0d9cb1dd55334baceefcf114ce51484533a3b5c64`  
		Last Modified: Tue, 17 Feb 2026 21:49:59 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.10` - unknown; unknown

```console
$ docker pull couchbase@sha256:add61c3c9e3dc7b5053927ee1800e013aaa95d43dd8a4adf4c3c2bba9175e716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda9506d7d34b480439c790be203c9022870634baf4e70f3e19a2aca79620e4b`

```dockerfile
```

-	Layers:
	-	`sha256:151f9eb33504b018decc549ff5f91f1c974908025ce85f602a1a68ced59a0950`  
		Last Modified: Tue, 17 Feb 2026 21:49:54 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.10` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:6446a208089eeefcfe0bca3220028822632585b9f9f0671961574e0488257185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **797.9 MB (797891043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5037460284000bad37db30c2cde51d20a04db3d558b5ba8dfca1f8429dae0dd`
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
# Tue, 17 Feb 2026 21:47:47 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Feb 2026 21:47:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Feb 2026 21:47:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Feb 2026 21:47:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Feb 2026 21:48:19 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Feb 2026 21:48:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10
# Tue, 17 Feb 2026 21:48:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb
# Tue, 17 Feb 2026 21:48:19 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Feb 2026 21:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Feb 2026 21:48:19 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=680d6833172db7691aa0f9562aa50e044214f97cd8a785b410e828a840ce38bc            ;;          'amd64')            CB_SHA256=80938b3c86eb4cf412d9eb80b6494d96d32ce90555dc8536e0fb44a884f453ef            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:48:47 GMT
CMD ["couchbase-server"]
# Tue, 17 Feb 2026 21:48:47 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Feb 2026 21:48:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec6ac0f7c8787d1822a37ca8102a36d7cb4dfa3a0b3e9f0199319ba79fffdb1`  
		Last Modified: Tue, 17 Feb 2026 21:49:40 GMT  
		Size: 43.6 MB (43631349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dee88b8c96bd69e74f2201923a03752fe8db8107237f660850195135c94c6a`  
		Last Modified: Tue, 17 Feb 2026 21:49:38 GMT  
		Size: 1.8 MB (1832577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32894227a54388222661528981174ee6c595dd303f1f54db8f0cb37263f1ef5`  
		Last Modified: Tue, 17 Feb 2026 21:49:38 GMT  
		Size: 3.7 KB (3721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a330280881987ea5e84dd28dc12a02199247271be0a5f7924e862e17bd2d15e`  
		Last Modified: Tue, 17 Feb 2026 21:49:51 GMT  
		Size: 723.6 MB (723555013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b041e2bcf6a1e70faf4a5346676438ef8bfac014b68746c78f7731e12e1d76a`  
		Last Modified: Tue, 17 Feb 2026 21:49:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcc070bfceec40c98995248d3a14ccf6530cd5da2a92f43e8a6603d8bbbb471`  
		Last Modified: Tue, 17 Feb 2026 21:49:39 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac068bc0669a90e9a72647efe375efbf45499579f345767f83d17cdd5c33e27`  
		Last Modified: Tue, 17 Feb 2026 21:49:40 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1a0f54f17968a9c010553d5f52f2674f1323c058f92605b9ffc2e4e73e1b22`  
		Last Modified: Tue, 17 Feb 2026 21:49:40 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c670cf32b25ba6fff4b2515db1e8563976cfbe4ccccf5bcc75a2011a9d3b6be`  
		Last Modified: Tue, 17 Feb 2026 21:49:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9516ea8f92f685ed1bcbf0ca1cd227c933c036801ea3cd0a52b77ffd04fe2d25`  
		Last Modified: Tue, 17 Feb 2026 21:49:42 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.10` - unknown; unknown

```console
$ docker pull couchbase@sha256:6afd86df1575fdca35a9fb9384d38017ce8875c4260535c492b06eabcd8173f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de99eccd51d7b7eeeb64a62abe174580a3f3373d39050e8901c9654ebc6613c`

```dockerfile
```

-	Layers:
	-	`sha256:d130ff8df890c48efde61acd56aa40f9a10bd5098f37ddfe9f2ccffd41f1e7ee`  
		Last Modified: Tue, 17 Feb 2026 21:49:38 GMT  
		Size: 37.7 KB (37738 bytes)  
		MIME: application/vnd.in-toto+json
