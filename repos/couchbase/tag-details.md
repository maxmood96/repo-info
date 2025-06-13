<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:7.2.0`](#couchbase720)
-	[`couchbase:7.2.2`](#couchbase722)
-	[`couchbase:7.2.3`](#couchbase723)
-	[`couchbase:7.2.4`](#couchbase724)
-	[`couchbase:7.2.5`](#couchbase725)
-	[`couchbase:7.2.6`](#couchbase726)
-	[`couchbase:7.2.7`](#couchbase727)
-	[`couchbase:7.6.0`](#couchbase760)
-	[`couchbase:7.6.1`](#couchbase761)
-	[`couchbase:7.6.2`](#couchbase762)
-	[`couchbase:7.6.3`](#couchbase763)
-	[`couchbase:7.6.4`](#couchbase764)
-	[`couchbase:7.6.5`](#couchbase765)
-	[`couchbase:7.6.6`](#couchbase766)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-7.2.0`](#couchbasecommunity-720)
-	[`couchbase:community-7.2.2`](#couchbasecommunity-722)
-	[`couchbase:community-7.2.4`](#couchbasecommunity-724)
-	[`couchbase:community-7.6.0`](#couchbasecommunity-760)
-	[`couchbase:community-7.6.1`](#couchbasecommunity-761)
-	[`couchbase:community-7.6.2`](#couchbasecommunity-762)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-7.2.0`](#couchbaseenterprise-720)
-	[`couchbase:enterprise-7.2.2`](#couchbaseenterprise-722)
-	[`couchbase:enterprise-7.2.3`](#couchbaseenterprise-723)
-	[`couchbase:enterprise-7.2.4`](#couchbaseenterprise-724)
-	[`couchbase:enterprise-7.2.5`](#couchbaseenterprise-725)
-	[`couchbase:enterprise-7.2.6`](#couchbaseenterprise-726)
-	[`couchbase:enterprise-7.2.7`](#couchbaseenterprise-727)
-	[`couchbase:enterprise-7.6.0`](#couchbaseenterprise-760)
-	[`couchbase:enterprise-7.6.1`](#couchbaseenterprise-761)
-	[`couchbase:enterprise-7.6.2`](#couchbaseenterprise-762)
-	[`couchbase:enterprise-7.6.3`](#couchbaseenterprise-763)
-	[`couchbase:enterprise-7.6.4`](#couchbaseenterprise-764)
-	[`couchbase:enterprise-7.6.5`](#couchbaseenterprise-765)
-	[`couchbase:enterprise-7.6.6`](#couchbaseenterprise-766)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:7.2.0`

```console
$ docker pull couchbase@sha256:5903fbd69888f93c4e30651d4cdf027e58eb6a14e2e339c32f89ccfab2d67e10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:31f88212bceb31fad149a4ee4054bd7a6ffdedb50a839290a6633e15c7ae3b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.8 MB (698757280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50849322570fae9771a13f147ca945000fe7b3b38304065fe2049f293dd1eb57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:23:17 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:23:17 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:23:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=b44a4d8e577613ad027dbac9830e6123deb7bda22facefe687d6b6e98c86ac66            ;;          'amd64')            CB_SHA256=2fd31b46a6df5ed9c85d3a6cadfb0214e3f928c14ff0b03e6a24652700128328            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:23:17 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:23:17 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:23:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc07d2a16bf1e0137d7d77f6eb59d22890f7e9dcd4bdbd1ec051c27b67aa0d`  
		Last Modified: Thu, 12 Jun 2025 22:54:25 GMT  
		Size: 39.7 MB (39663052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399f8bb9e64b1b0321b2f53a1db86a12287c0bef4ba447710cecd24286701c16`  
		Last Modified: Thu, 12 Jun 2025 22:54:23 GMT  
		Size: 926.7 KB (926735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0dc39fbb9a867beade04f06e2cc150de4bbbbb0b2844407479f8f2ed1ca79e`  
		Last Modified: Thu, 12 Jun 2025 22:54:23 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dd0ac1184b561d815a9953efc83829d67d584575af81793890e011acdcdf72`  
		Last Modified: Thu, 12 Jun 2025 23:31:50 GMT  
		Size: 628.6 MB (628629308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd4c2dce965d4648509cf2e03d3a9b30c33e79d40e8210eaaf08250123a63da`  
		Last Modified: Thu, 12 Jun 2025 22:54:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3056f8515988a338339951438cbd7ae7c24261d04eb6fa5e096ac9ddfc5f19`  
		Last Modified: Thu, 12 Jun 2025 22:54:23 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83519ace6d1861c8ad3ee0fe6c437da8084fbe5e0d842c71fab653a16ad903a4`  
		Last Modified: Thu, 12 Jun 2025 22:54:24 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02bed1bcd48eb6123ffbf42969b31630aeb92a29270dd06dd40185bf64209f3`  
		Last Modified: Thu, 12 Jun 2025 22:54:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de802a1c967cd99c41cd12b7ce383dc6e74e7c727397e4bf6e767a030373ac0`  
		Last Modified: Thu, 12 Jun 2025 22:54:24 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9add43c4fae696f20ad685bd9ffc3306cbfcab18cd737b4aa91db3f2b37fce`  
		Last Modified: Thu, 12 Jun 2025 22:53:40 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:e0871753bc0f82b84ce35c0fe3d670f4384a1f8c6304433c772b33a952abbff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e44397b7ab2d39b3a87471f4869554b5012ec813de86b35342b1ed12f4804ef`

```dockerfile
```

-	Layers:
	-	`sha256:d73250c7c6746e800b969548d9c9ec657458595d975011eabfb1a77f0a38316d`  
		Last Modified: Thu, 12 Jun 2025 23:31:19 GMT  
		Size: 37.6 KB (37564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:19e4731c7fc0bf9b784e5649eef54d7c7627111bf22d2a2d68875f116c22f2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.6 MB (670589921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9b8b4d060e236c19415d44b751093d96f1ab4feb1d6f4eab3cf3fa3de1aedf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:23:17 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:23:17 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:23:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=b44a4d8e577613ad027dbac9830e6123deb7bda22facefe687d6b6e98c86ac66            ;;          'amd64')            CB_SHA256=2fd31b46a6df5ed9c85d3a6cadfb0214e3f928c14ff0b03e6a24652700128328            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:23:17 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:23:17 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:23:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e6a2429701c4282f51b3d41383366f0e0e9478774dcf1548795cd1503d09c`  
		Last Modified: Fri, 13 Jun 2025 00:37:49 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a4284e8f893f30000e9945d7f0f12f3bf73edf168be902b77483663725f87a`  
		Last Modified: Fri, 13 Jun 2025 02:31:55 GMT  
		Size: 603.3 MB (603251419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202962f366f1c09efd638bde89504c0a186539fc545d4aad32bd3c0ca26e682d`  
		Last Modified: Fri, 13 Jun 2025 00:37:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ddf16aec84e5a570869254dd33a78289ecabe8147264fa5f84572ef58a5275`  
		Last Modified: Fri, 13 Jun 2025 00:37:49 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf927e6bb267bd0019abcc802c82853fac854a0a65b3758f2c68804fa5ff38`  
		Last Modified: Fri, 13 Jun 2025 00:37:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd4c8ca44a9f0a4049875b9f507704670e6c85ebf6393b3826e43205cfd9750`  
		Last Modified: Fri, 13 Jun 2025 00:37:51 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32191ea4d2ab2d929c82de5a66ac0a34a945835d9caed7faf11c49a65f04876`  
		Last Modified: Fri, 13 Jun 2025 00:37:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d886b2fe8965d7f67d3b2bd1e2f1f0c55d56878d0c45fcb93b08fc9b9f0bbb0`  
		Last Modified: Fri, 13 Jun 2025 00:37:51 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:9bca4527c87a69dab17ffb14a0fd23fd6146dd7aaeaeefe622c0a5637ca4a581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f1116659811c1e9960737da2b9c38c648587643d8ae3b0546eceacbec58541`

```dockerfile
```

-	Layers:
	-	`sha256:d93c696fa04f4fa167fddbdeb06bbcac20dab59dd10091edc8b3f2cb5929ea7a`  
		Last Modified: Fri, 13 Jun 2025 02:31:20 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.2.2`

```console
$ docker pull couchbase@sha256:8fa3a7d527f44c905cf8814cd979cc72ddbc00af175e1c03f4cf24cecbc35916
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:a19ec58565546640ce8da4ac8b0e0497d40eaf4ecb5b88bc9d05633bc4d6989c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.9 MB (703930557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4138389afc9331760e16d223619951f7ee9e35b71c2908426c0c75c61183233c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:32:06 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:32:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:32:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:32:06 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:32:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:32:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f107907d53e2361344dfc4357ed319d478ba4b6f9887ee23afba17e518916eed`  
		Last Modified: Thu, 12 Jun 2025 22:54:44 GMT  
		Size: 39.7 MB (39662068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabaa524eb5ff279a762749c414210ccc99844adc93606e3c015527962f0ac10`  
		Last Modified: Thu, 12 Jun 2025 22:54:42 GMT  
		Size: 926.7 KB (926688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7c0fb24f91c6cc3996a50c59d93f19a70ba469f8880e388fa76bc1f39f859`  
		Last Modified: Thu, 12 Jun 2025 22:54:42 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ba7cab0bd2d2e1c28b5ce8a2505a30d64515b1d87bd6ba4f7fe0bcba74d3ef`  
		Last Modified: Thu, 12 Jun 2025 23:32:30 GMT  
		Size: 633.8 MB (633803620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0a628e0db4d8c44f66fd8747a09914ffe9d6cb37ed6e56d9239090edae5c52`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bed21221646d551c31846945d48cb58743f3bb6eee0c86479df6c7ed90c280`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80478c4edacff4457e1dd268637ef6815d811ef0758eda8036ff2d4e798f6839`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec7c0dfcc59e9a3413516b8adfb4b0ff66c88d423be768c31104bee25efbbf0`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843f0de77d8204f29306599e736b20ed821768ba72baf61618faf7df519008f6`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fc1d36fa5094a22cf3d3ba7f00b59dd9a7a347b4d4bf9ce9f1e023ef56592a`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:bff2c164c8649a3eb3302805491042c3fff28f9e85ccb626d72107457077fc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63800db6e89a8e49a61f95f5c865d8200ad220f377af01ac3248c614af1553a`

```dockerfile
```

-	Layers:
	-	`sha256:3f06e294a709aca3d5765f412553f9225c8c17dc5225dc7bf12fd0aa15b23a3f`  
		Last Modified: Thu, 12 Jun 2025 23:31:24 GMT  
		Size: 37.6 KB (37564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:69cb59a0585d6fc61cc8432c6575bcb8045615d2079a557c233757a55ab0bfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.2 MB (674187907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e032e0f3158bb51e95e910074122a2cb9e38a330302b3b6c539d4d42839d7901`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:32:06 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:32:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:32:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:32:06 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:32:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:32:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880c8d6ebca9e0e7c4d467d832f4b1d938f72516eb584d074f42f0b8f45680f4`  
		Last Modified: Fri, 13 Jun 2025 00:34:32 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc7ee46123cebee8a6bb90ca9c58c0de87fd6f25263de693ad44cf17ef1f3ba`  
		Last Modified: Fri, 13 Jun 2025 02:31:46 GMT  
		Size: 606.8 MB (606849403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64658e2dc30c74c06bbe96a5c5fd241d93456d8b726c936b7f9e7ca6c7b8f09`  
		Last Modified: Fri, 13 Jun 2025 00:34:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7bc1f28314c75409c3d28bc791fb6cc221ddbd1250831cffe947fc4d364a43`  
		Last Modified: Fri, 13 Jun 2025 00:34:33 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f6ebe51b1da8caec5732f4de23ebda30d137f9967d5c3feed8e01413b7a1a0`  
		Last Modified: Fri, 13 Jun 2025 00:34:33 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0658dbcc92c8ac5e3947cd8c7378a559753835ceda224080c04ede07898d61e2`  
		Last Modified: Fri, 13 Jun 2025 00:34:34 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c1e02c7d88ca7164d6154a6ce2ac4ce4f394fc41cd899189494b618c26b08a`  
		Last Modified: Fri, 13 Jun 2025 00:34:34 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613317a29d35bbf6faa4a5f65cc11fc68bbf95d194b15c4bd1993dc022169d95`  
		Last Modified: Fri, 13 Jun 2025 00:34:34 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:009649c3d3b88b6065017755213d92b937fbcd28937a202828f0653ea7a47c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39e434665044faa844699cf8bc9742608f68068db63844fb5c8b4743121426f`

```dockerfile
```

-	Layers:
	-	`sha256:b26f3122fba0af356d59af6cd73e4225c4a537cafa5729c03a10175e013d1535`  
		Last Modified: Fri, 13 Jun 2025 02:31:25 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.2.3`

```console
$ docker pull couchbase@sha256:550275517f9d321fcb70440250be1fb2a71ba7658657259ec49a7f4f0cdec43c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.2.3` - linux; amd64

```console
$ docker pull couchbase@sha256:b9c4574fd7e2dc46d0c7cd70f79c468215b4ede7f9d3c9dee6640d76cbe04e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.1 MB (705089528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fb79c0ed302f92da770cfc314d25e048162c2d369834c30ac23ba3ba98c9a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:43:25 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:43:25 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:43:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:43:25 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:43:25 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:43:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada5f9d92ce31847d28cc65155b4d53cd20e2f0feb5a9d5e50c19c8ea9f04de5`  
		Last Modified: Thu, 12 Jun 2025 22:54:18 GMT  
		Size: 39.7 MB (39662267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f314f9540cb794c1c6d458e1c5f696fe026d2d715097c190b30e7656707201`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 926.7 KB (926685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054899b4bd44e21e80a0d93a198b3bcacf9adf41b06c62539f375563dd1f5bb0`  
		Last Modified: Thu, 12 Jun 2025 22:54:15 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f52c53be83b3e824a8be981e1c5c25afe66afcb330385e6e51d05e5f57b0815`  
		Last Modified: Thu, 12 Jun 2025 23:31:52 GMT  
		Size: 635.0 MB (634962399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3c64516be992ab915a2c3d74b9b27bd3249fe30e76b4d6a2799b81b786338`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd47933b20250284cae5e8a1e485588451b695747dfb1dcfc50aecf9955648df`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b75ced0b490b0ca997a028238b3eac14b014f850a60efd2be72f8eecfc03ff9`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35357947bdb507a86a00385bb50c039cb291f15813b89c22aec603cdd030ea4a`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e84b08a01e1e97c41c412010ef812dca02afcb323749f13edaf66bf3dec69`  
		Last Modified: Thu, 12 Jun 2025 22:54:17 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0837de8b7a88598dcb5ba1b9c4fe396fc7f9a57a1ade64fb0c33bcc6af6797`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:7517f8c9972ae7994bcf9c8182617637ecb8d0c77d8374d154126cde2a74dffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7281b0cab61409727f7dbface688f9f01e5bc2dcc2a9ef911b73b58baa9df917`

```dockerfile
```

-	Layers:
	-	`sha256:7f669c94346a931f2e501b4241623e529f92e7d6c0865efee5baa5636a5d5876`  
		Last Modified: Thu, 12 Jun 2025 23:31:29 GMT  
		Size: 37.6 KB (37564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.2.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:835ef4188c9e1cc3cb06b1e65bc042720c185f17dbb75cc2b867bdaddcd0ed65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.3 MB (675253927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ce254586553c6c98f546f193c1626ad9f359c108fc052c57c1ff90da8ee4d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:43:25 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:43:25 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:43:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:43:25 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:43:25 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:43:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be109c36b0e255091c2d780f7db672d5b6fc8fe0f7ab9164e258a5f446a91bcd`  
		Last Modified: Fri, 13 Jun 2025 00:32:48 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e70616205835ea0633debc70736ee3d01a7fe72d43013c46e7811967538780`  
		Last Modified: Fri, 13 Jun 2025 02:31:55 GMT  
		Size: 607.9 MB (607915424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0e08cbe2004368f4d8974246897045bd6d8761c127a063fbeb5f568272a598`  
		Last Modified: Fri, 13 Jun 2025 00:32:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fe7d1528be1bf0b503995df2ab0a8eb29a4cccea314a6dd14744210673e3d8`  
		Last Modified: Fri, 13 Jun 2025 00:32:49 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f146aceda8052a9f8409d6374ed514f1d53fc46448e8db4632d64f11df9083f9`  
		Last Modified: Fri, 13 Jun 2025 00:32:49 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3feab1251e318361368d25badd5dc0cad00bfecccaa6d0c046ffb3f0172b`  
		Last Modified: Fri, 13 Jun 2025 00:32:50 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee224b845d5d87f19370b3f0e7ec67a4ab798d5b4ad9b8e41d5e81fe3146013b`  
		Last Modified: Fri, 13 Jun 2025 00:32:50 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7d4a1d12267d591c99b9fa616589b9730f0ec09926bc0eacebf7d172040b42`  
		Last Modified: Fri, 13 Jun 2025 00:32:50 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:c30d945c5f67530a7627ed709594297971de2fa94f6962224c2a5296bc94de43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de65943784d2b98ee26854777d127dffec7fee01c275f2db70cd304c0a6c0141`

```dockerfile
```

-	Layers:
	-	`sha256:921f03453f34a3761df8e54f39847677821e4cb28ccbd7d4129675842ba8f277`  
		Last Modified: Fri, 13 Jun 2025 02:31:30 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.2.4`

```console
$ docker pull couchbase@sha256:774bd2b4bf41c702c65f084f4f670e97a4b781315051687e575b0ab29f8001a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:f7f16ac118809c4f8a10b20345a8caa4a052c26326b5ff8abd882c8abca2e46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.8 MB (675793697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776a783f098ead05ee73fdcc18d992e66d5b626933ec029c4afaed371409d74f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:50:29 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:50:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:50:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c675d9e2a355cca833c9c12f85585e92a4d1cd95858d79e958b507f9ba1a4349            ;;          'amd64')            CB_SHA256=0f5edf6c011df25e172ae54c6bbe5f83be6a3c24e4e23b25e77d5079262c30ca            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:50:29 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:50:29 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:50:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f4a1a05bd5e8ab1925e2531c695347c04cc0bed559a2fe2aa59de644fc21a`  
		Last Modified: Thu, 12 Jun 2025 22:54:21 GMT  
		Size: 39.7 MB (39661582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08ffc457d1e7964b3047bb444141afe1fcf9b17f9b65a23b8355691f5cc717f`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 926.7 KB (926717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807b824192ab90051a1350760e8290d36d293c7929e2340056f8d8d1ede213c0`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4f33dd97ad1a831264c25619854d00b047def12c8a15fe532b4b93a7c13d7f`  
		Last Modified: Thu, 12 Jun 2025 23:32:49 GMT  
		Size: 605.7 MB (605667215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9d628d1fccc94e229852442cbf7b76fc43606526be191d9a30a2b1b2f4e3ad`  
		Last Modified: Thu, 12 Jun 2025 22:54:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec373d2b6db9e083cdc0206e441423a547bfd02603db62a0b405f92fae7b4790`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba056eb399368f8df6abca629cfa9e7c8eb6125b3af12c4592e8a193ca8781b4`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f145641e3cc3822389c3e05dac06116dc5dae92c781a70eb4cce7e330ad410`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d9b5e2fa4b6458fd448b043e779225ebb78095d0758e2a6c1684a9e4d9ba9`  
		Last Modified: Thu, 12 Jun 2025 22:54:21 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0837de8b7a88598dcb5ba1b9c4fe396fc7f9a57a1ade64fb0c33bcc6af6797`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:9a6b939d937491150a341383da6d4f028885a79928a73c3c4af7e2c17ed5cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c1f8b6cbdde81dab7c8fcb898acbf496927dd6922c10776128be7f4393be9a`

```dockerfile
```

-	Layers:
	-	`sha256:76f2699312d87698b3674d6091a7082b24bd3bab904fa82c91076b12f70c91d1`  
		Last Modified: Thu, 12 Jun 2025 23:31:34 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:5792ab3afa35ed4e807c300a3608c4d8550e026e333c70ebbb263400da20231b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.7 MB (649745090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dd259c4a7b6388c3c3ca68e804d50e8e1a217591615407170b715c4a78225b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:50:29 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:50:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:50:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c675d9e2a355cca833c9c12f85585e92a4d1cd95858d79e958b507f9ba1a4349            ;;          'amd64')            CB_SHA256=0f5edf6c011df25e172ae54c6bbe5f83be6a3c24e4e23b25e77d5079262c30ca            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:50:29 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:50:29 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:50:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4280655c3ce47770e575d428dff5ba5cdd53d48c389eb4ba18fe4950c6a404b`  
		Last Modified: Fri, 13 Jun 2025 00:29:43 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a8b0b3dc230785bbef0f2886729f0f68729b71bfe5069c99dde096adf7affc`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 582.4 MB (582406589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97836be91af5aee9698364a4fad3fa9f65fe65d4bd38424913f722fe8a1213ba`  
		Last Modified: Fri, 13 Jun 2025 00:29:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1b9abb614800a250234bfa8ceb39021077c57e3103e19684dedd705ac4680a`  
		Last Modified: Fri, 13 Jun 2025 00:29:43 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fba3cad805715f80566d8b56d1d5f5029be0cc5319ce9c077dbe615f784e06`  
		Last Modified: Fri, 13 Jun 2025 00:29:44 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eb118d2535fa9ab96c9e9970001de0a7df37c2aedee1c930c42dc80c37465f`  
		Last Modified: Fri, 13 Jun 2025 00:29:44 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518d49e34717ea6a7c01c0e9e4e2ebea6ec73a369b84a8e1d29542ca9e142bff`  
		Last Modified: Fri, 13 Jun 2025 00:29:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e92531b82f1c31f3c3b00dfbd685be2b91332f556e268541986c903999a47ac`  
		Last Modified: Fri, 13 Jun 2025 00:29:45 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:1117a0f938cb2f7c92d023f344aefc7d1df75423074fbd23ae62f3c8f3e3ba2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91eac438b40af1b0f4b0215c7586777c2305858a300342389c7c3ec33418dc1`

```dockerfile
```

-	Layers:
	-	`sha256:76fdd5aebb347ec4ab0b42be59fcba0d943574d14fcf334889b5103982707738`  
		Last Modified: Fri, 13 Jun 2025 02:31:36 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.2.5`

```console
$ docker pull couchbase@sha256:d174c71343bbdb954628bec9a74f3e37a2c9198e8b3dc9bad50478030846fc46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.2.5` - linux; amd64

```console
$ docker pull couchbase@sha256:56678afa56e7da69f4cf4d476489f6ebc22a15e519b7c3e4393249db566cc4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678279523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9f675fee53eaf67aead3b22c0d18a97b7ed7e3ac16629537286fe53297e948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:00:36 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:00:36 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:00:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:00:36 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:00:36 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:00:36 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259d186a8bdd83bb89e0d444cb03b56a1e25bf56ed2e496d40195fca06f8bae8`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 39.7 MB (39661916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b258415211893d2d2e0d02a524af2a738b49a7303359fa172238f36f177d4cb`  
		Last Modified: Thu, 12 Jun 2025 22:54:11 GMT  
		Size: 926.7 KB (926716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b4ef514e0271d07ba46219bd0e07151c260af86c0d717e6c5f6c196c46c12`  
		Last Modified: Thu, 12 Jun 2025 22:54:11 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b296622690961c3f744e23d8266f8d62a8c80c107d39997a6f0aa41eb81f2f7f`  
		Last Modified: Thu, 12 Jun 2025 23:32:48 GMT  
		Size: 608.2 MB (608152710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969f38e48ae02d2fe72e25a676365cae707fbb75291516fe090cfa3e8c411e6`  
		Last Modified: Thu, 12 Jun 2025 22:54:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbbdf3feb1c0617158ded53b7fa2aa3574ce4a294dc996fd17d62f3fcbde744`  
		Last Modified: Thu, 12 Jun 2025 22:54:11 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dd91a1307cb8b92c952790b18e9bf4138e9eeaca97a26ead9f3ae47ffd6aba`  
		Last Modified: Thu, 12 Jun 2025 22:54:12 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42c96e2aaf713fa9e532fce9973aee27509f6c51f4d5c0452eb56f148885443`  
		Last Modified: Thu, 12 Jun 2025 22:54:12 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255a8d83296df84ea1e84b47617c0b9bbb41d3ecf32f110e7035a1ee18eb8cd`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c3ae3afe347e85a46598fd71f89156b61f6518b159107365db731dedcf00f`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:803599731311bff99da51b127a742301f6c6bb6b6432d497c8d55ce04b090987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4366bf0a6162c7782a626e3b7ae3f47b7f52bea2c9dcc03931248bfe99a1b8`

```dockerfile
```

-	Layers:
	-	`sha256:6cad51b844d2f9117f9b29cb970a1aa66c20bf8a1de146a302e25ce9a663ca58`  
		Last Modified: Thu, 12 Jun 2025 23:31:37 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.2.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9956f793cc285b892120ffaaef4b0674486986839bc205bfbc9b26e3afc76af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.8 MB (652756203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e996757cf2f5c835b76636ac79ec65b13a23b29d813499b0a6b63f4007ea47a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:00:36 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:00:36 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:00:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:00:36 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:00:36 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:00:36 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d58a1caf4430f01f3389631ea92dce68c0a7af74e66486367affad12ccaa3d`  
		Last Modified: Fri, 13 Jun 2025 02:31:47 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527e3853254046d9e3058ca7cc0d785216e5ef80a2d9520fca1ab6e51cd1ea96`  
		Last Modified: Fri, 13 Jun 2025 02:32:03 GMT  
		Size: 585.4 MB (585417706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bd09b87be592878f22afbd2557b25d8e379bec0f3d8b5439e6c3c6058176da`  
		Last Modified: Fri, 13 Jun 2025 02:31:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024bb0ad9203da930466096a81737cd1f6b41db672a2d1fe5587ec58da33bcb`  
		Last Modified: Fri, 13 Jun 2025 02:31:47 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a796ec98540c8a5c9fe97aa52546d18d70419ba6e3cf59c20f1735c1a81709d`  
		Last Modified: Fri, 13 Jun 2025 02:31:48 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55268ffa42bac369cdb34ebeae96d03e168ea91d1594454b2f31023c3a44ef73`  
		Last Modified: Fri, 13 Jun 2025 02:31:48 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433b82c078a32135e74a6aaf4c5629dc411fd704957480ae1a45023010d9d036`  
		Last Modified: Fri, 13 Jun 2025 02:31:48 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560bd650008423fd05009af2592dfcbe053ee5cd8b375f2d0bb21cd0911399e0`  
		Last Modified: Fri, 13 Jun 2025 02:31:48 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:ecc07ddba6315269ebb5b9da50afa0d25260c1a8ce089a227b6852de6bec50bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a4a65a47a93213b385f5a244f0bab47cc77c75f72efd2b7ea60fe3b596aa63`

```dockerfile
```

-	Layers:
	-	`sha256:4b81e96754f1bc8b1b3d50f95120e8fe6652fb52a08459ec4d0fdd6bd4fba397`  
		Last Modified: Fri, 13 Jun 2025 02:31:40 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.2.6`

```console
$ docker pull couchbase@sha256:3fd8451d44022d9f59ee18ed378ca550d30c292b98ef3571a796d37cc2f592e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.2.6` - linux; amd64

```console
$ docker pull couchbase@sha256:742742c2b9462ff5228bd6b543c73a5228def3131c68084ee3ce57255ca480be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.7 MB (690668356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff663744ea006c54fb586c0520424611bf4d66992aae61c30c96aafe101ed29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:07:10 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:07:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:07:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:07:10 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:07:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:07:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6342502ed45c496fc9a772bf28dce27961b7f3f260815b8c9bc998c905ed0949`  
		Last Modified: Thu, 12 Jun 2025 22:54:37 GMT  
		Size: 44.5 MB (44462513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e119535dc9d9cd9b87bb7f9f480283d921f6e1fd9995f68a8df6b3dae2afdb`  
		Last Modified: Thu, 12 Jun 2025 22:54:32 GMT  
		Size: 877.9 KB (877888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8080ed5fe938e91c6fb2cf13df2c6774d671673dc21f86303370c6826fbfa0`  
		Last Modified: Thu, 12 Jun 2025 22:54:32 GMT  
		Size: 3.7 KB (3729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa01ec3e95beb8d8829a4ca55d4f1686ef293b72d9199314aa9ec1e972c4b1`  
		Last Modified: Thu, 12 Jun 2025 23:32:34 GMT  
		Size: 615.6 MB (615605698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3dc2fd94d56840efabe44416d9d3cd55577edf187a3534a96b66c0b1be9954`  
		Last Modified: Thu, 12 Jun 2025 22:54:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463b5f2c01b7d56a91294b84e569e56c7bc8141e015416fecf9ea580f176884f`  
		Last Modified: Thu, 12 Jun 2025 22:54:33 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fea10eaf0607de29318d5121d71e889e9bdb509e93e78f697e779b8a62ac8`  
		Last Modified: Thu, 12 Jun 2025 22:54:33 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0341c875eca6c4eebc54ca023e7ae23dba967372aaad35d4cd97ade0f30f0b24`  
		Last Modified: Thu, 12 Jun 2025 22:58:09 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76f5055fc3ff068332267dfdcea771ce824827b8ac180e2b1f933eb706360d`  
		Last Modified: Thu, 12 Jun 2025 22:58:14 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9add43c4fae696f20ad685bd9ffc3306cbfcab18cd737b4aa91db3f2b37fce`  
		Last Modified: Thu, 12 Jun 2025 22:53:40 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:9c299b47aca350a282338de4edf9aaf24f5c7b56250aca5fa2c704505db1081f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6421b0be3156000fa4bb38046e52c19cbf71ed14181b771285ed0e77d7e5da`

```dockerfile
```

-	Layers:
	-	`sha256:fdd92a35fd8b2955a09e81f54efb29a1bef36480b164e39b65b7d54e11bacd15`  
		Last Modified: Thu, 12 Jun 2025 23:31:44 GMT  
		Size: 37.6 KB (37563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.2.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:985ad2a08187025ea9197de6243c81a89771141824f14905defd6e2f03e0b957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.3 MB (666288345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f03666a59a56c5d115ab45383c6da0da0c639749c4e61e55491bf48ef7291b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:07:10 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:07:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:07:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:07:10 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:07:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:07:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107df1885da6b3f0d704e6528f98f7fa3c94661b8f92990d84afdcb07a1bc0b`  
		Last Modified: Fri, 13 Jun 2025 00:12:58 GMT  
		Size: 44.3 MB (44276800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc711ea2f9a6417737f414cef7ac703989f3b88829d303e343141988a94d9f`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 765.0 KB (764954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc15ffe6674bf89403fb61246091c14f2e20302789955bb712245f5a24042e7`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 3.7 KB (3727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab95f41f0304173102959b4f235cc5bf12709ba2379afaf549082acd66f6fcd`  
		Last Modified: Fri, 13 Jun 2025 02:32:09 GMT  
		Size: 592.4 MB (592387770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0cbe9d7cf3571e27db243e40d61c2e7ef30ddd94fc428741b9176a61c5278b`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1312fc0ee350d9939d2b925311037ee43918449530d6611dcc6482054bb39db3`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4494771efad92b1a50b90a330adb0bbcf3d4c823f58fcee7e527b88a9df13bb1`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251d1bf68f500d8378177ebabb098f2166cc199528abd0776ddd57d7b38b457b`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9a5adc90956c563c0ba63196c5a7ccc3e528b8e1ce5dacd4d9ca3b9bc6b3d7`  
		Last Modified: Fri, 13 Jun 2025 02:31:57 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e075a806a76ca9b6cdf03fcd5251343c000b62798bcf9080fde2ab478c7d81`  
		Last Modified: Fri, 13 Jun 2025 02:31:57 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:dada07c68a212e50ac190654e1ea53302990f03753c5dbb133a5dd4df9b23d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e51134cb0b31baa48fb289d421680b0ddea0f511945554609d996919eb070a`

```dockerfile
```

-	Layers:
	-	`sha256:f813ad93b40c677407c5ce0c3a52c492c834209d20f0f865c6c750d34b4a125c`  
		Last Modified: Fri, 13 Jun 2025 02:31:44 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.2.7`

```console
$ docker pull couchbase@sha256:49ee943706e38117af05bf4db9d743a02616e9fdd710da5e236d5d3f8ae9f49c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.2.7` - linux; amd64

```console
$ docker pull couchbase@sha256:9ab200319bac14c9d5b401fb6f18c432754a58027bdea17e236c85ee6c61260a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699262059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6049f97f9a10641a71c296c9030df4ddcbf0bf78be28f6698ade254cd9ea7a80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:11:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:11:37 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:11:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=00115e7e10447a1f2e16aedad43cc33205a30e546e0c881e6dd8703bf8b6acf9            ;;          'amd64')            CB_SHA256=40e45a65a78bf5c9bea0f0d16a1c2e3aab3704aaadd41dccc2d8db2308f30fcd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:11:37 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:11:37 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:11:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b059b2065a301b689a97e29a44f7740d103b4eb6062ba13a205aefd3fb9a8edd`  
		Last Modified: Thu, 12 Jun 2025 23:32:13 GMT  
		Size: 44.5 MB (44463012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c19d4b0a4a35ae5cfa235ab8a8b079e5ba8c0c57888045a9b8c22d03cd6a18`  
		Last Modified: Thu, 12 Jun 2025 23:05:15 GMT  
		Size: 877.9 KB (877913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f7aeb36e17d659bb6444331d594dc893c6076cdf7d4ba344d88e4eaf29909c`  
		Last Modified: Thu, 12 Jun 2025 23:05:20 GMT  
		Size: 3.7 KB (3726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8334a679699f1eb83955fef259a53d1db4957a35db8a0cd6cad5c6ad446102`  
		Last Modified: Thu, 12 Jun 2025 23:32:22 GMT  
		Size: 624.2 MB (624198884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a7837b180f9156c6abb8a2b1318f536ff15830b273ea41afa31708736dcdd0`  
		Last Modified: Thu, 12 Jun 2025 23:05:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ee17442969f3e1824dae9347fb3e51add7325a448fa74e3a15d689bd9ce6ed`  
		Last Modified: Thu, 12 Jun 2025 23:05:27 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83a19acd1280865a5fa48949e03d150ed69d014f1d34105e38b11589c5d598c`  
		Last Modified: Thu, 12 Jun 2025 23:05:33 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686c2c2a20b0e3e8a0911e53ea126b38be748b671e3e99544e754c360d6b61b5`  
		Last Modified: Thu, 12 Jun 2025 23:05:36 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d356a8ffb6bb90dec436ff189c1d71ae4f92cd468a55d61d9ade75cb983afd7d`  
		Last Modified: Thu, 12 Jun 2025 23:05:38 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a4faf0c5f1c7e5f849554821b0b0b2b3f8af38d274cf279068abc83ac8004f`  
		Last Modified: Thu, 12 Jun 2025 22:53:20 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.7` - unknown; unknown

```console
$ docker pull couchbase@sha256:545b1b87718b8b5eca43417ae3dcf7cb53ec17894f57a3258028ce74df44c7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d995ea0d11c1c46c8f241f8c8e5fe3dae8979e13a5216219badca20860d2c3`

```dockerfile
```

-	Layers:
	-	`sha256:c4469ec1a0b391765f5dcacb1d23d5921657fc7aa6818014cac7c64a8c24804b`  
		Last Modified: Thu, 12 Jun 2025 23:31:48 GMT  
		Size: 37.6 KB (37564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.2.7` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:425d1b1f7c5c4464b1028b3ca0b0c8936f8607f4c4696bbb3f6cb02b4b136ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.7 MB (677743552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aff41b5d201a1751b1977c5dc671bf6f2238a2eb330f3bf134ddae53b1b861`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:11:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:11:37 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:11:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=00115e7e10447a1f2e16aedad43cc33205a30e546e0c881e6dd8703bf8b6acf9            ;;          'amd64')            CB_SHA256=40e45a65a78bf5c9bea0f0d16a1c2e3aab3704aaadd41dccc2d8db2308f30fcd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:11:37 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:11:37 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:11:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107df1885da6b3f0d704e6528f98f7fa3c94661b8f92990d84afdcb07a1bc0b`  
		Last Modified: Fri, 13 Jun 2025 00:12:58 GMT  
		Size: 44.3 MB (44276800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc711ea2f9a6417737f414cef7ac703989f3b88829d303e343141988a94d9f`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 765.0 KB (764954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be692b5118b612d6baf9aa9056ae5efd493c5e9807362896fe797727feabfffe`  
		Last Modified: Fri, 13 Jun 2025 02:31:59 GMT  
		Size: 3.7 KB (3726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96b46f030472e3c9887d60e529d203e2520faed550d9e2f820d457bdcf3404`  
		Last Modified: Fri, 13 Jun 2025 02:32:47 GMT  
		Size: 603.8 MB (603842983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396b6c8f201c323bbc9732984f221b5622b737aff275bf06a986f02258acc0ad`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd221398619cff3d7fa1480346668e9bfb337326486382f1231e73d97ad53d2f`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a28a2a71946b0b6ea40d615326d40c20df71d7595c9b0359180ac902139be`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6737f3f4e13bc3f3b9bf2d3f96dcced60fd3275060344ba64cbc8555d6bae58`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb8ff10d43f845e6eef6a3054eb46190dfd8eddb8e6a159aa2775c4ca88d6cd`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352df11691fd4077f6ca6af024d7f8aa6ea677c4504fbab1b06b704f01d38ce7`  
		Last Modified: Fri, 13 Jun 2025 02:32:01 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.7` - unknown; unknown

```console
$ docker pull couchbase@sha256:99b5fcabe832d4ce7387079d20afa4755e3539e19572543fecb6438ade41bcd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b23d66c20d413a34a2a2917605e4b394df2e4a2f13aefed99bfca7b3ff95bdc`

```dockerfile
```

-	Layers:
	-	`sha256:fa81e88d6461ac706ae299513ee2ea65e25f206d666958092773eb4582c787db`  
		Last Modified: Fri, 13 Jun 2025 02:31:49 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.0`

```console
$ docker pull couchbase@sha256:fcdc4b32e4a6fa8c0330e23fae5df21725096777296bdd98b57e826e5a5d91cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:8c58435ff60d6ef66d0df41857332d957c1eaec67d6d0e8e2b16b9e87b20af1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 MB (760173247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07541be50814b75b453f83cf2c5215da9d0d51cd2f57dfaa0f004921cb713d2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:28:01 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:28:01 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:28:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:28:01 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:28:01 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:28:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672f48fbd7973400f2aa7ee2ef624e3a15ea0781a2654c7a044f350fdf17254c`  
		Last Modified: Thu, 12 Jun 2025 22:54:47 GMT  
		Size: 39.7 MB (39661820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28913960457f71b38567d7c306bc339d2ad81b0b7f5210c70b4edb0bf9dc2ee5`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 926.7 KB (926716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd74d520bfdd7cf7cfe25896e800591b136144f982501697ff8bcbcd38cb2b5`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9701b9399e309603581d5df8ef5e32b0f2752ae43079e46a818f09e7aedd28ff`  
		Last Modified: Thu, 12 Jun 2025 23:33:19 GMT  
		Size: 690.0 MB (690046534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28482dcd9d94263ad7efdc8a71c830dca382188b456a02624ea3a20612fae067`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d788221dba99727f03e93703d08373582b49fa74c4ac61ff458c14503c1c1c5`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfa9e9407ba3b9fb4e6ebe7e8d31d8e47967a45746cefb3ec4ec49aba051e18`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd6ab5b325f510f1ce8dbd588ab0457038dbf53499ce740e276fa94dc09019a`  
		Last Modified: Thu, 12 Jun 2025 22:54:46 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf340e6775252fbf2d20f2fb23fa52506e0cb8a185c9d580669c4430796bc99a`  
		Last Modified: Thu, 12 Jun 2025 22:54:46 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bfbcb12390eeca93aa3653d2f55e92e73bb0a1159a0d7ba30fb236dee9e976`  
		Last Modified: Thu, 12 Jun 2025 22:54:46 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:ecb47bfff99767f6d0b2681b141858e110b451420e58abc6f890fdc3851701e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90439dd8b70e239fbf144f025e3ccbf63b171ec41eb6bf8be20a4ed2f05e0b3b`

```dockerfile
```

-	Layers:
	-	`sha256:db5f59511b1df4122c7565e668ce3c5155126bbe6b2e19ad6f80ac3e1f8abf8e`  
		Last Modified: Thu, 12 Jun 2025 23:32:45 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:8aa182e860c5d2fdae1dce2eb4dfecdde355f8e0823c365876b567ecde85c320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.2 MB (732246834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3da683fc3547b0359304a7bdced0a6dd595e2047f786daf9d62042b4122f7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:28:01 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:28:01 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:28:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:28:01 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:28:01 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:28:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949b410f178786e3a791e34cf4caa97ce01371746eda082846015d5e4bfc5eb5`  
		Last Modified: Fri, 13 Jun 2025 00:21:34 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0ce8ac50e9fefa9df2b0402b19bd806c1297ccd96d66aca9b10bbf8ad213ca`  
		Last Modified: Fri, 13 Jun 2025 02:32:17 GMT  
		Size: 664.9 MB (664908329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7861f610f7e4584905c7c272843e2b1a1ae6981d2b0bc418ce2ede67d2e38`  
		Last Modified: Fri, 13 Jun 2025 00:21:35 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42df63d6ebe20b4d802f3f893389db5ef4ee0ed02f7b186f5668f73e96da20`  
		Last Modified: Fri, 13 Jun 2025 00:21:35 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fc61264ad0267e54e0910f263ab8cb3838aa7bb8b0db75ca61a75833bb6e8d`  
		Last Modified: Fri, 13 Jun 2025 00:21:35 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9942a900a81e9dca916e1454757318862359d7181423fde8896bd270142abb1`  
		Last Modified: Fri, 13 Jun 2025 00:21:36 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd42223f51d5c494334523a198291ce7578154ad3085aefbfe3e060cdd1781d`  
		Last Modified: Fri, 13 Jun 2025 00:21:36 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c67a232a421feb9116d5357eb6b5003c276f1f04eb3f90a38f46a012da195a`  
		Last Modified: Fri, 13 Jun 2025 00:21:36 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:c3816aeeefa647e9ebd9d312ff2bbfa7f276eb960b90685be3ad0698f5b3bc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9aa755623c51b01c98cb273ba0b80c0956d36f7699eba462521fd7c327f349b`

```dockerfile
```

-	Layers:
	-	`sha256:ca5806b4c12d660a22550e39e8ace2e7f285891c1df2c7aeba9204d39001a268`  
		Last Modified: Fri, 13 Jun 2025 02:31:55 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.1`

```console
$ docker pull couchbase@sha256:38dbc5eca6a2c7c3c3ec3c9680da757421e2c238a493027c1a7f562c5742741c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:fd607b754f44fd8718d872e3b45bcd1e76ef6eebf9b05a9e4629a0266198fb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 MB (760198848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88590696426d49a5e2ef00e0861ae0e665c412c6aa436537c48c48a7fece5fd3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:37:02 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:37:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:37:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:37:02 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:37:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:37:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e39031db150ce656cf9ca6a0fca0d064165dd6a74217a23da76bad5995bfcae`  
		Last Modified: Thu, 12 Jun 2025 22:54:15 GMT  
		Size: 39.7 MB (39661970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d673779b83adf8b8ed2f7c68fa1df646fb53d3b619954f75d59e15a37debc3`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 926.7 KB (926658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2cad75f5e35fa7ea4bce1e8e5c4b23fcf9fa5d28474f4e42771faf47d32dc3`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93292503745e1d91b7f00658690ebd8a1d02145bace63c37f5fe52f8ed1aabe4`  
		Last Modified: Thu, 12 Jun 2025 23:33:28 GMT  
		Size: 690.1 MB (690072039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfd485997df4612e9271e8f31669df600f763072a758d987e5afc0f86193ea4`  
		Last Modified: Thu, 12 Jun 2025 22:54:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd51eb2052c1eb2d677d57128e7762a6eb1f6c48a891f970477f7b9f1458be7`  
		Last Modified: Thu, 12 Jun 2025 22:54:14 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d11ccde910c127552791c99203152099a2417683047e77bebc89180c6f35`  
		Last Modified: Thu, 12 Jun 2025 22:54:14 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e49970b2b2fffc8fdfaf2d63094df41f865fac6816e401c97a35b959ad3f3c6`  
		Last Modified: Thu, 12 Jun 2025 22:54:14 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523793682babdfbae10abf450f3190d11461e112acf046c32680165d7fcd4fa6`  
		Last Modified: Thu, 12 Jun 2025 22:54:15 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4790857e1cc2dad01c5da2bffd3d1dab5d6c2d096b70dec4545bc41e3b0d0f68`  
		Last Modified: Thu, 12 Jun 2025 22:53:42 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:66c869bfef0ca748e17a02c857574bd3f707cef9b3a9ce9fc582c2c55cc1736c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55f0c7fc2c3d0d7abd95872dbac356d2ca9c2a989f57fb78949ffffc5cadd57`

```dockerfile
```

-	Layers:
	-	`sha256:1957712fb032d050690aca408537e8c8960e0653a4da3c222d190a8f1083d0d0`  
		Last Modified: Thu, 12 Jun 2025 23:31:59 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:260465c69f1cd94cf6f05661a6d176e0783fb656e94869a1233809de36f1e499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.3 MB (732256190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e97c6fb733cd8bfa1d849447c25b1f7d38c7706ccecc11bcda6ca0bf65ac1d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:37:02 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:37:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:37:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:37:02 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:37:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:37:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302123858fb97709374ed5f0a5ab03a0219ce73bfed4421d66e809c51ede908`  
		Last Modified: Fri, 13 Jun 2025 00:18:17 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0cc7effa53c5c55e7f2b8e111b5a7057dd11323e57cf6c97a12541e41444c`  
		Last Modified: Fri, 13 Jun 2025 02:32:56 GMT  
		Size: 664.9 MB (664917689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41824fa2fdb6bb2e9ba7fa544931671742b7045afd9c67cdb3782f423f006e8a`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc4a03842852c17e967ac5342dbe8ecc31e0fc62c8c99a10566483dc37e359`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1116f3e3f0afa1e47a10b485a5638452fb0f8f2f3c7ca563131dad136a6e794`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ba829865135a6eb347d14c978f3846c7dcc664d707e99982a0cc01d2bee32`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6855c02d059c04f5c3b6f05e056955193e06f87fd490af65ba3e0aaa2b1e601a`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4265ecdce870e125cf87962388458ab697ff852085339a7cdf2ffc3d255f56d`  
		Last Modified: Fri, 13 Jun 2025 00:18:20 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:20a9fae29b2197bf9a658d76becac93535d9ddd4e8eef22084975309941b4845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd06b10f8c873d09f7052d7ff1daca1afcc0d9754dc447c7b41a53780955637`

```dockerfile
```

-	Layers:
	-	`sha256:1f3813e8bd608e8b8863d68fe18dde3eaf5b1070c18c30f16a8a5186edfd938c`  
		Last Modified: Fri, 13 Jun 2025 02:31:59 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.2`

```console
$ docker pull couchbase@sha256:617e8e93866dc72fd505053eb1f60a516394d4868899f5463b05917eefc4256f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:ca8cf49e12246337a3b8147313915822dbfc50fe0a042e175603dc75947c84b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.4 MB (774351777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced95db906874cae18d89890bea37f4bf27f61bfdf32976e1e5dabaa8f203371`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:45:24 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:45:24 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:45:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:45:24 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:45:24 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:45:24 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3882126313fe1a25b4825da041ace7b8bc7f7f228a6bf588d2bfb1df9c26a6e`  
		Last Modified: Thu, 12 Jun 2025 22:54:09 GMT  
		Size: 44.5 MB (44462796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0b40090f76c753c8eb038cc192fd505dcd942fd017c63f9284b488639deabb`  
		Last Modified: Thu, 12 Jun 2025 22:54:07 GMT  
		Size: 877.9 KB (877910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e0be32a665300ca61ed94fbb4d98c09fae2b720fcac15146d4533815ef41fd`  
		Last Modified: Thu, 12 Jun 2025 22:54:07 GMT  
		Size: 3.7 KB (3727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5546dc435c89078d16707ace865c3703a6cf5765bb3bf611d51a4c1cd56feb0b`  
		Last Modified: Thu, 12 Jun 2025 23:32:29 GMT  
		Size: 699.3 MB (699288816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f307ccfdf77152847509050292006e6c2d72069c62bab7be9970c9f3735ed8`  
		Last Modified: Thu, 12 Jun 2025 22:54:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a16d1afa31985697405cd913acb67158cf5d39ad047b0693f698f310ae31c0`  
		Last Modified: Thu, 12 Jun 2025 22:54:07 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882d677decc39c0d8272e63c8c284b8d6deef4c3b4575894e24f2ff64914e2eb`  
		Last Modified: Thu, 12 Jun 2025 22:54:08 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d83b82cb36dfe0db3592c2903209c0a5d165040c2978a985bdabb3c05a4010`  
		Last Modified: Thu, 12 Jun 2025 22:54:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c66aeed2ad9a7c37ef2a926d6ee819ef13ed6511bc8ea514b34a2f44de76fd9`  
		Last Modified: Thu, 12 Jun 2025 22:54:09 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b27bfad1805a8c209119f1e44b896c0c244c2de1e7e3c7339b1b2450db66de`  
		Last Modified: Thu, 12 Jun 2025 22:54:09 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:02169ee36208c613bf0e0fd62fc043b027417bc7a77cce80c714d71e32b15951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316ded06288cd67d9131d05bed503c06f902304d5ec28bd9bdd5e9c915692e2a`

```dockerfile
```

-	Layers:
	-	`sha256:7b4c1ac3ba72f9ede95c0ff77413394a8c783c768f58fdbf2a827d6919a56531`  
		Last Modified: Thu, 12 Jun 2025 23:32:02 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:777def477daf718cd43c2fe39ea247038cdb937f737415ecbed02fcae2d9bdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.3 MB (747295599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410c68a8d54c5f897ab48ed8400db7071641c92174401e08439812353542925a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:45:24 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:45:24 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:45:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:45:24 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:45:24 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:45:24 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107df1885da6b3f0d704e6528f98f7fa3c94661b8f92990d84afdcb07a1bc0b`  
		Last Modified: Fri, 13 Jun 2025 00:12:58 GMT  
		Size: 44.3 MB (44276800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc711ea2f9a6417737f414cef7ac703989f3b88829d303e343141988a94d9f`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 765.0 KB (764954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3155b24d9b7071433303d6350d6fc960f85472c86fc383cdef620190cda64385`  
		Last Modified: Fri, 13 Jun 2025 00:12:55 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c87b61fccd5893ae49bf8b33baed55acbf276491c523f51007b8224445a02d1`  
		Last Modified: Fri, 13 Jun 2025 02:32:59 GMT  
		Size: 673.4 MB (673395035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39920de859b77d1cd52a94dd38594ebcd62fa3b1d73aeb61d7617163239b3ef9`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7503cd2524050cb4857d3586ba56d7c7e1bb40915a798e7d19feb2614a4cedf9`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7475c3a523104cbb21edce6e8460f41e07e2c97d1e2869f502e183c41078d9`  
		Last Modified: Fri, 13 Jun 2025 00:12:57 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12176b6ca9a5d1d52bb1659bdda87d6cfc0f434fa710467f473f83a65850944`  
		Last Modified: Fri, 13 Jun 2025 00:12:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9301660eee6c297fa23b70bcd066146ea1c2765a8ee7257db66c0ceb81eb18`  
		Last Modified: Fri, 13 Jun 2025 00:12:57 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8aa3b6a7e8cf2952ee27ebc80f9422015e0bafa123fe7dc5e6900fba74b5c36`  
		Last Modified: Fri, 13 Jun 2025 00:12:57 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:78be8969caa00accb9b2a0240c07b3ff5d0b70d83e903d76b9cd0c40b285d64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcc774416e8ff563d50b87dc0c71edb3336ae5f3e57527fb6d2294632100a3e`

```dockerfile
```

-	Layers:
	-	`sha256:f58d47e20a743f295b24c671b3b88096e32179a313d9750e4073caa93cf859c9`  
		Last Modified: Fri, 13 Jun 2025 02:32:04 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.3`

```console
$ docker pull couchbase@sha256:f29225ff3d52cf9e793c27af4e0f89305b9d4897393ad9ad95a58138174abc98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.3` - linux; amd64

```console
$ docker pull couchbase@sha256:aa8da6957cac0f4690685fb729577c16aba6bbb8d8d2dccdc4c9ef2aa8e71227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.0 MB (768950880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab146357bae23f7b2666a91639ed99a88e26c8de3bedbef971ca996f7e0adff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55222b70d50b4c6ab08b229e868de57bdcd2cf94c8d2c8398e6a4079077dcb9`  
		Last Modified: Tue, 03 Jun 2025 13:59:26 GMT  
		Size: 39.3 MB (39303165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c44a8a81960048f337df5b1d2876d8db39f18a4d15a3652130caf651b08584e`  
		Last Modified: Tue, 03 Jun 2025 13:59:23 GMT  
		Size: 926.5 KB (926489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be96b2f62cb9e476616bb01bce73aa8b42b17c8c5e969b09b4edf1d7d3de221a`  
		Last Modified: Tue, 03 Jun 2025 13:59:23 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97bbc27af356991c02b775de2a194b0df095827669c832a76b9cd06f84ed2d3`  
		Last Modified: Tue, 03 Jun 2025 13:59:52 GMT  
		Size: 699.2 MB (699183043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f479e0fdd5d97f5cece894147abf8af640f3ed7ce7e7419afd5d3f5a60dc41`  
		Last Modified: Tue, 03 Jun 2025 13:59:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d119f621afc395f502b91ae991e509cb492c9338e4eec703caa06b5e30936abc`  
		Last Modified: Tue, 03 Jun 2025 13:59:26 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aca629660826303ac3e396bd9341711a53aeaa0a031ef68dd693af3fd87a1fa`  
		Last Modified: Tue, 03 Jun 2025 13:59:27 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef38953cfff5bef3c935f2169b1743906082dbf2fb8b74f611e042da5ac7e3f`  
		Last Modified: Tue, 03 Jun 2025 13:59:27 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87451e6d0a03ea5f6b6ef031f00864f9d885fae621b018b3857a1642a6827f`  
		Last Modified: Tue, 03 Jun 2025 13:59:28 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ed3a9fdf3ad7d37e36b9b22b9f67105408285bda2f1d71474d608818ffc48c`  
		Last Modified: Tue, 03 Jun 2025 13:59:29 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:322632fd79638a00ccb5750f721f5caaf09923c652f75b0de915dbf8a8a77038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6cfccdee9d1c6a9bc88d654804bb8c3428b18aa879a2fb1b17f5b799112b7c`

```dockerfile
```

-	Layers:
	-	`sha256:30550a622610d3e98a55f0f5f2b57e34d0343539f397186bd92e3b89baede131`  
		Last Modified: Mon, 09 Jun 2025 09:39:41 GMT  
		Size: 35.8 KB (35816 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:2a759f1ddced1a6fa2c8e68facc4d053231438860e9cdcdd7cf57367e34e8793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **740.3 MB (740276108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1438957e900bdb6e7d66a195bbdbe773851563b8b124ae48e27dcdf30d4d58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b154720591954ca83cbc0b928875845debd45fcdd5096534cf440f0fc16986e5`  
		Last Modified: Tue, 03 Jun 2025 15:24:45 GMT  
		Size: 38.8 MB (38849664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e244477b78cc71a61574fae065b6dbb60f35a58c3a4e8123349f9a4de88d428e`  
		Last Modified: Tue, 03 Jun 2025 15:24:47 GMT  
		Size: 770.8 KB (770780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f050eca393d797b23ce8cea8082de1b24b4bd73065997fb4d1c2b0a29e96b86`  
		Last Modified: Tue, 03 Jun 2025 15:24:59 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edabb57d607c5dc7ed3962162bcfda1afb083299ef68fe8e2c50654ea285c266`  
		Last Modified: Tue, 03 Jun 2025 15:25:16 GMT  
		Size: 673.3 MB (673294899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14145d888a1bab86b49550c932bbea8dea33f4ebbfad7bbac7d60e597f8ab9cf`  
		Last Modified: Tue, 03 Jun 2025 15:25:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765fac2fa5480dde9bec86cc095ce940692600d829cabf3884d7eabd3796b78c`  
		Last Modified: Tue, 03 Jun 2025 15:25:43 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1695ab1a7319c572db06621456ebae651bf501a56c9885bd151a821d87f55b`  
		Last Modified: Tue, 03 Jun 2025 15:25:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3163f0787aaf49e308ce31c8a9c615a7553238f268061ad5a9e384f680f05a`  
		Last Modified: Tue, 03 Jun 2025 15:25:47 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297edacd09fccc9c8389aff7a9c110bafa3829928be377cd2659efeddb151354`  
		Last Modified: Tue, 03 Jun 2025 15:25:49 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5da48f4d40906bddeb8b543559f8ea3eb0c46a4828d857f33e339d9447dcd8`  
		Last Modified: Tue, 03 Jun 2025 15:25:50 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:f6317c5cbbface9b95a038df62e43852366f11f2370ea9c3605eed5580d0005d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad297eb02eb69ded13d1a799d9a42c81f55abe5085c62da7e65fe50657fea7`

```dockerfile
```

-	Layers:
	-	`sha256:b938abe563324a7bba451c43857a95da7ea9c4f2c2cfb99fbef902036889ff38`  
		Last Modified: Mon, 09 Jun 2025 09:40:23 GMT  
		Size: 36.0 KB (36001 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.4`

```console
$ docker pull couchbase@sha256:fe89075e364455e25a09c2c4cd663b9a579453001db64a990bbd83cd960a2b37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:8f17595567e2af921ebed345cdcf762f537705085ae15113800ee5f50877cc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.6 MB (771641867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c86687d7d93b858d8527ad737c86b9225a487026572d223ebf063a0c4937b99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Dec 2024 01:31:34 GMT
ARG RELEASE
# Wed, 11 Dec 2024 01:31:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Dec 2024 01:31:34 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b474f1da5b847f8b8cff69cc18bcb780f85d2ba869bac4f7f648323563e45c96`  
		Last Modified: Tue, 03 Jun 2025 13:38:35 GMT  
		Size: 39.3 MB (39302774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f20a70270ad90fb3501c9902d7c99ebe44d6a33de8a7ea07e69583eb02bbed`  
		Last Modified: Tue, 03 Jun 2025 13:38:32 GMT  
		Size: 926.5 KB (926503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50bf634fe340d52f8fb091e69a599bc3ee4f5710f8ad5f213c85bfe5ffc1e80`  
		Last Modified: Tue, 03 Jun 2025 13:38:32 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce17fcdb19e9aff9c1fcd3d1ecddb2723802122963934355d6c0f88554834bab`  
		Last Modified: Tue, 03 Jun 2025 13:38:43 GMT  
		Size: 701.9 MB (701874410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765a02c753fa411a3804a288d48202488cf820caeb9b5ce777863ff992250f0e`  
		Last Modified: Tue, 03 Jun 2025 13:38:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae846ae6621a11dc987bcddfda7a153e60d56fbef47fd950bf14ef4971672a2e`  
		Last Modified: Tue, 03 Jun 2025 13:38:34 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0402ec5fb7e687854b511c872d1ce6e362c43f98d1035bceb09a946292abcee8`  
		Last Modified: Tue, 03 Jun 2025 13:38:35 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b080d8344eb228c851803ba32c22a556f02a60b141587290f2bcc7194d2b5a`  
		Last Modified: Tue, 03 Jun 2025 13:38:36 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967466dee179d250ff92503444e804444873417b8a909ddec81bdd7a710511bb`  
		Last Modified: Tue, 03 Jun 2025 13:38:35 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543636058992d931a7b6a573e54564235768a9eafc02d3a6c40dea19d634acb9`  
		Last Modified: Tue, 03 Jun 2025 13:38:36 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:d8b55ce73a114df6c730693943dd1738a033f4c660e2b96f029cf2f960ff0003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2126fa67fb09cdab45ddf4c0943bb57b980507e764dfb0c9036ccb9003999`

```dockerfile
```

-	Layers:
	-	`sha256:d0911ee5ba0070ddc6341ca142efb79f30c770863ff7000b952f2c38402a44fd`  
		Last Modified: Mon, 09 Jun 2025 09:41:10 GMT  
		Size: 35.8 KB (35816 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:fedd1c2701d8e23b1336d428397945d8b4119aa36ec90ccc5ed01eb27ff3c2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742538627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0564948e24da3752c3ceaa553bf256d8796e93697d0db8507c9ac35cb77f38fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Dec 2024 01:31:34 GMT
ARG RELEASE
# Wed, 11 Dec 2024 01:31:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Dec 2024 01:31:34 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f361a6f25d6c2f377926be0702e03dc9020fd5bb8b191d1b234a4d32f7f2e66`  
		Last Modified: Sun, 08 Jun 2025 13:16:46 GMT  
		Size: 38.8 MB (38849514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a669d8a690ed3f16e2ab00fa8214a52de719f88a9e1e23bece54c0d8baf3e72f`  
		Last Modified: Thu, 05 Jun 2025 00:47:58 GMT  
		Size: 770.8 KB (770800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646547249b04cf88edb49f635fef620c23ba8a643faa4b2ff8f1f6247ba03c22`  
		Last Modified: Thu, 05 Jun 2025 00:24:24 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231dc9ceae02aa6e40e37648f0cd1726ab1e05ca0e6d5cf8310303d28eb3d783`  
		Last Modified: Sun, 08 Jun 2025 13:17:13 GMT  
		Size: 675.6 MB (675557549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a737d39bc61fc15decf4a2e6b29f1be076a506471159bb2c50c4fd933be76e0`  
		Last Modified: Thu, 05 Jun 2025 00:43:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf90132ee89615a36b1c5f37e5291641a7498672275061c547648de3279a9eff`  
		Last Modified: Thu, 05 Jun 2025 00:45:14 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628447a14c4cbea637f72796599c3b120b714280782c7e3e012e69333ab23f41`  
		Last Modified: Thu, 05 Jun 2025 00:25:41 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f94330626f2e359c1997d6b178c6a0c03978e1eae9f5dae1cf57e49f947c8`  
		Last Modified: Thu, 05 Jun 2025 00:30:54 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a470098480b27d22a01494dce12c03aa32cc5a1232d45ab02f2d77f95a223ed4`  
		Last Modified: Thu, 05 Jun 2025 00:29:52 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445bc610a57d7b990415ad150673af0cacf1ef671b638809c4483d45669140d6`  
		Last Modified: Thu, 05 Jun 2025 00:28:59 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:6703008d78bb7f76b08aa148b9bfd3a24385c6047c5d1d98054b9e2ec9300240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e515c7ee094b3b0f61b49f64b6429f6324995d1cb7d3f9bc02f640aa6912628`

```dockerfile
```

-	Layers:
	-	`sha256:e6e734518b1d52aafc2675f97053ab22cd46ff7e007efc3f8bac926d313cfe71`  
		Last Modified: Mon, 09 Jun 2025 09:41:49 GMT  
		Size: 36.0 KB (36000 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.5`

```console
$ docker pull couchbase@sha256:53cabb59e0a6ccf313b0c626342857697bb7d9045e7e9d0bea1f0c9c4ec2f82c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:e2a5539f374401a1ccec4e421e3458628aee15f1a0b866ffc0ad1a0d7f5af427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.5 MB (771502076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c3be3031535a1639e938ad3b16caefdaeadc1ab276da48ebe73f9aab01a2f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df6d811e414c9bc0fa90313a5ce9ee533a0db9c4658fa92afde557c0fc3b4d4`  
		Last Modified: Tue, 03 Jun 2025 14:21:43 GMT  
		Size: 39.3 MB (39303079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ed4b23b372ec2d8be0d41054c75a1e80e784910e019d0fe86688efd3c1d9e`  
		Last Modified: Tue, 03 Jun 2025 14:21:38 GMT  
		Size: 926.5 KB (926524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862f0a3683e11cad7cc02782d6011c0e571f17f1eb5c000a8d2025a8c3893963`  
		Last Modified: Tue, 03 Jun 2025 14:21:39 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279ad3bbfca41c98ef9b4dc6d7fd9979c04720a54427c1795c640d989f850d64`  
		Last Modified: Tue, 03 Jun 2025 14:22:03 GMT  
		Size: 701.7 MB (701734298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97630b598230fa86b42fd9f6172b4193d182f5bb10a60257f790f664e2bf066b`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ac2c371a7eae27c0e3881d6f60e62b53d7b1d564b8d1bf1bd1154df49bad06`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e1fce97eec6b12373568d9298ace868e680da3666ea8a23a8d28172f70f842`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e941e9da6a51d4b21df61434f398328cae1d3dba5ed62846de65e6d5fc7815a6`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73769932534b2a83793205d49391a878725c37b62293cf84f5b21c2fb2b97d1f`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543636058992d931a7b6a573e54564235768a9eafc02d3a6c40dea19d634acb9`  
		Last Modified: Tue, 03 Jun 2025 13:38:36 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:2b48d96ee77f7a90f1b4467865c7881530ac85ee8319590ad1131241be1e16f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31ccf954e591cd39beed8b92b87a4cfb33c75eb118a7c85eb3ac103803f7d2f`

```dockerfile
```

-	Layers:
	-	`sha256:d755417d8bac42b0e89c6a1fc7e854d6e138796faf3daeccce06eaf3c2f28ac3`  
		Last Modified: Mon, 09 Jun 2025 09:42:29 GMT  
		Size: 35.8 KB (35815 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:44df46e4dd6331d55bcdebb1b42d7456fec362b455b06643d4a9ff1b7e1d1b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 MB (742447046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c642f10baa1c1f95c4fd182c779f6de5b958cb90aaa393ba33d69699c5af3f87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb218b446475a0d4ef98ac0a6db53f42870b1da38289d0c5e60bff4e9d16e00`  
		Last Modified: Tue, 03 Jun 2025 18:33:24 GMT  
		Size: 38.8 MB (38849424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75e7de92406d824e5b74f949abbe64e88cf0040128c07c384a24c6feedd88a6`  
		Last Modified: Tue, 03 Jun 2025 18:33:22 GMT  
		Size: 770.8 KB (770794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1444fd4fe9e404a94930de4acd996527fdfffc3d0d1094277159b9d717b8406d`  
		Last Modified: Tue, 03 Jun 2025 18:33:22 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c73bb60bd14f2ccdf3877c41d2dd981c2d83ede446cbe1e2a17121cfb9e02c`  
		Last Modified: Tue, 03 Jun 2025 18:33:41 GMT  
		Size: 675.5 MB (675466064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6606151ebe3c7b0d421fb4f4e806eb2b702734d351232e2584583cc6d54f2968`  
		Last Modified: Tue, 03 Jun 2025 18:33:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21da1ebba94c5246925ccece3d1cef02b24d91428cdeced0ddc1c01d2dc30842`  
		Last Modified: Tue, 03 Jun 2025 18:33:27 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7756633777d4a877f22d181e683180b97887e1ed4c26cae124daf15f558d4a4`  
		Last Modified: Tue, 03 Jun 2025 18:33:27 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628745b3c92e6e0ac6d209b65897fcaa7d1f9fa28cab52fe71c960d7f44fa707`  
		Last Modified: Tue, 03 Jun 2025 18:33:29 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0867532814dc2223df70637b5efd7792188339cba79d2ad041581d8bb6a51`  
		Last Modified: Tue, 03 Jun 2025 18:33:30 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a471e6d02789d12ffdd987716bed3c6161b99e00c9053e8717e40ee3e05638`  
		Last Modified: Tue, 03 Jun 2025 18:33:32 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:cf1fd9455b73fb3eec6e8c228c2937f2e4a1e2cba8de00ec717981aaa530918f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14af482de3103e7b7dfb2be6e93415a1378dbafcbf8632f23870214875f4e217`

```dockerfile
```

-	Layers:
	-	`sha256:1dbd85a2183ab607d618287882ab20aa489e848bb687bed4c8affbf4bbfbcb92`  
		Last Modified: Mon, 09 Jun 2025 09:43:07 GMT  
		Size: 36.0 KB (36001 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.6`

```console
$ docker pull couchbase@sha256:ed940813ca0f960529d855c742f4372df0e88b0ade7c0679627878e42b6c4924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.6` - linux; amd64

```console
$ docker pull couchbase@sha256:813b49e0ef39898d3faebf195415d335281419b36e9e91bf735b5f7e343bd056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.7 MB (794747783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ffca8857d13518cb9908e5b399639ad3252e6a8cedbfbdbd81ae23dde24b27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c3b3cacce9f37e529d00643dc6a7356b93b7d570405de6a0c61641956cbc26`  
		Last Modified: Tue, 03 Jun 2025 14:07:29 GMT  
		Size: 39.3 MB (39303163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dda7d77f72011a4ebf049e73e839994a45f1e0354ec21466733d34be426f15`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 926.6 KB (926575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf7924979a5479a138d955d08a263461036a06e7ae36502d75c3c538b2ceb3`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0988595feb9082d9db0ef1f794d362bafef150552c279ccbef7d19658e7245`  
		Last Modified: Tue, 03 Jun 2025 14:08:18 GMT  
		Size: 725.0 MB (724979867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b1e063f9f2404c773cd3c78b32f368fa15f399dc40dfb9f672cf164f335f1a`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bea16e78db287004b1ad579baf90c6b57e09cf51ddc0d96a0310218cd724e1b`  
		Last Modified: Tue, 03 Jun 2025 14:07:23 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2709a0a231e86cd0d2106017eb8e7f72cd40b9437fa35ee1d4b905ccb449ea8`  
		Last Modified: Tue, 03 Jun 2025 14:07:23 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082fb5c7ef2892c9a9fe0f11aa63bcdb5f588076c0cc5d8f95ecfa7aebe54ebc`  
		Last Modified: Tue, 03 Jun 2025 14:07:24 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254548277f51a3a7ba0b0bb147b391c1bbb5c6d00278719e96c50b077a7401b4`  
		Last Modified: Tue, 03 Jun 2025 14:07:24 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124a32eeb718d8c54c6f29c2cfc25b213993e9c7c18a2aa9f78a6fc3406b8c8`  
		Last Modified: Tue, 03 Jun 2025 14:07:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:1daaa4381959c4b4ad2f72a92916db538dbbaa3abec64a39c63885b05dfd0d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15a75a67b82da4a16cbe101895e937cee932dc19cff9438f2168fbc00d96b39`

```dockerfile
```

-	Layers:
	-	`sha256:33308da65b82e8843d44557e4599ddcc303a72f6765b43c1b91b30528910a4f5`  
		Last Modified: Mon, 09 Jun 2025 09:43:47 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:98e455037d80a274b6cd74cd39f5af3e415f82701681c0bec5e79741e3870fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.4 MB (763408090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248c506b8cd15abac9233058c8c0eb3b712c0cb0af360622488f453792122ef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffde452cdb09fa506c9cb01e48875a79d2ded94d9d6ddd3f83c385acea1eb61`  
		Last Modified: Tue, 03 Jun 2025 16:23:38 GMT  
		Size: 38.8 MB (38849499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c55621952ece84f3edc704718bb4859c7e103a8964f6844479de0c663696207`  
		Last Modified: Tue, 03 Jun 2025 16:23:36 GMT  
		Size: 770.8 KB (770806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9129adffdc0253ebbaaf1fb32ef66c49ad8caae70fabd05c02f825d48b70a3`  
		Last Modified: Tue, 03 Jun 2025 16:23:37 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c25687cb69cd4f05d93b1b6b36d4e2ae9b3ec616d633182a417b035ec7587d`  
		Last Modified: Tue, 03 Jun 2025 16:23:47 GMT  
		Size: 696.4 MB (696427022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2472d3bcb419b1c988d37f3335bca984f97e4761e92591bbd90cd6c310c3ec0`  
		Last Modified: Tue, 03 Jun 2025 16:23:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86103da5720e37d892f6759b260e4e107cc473a6bdb28fd91e56fd9c0874ec`  
		Last Modified: Tue, 03 Jun 2025 16:23:40 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb1c195d48e7e38da8cf8ed94d652eac554674f4dd6a11e3b3f5e2a5638e5f`  
		Last Modified: Tue, 03 Jun 2025 16:23:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245cae7b9c382625baa4aa92f8cbad7a51be6eeb8699cb27fdea759f77a321b7`  
		Last Modified: Tue, 03 Jun 2025 16:23:41 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd96e7c64ea0cd990e8b0a28cfafefa13e66d5770a6b4936f2be9253cf4028a`  
		Last Modified: Tue, 03 Jun 2025 16:23:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80e30ef682957a3d400e3cde48f2ba445546fe6d766b773fced5cff5cc0d584`  
		Last Modified: Tue, 03 Jun 2025 16:23:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:4420ad1d2cc33c840698e68eba16d59df4d23079db1a823d3190554adce826ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d235a4a034c854c1f1afba39ea87e6a6bb8556d36d3122f53e96399cdbf05ed4`

```dockerfile
```

-	Layers:
	-	`sha256:7ef6c92eff7f2075083657443152388b0e1d290e559404824f0a8cf72af0bd01`  
		Last Modified: Mon, 09 Jun 2025 09:44:31 GMT  
		Size: 36.6 KB (36640 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community`

```console
$ docker pull couchbase@sha256:48e35fcf9e73451a9526fd5697f879eed69bf9a9b62bec456bc7b074ea036de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:a465b4c12e610f072fd9838cb1df2ef084a21531ee48e8056e85534d8611598b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437367529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c95d88ccedd175a637eff7de500807beee1b9191fdf24506043834c693d01a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:48:47 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:48:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:48:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:48:47 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:48:47 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:48:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719b2d0f6e6600a5c02260fd376ba8f5e8eb14ac221831278ab240457e79ba18`  
		Last Modified: Thu, 12 Jun 2025 22:53:20 GMT  
		Size: 44.5 MB (44462800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e8abc0a604a00aa8b0ca3933bff077eff98a62c16be32f381edd1011734ad`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 877.8 KB (877846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2ed01b960a1385d9060ada80c03ffca841fe279ec57c0b17527e286dfbb37`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdb84b55eb00e5f4427e4f04a98a26d163ad8bb74aaa4ee48dee95e7ba64529`  
		Last Modified: Thu, 12 Jun 2025 23:33:03 GMT  
		Size: 362.3 MB (362304635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de830b84b0f72536fc94a2ebe23fdc73f9f03c46698f8390aa3ac5a7a142bf45`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd32a0a0ef72f57b36b0964340a1535cee8e4a114168b70c63ec501983c665`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73794f0e0dc14cff65f19ee795a9543c714e2007c2c9c75b84804c19e4529cb`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3367ce543f5bd3336152240754e4e757d5e8c12084562c147658b5dd52eee7c`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d6c241ef65284a7660d1df9e05cf2524397e2526dfdc4beb6371b8c8c3407`  
		Last Modified: Thu, 12 Jun 2025 22:53:20 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a4faf0c5f1c7e5f849554821b0b0b2b3f8af38d274cf279068abc83ac8004f`  
		Last Modified: Thu, 12 Jun 2025 22:53:20 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community` - unknown; unknown

```console
$ docker pull couchbase@sha256:9b4b9e574d7d1a10d45c5725beacf35c192f9882f815ac2c3c9653e6d69a63c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec44b1ac0cc4af95c76f991317231dc86fd196f913fb0cc12f78d760eb9cddc5`

```dockerfile
```

-	Layers:
	-	`sha256:8363411207df39d3da4df28b8caa481312f0fd5da40b92feb0236c449484d9c5`  
		Last Modified: Thu, 12 Jun 2025 23:32:39 GMT  
		Size: 37.6 KB (37562 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:529cadfa7f282a6f4209052573e37888b0f4e3d9ddb7af0f6d7818d969c158bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415466415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541fb5c6a463a41130bf4bad43e2d3370958137218ef8c73c2e4ffd0e48f92f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:48:47 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:48:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:48:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:48:47 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:48:47 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:48:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107df1885da6b3f0d704e6528f98f7fa3c94661b8f92990d84afdcb07a1bc0b`  
		Last Modified: Fri, 13 Jun 2025 00:12:58 GMT  
		Size: 44.3 MB (44276800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc711ea2f9a6417737f414cef7ac703989f3b88829d303e343141988a94d9f`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 765.0 KB (764954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83108333862d5447811f7b4d905a8b76f816da52e0f98cb855e702050111e57`  
		Last Modified: Fri, 13 Jun 2025 00:27:23 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127ae6f7bece4442cfb90a34e08dd7b86f0659245b4df43ae9ec21aec9da7218`  
		Last Modified: Fri, 13 Jun 2025 02:32:27 GMT  
		Size: 341.6 MB (341565849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf074eb0b15323eea4141088891e6f9264deb3a9bc93712fcf2382160fe7d59e`  
		Last Modified: Fri, 13 Jun 2025 00:27:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b545a3e97d88b6f5ae04ef927396e373e728f529f0d538618954c70381fdb5e`  
		Last Modified: Fri, 13 Jun 2025 00:27:28 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78e44756dc61413dc8dc073a7f922ee71067d7cedec59f8bee24eb574cb683`  
		Last Modified: Fri, 13 Jun 2025 00:27:30 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10d1da6ece402f8be63612fe5fd4f36d68514315ac22b2450dc8bb5bd64434b`  
		Last Modified: Fri, 13 Jun 2025 00:27:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747b2806c5c459f261703be62e9066f43fdf205b27150ca52c16335e2061fab1`  
		Last Modified: Fri, 13 Jun 2025 00:27:36 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c738c0e8ae9593cf9ebe0c476a62f14ab03e438963809be890fe44405040a0b`  
		Last Modified: Fri, 13 Jun 2025 00:27:39 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community` - unknown; unknown

```console
$ docker pull couchbase@sha256:e27e70edd5be21d9d9c66a4dfc1fb0bb0f44b2cdeed33e509d63134bafeecb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276f16eb921503fb8d69fcf3df04ce5d31bfa1f3a6fb8f2e7766f327c668707f`

```dockerfile
```

-	Layers:
	-	`sha256:d942961a411e25b77b2b048ee8bf6b3603e5a54c8c43fe5a0e9e0d098bd5fb16`  
		Last Modified: Fri, 13 Jun 2025 02:32:11 GMT  
		Size: 37.7 KB (37747 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.2.0`

```console
$ docker pull couchbase@sha256:84d404d1e25db14853a4ea25e370cb39d492a23e47b3a00c9bf15cac2ccc9fe4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:aa97c97854ec24464294c853574998868ac418f6f31e04ba3fed5b93ed79d88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.2 MB (392203771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6e06624ca0063dd3aa39aa933d3936338ca07e4fd927951bbad853d017ef3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:00:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:00:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:00:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:00:30 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:00:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:00:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948adea9c6e9887afd4a745b302ab5a64c689803527affa87d330f3668761ec4`  
		Last Modified: Thu, 12 Jun 2025 22:53:54 GMT  
		Size: 39.7 MB (39662183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37d469eed07bb6f18e14bda532d0d50327816da2b0ba25714ea0792b724a5a9`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 926.7 KB (926712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e529d7e0a21ccb91d13fd3e716b783f4bb49e47ba71d9635bff35c0394343f47`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c094bf4e449d4d24396fedae9bb0b5c2eaa0da5d46e7113bbbeff770bc353607`  
		Last Modified: Thu, 12 Jun 2025 23:33:26 GMT  
		Size: 322.1 MB (322076691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ada0f50a6f1bf9f95cf2b0a1d6c7e43714c8c2a7fe108f2233ff40f0b07321`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8861cc98a1c40b30cac2f74a24d67514a916b4a6bdbbe3582727c26c45510690`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f25c40f5d0ec1997030a7ca1d32fcfdd3e418ab1d5dfa5b0e0108245ff4e36`  
		Last Modified: Thu, 12 Jun 2025 22:53:54 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec366e3ad4f37bd70a69e1fdd84425b4589bed9214f5a15c3ed8295a55cfc4ba`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de59c0b13d14776da90abc23a4d4390fa346d7548fccf8a138a6188ce6f696b`  
		Last Modified: Thu, 12 Jun 2025 22:53:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4676b7734b33c165c9858d1434ef2c87085668c13b5048c99de6466ca24165`  
		Last Modified: Thu, 12 Jun 2025 22:53:54 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:86e06956d01757485c78d1ef3c0ec82071cdc7105fba4a609fd61ae4df961773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23a7539c830c15111ddaef4e7c41ce8cfa5e4887ab52e7c1139731d1892ce2f`

```dockerfile
```

-	Layers:
	-	`sha256:90f48e50b357a3ec27b0695a4de3011504cd78309853e25bc85d4d818e8f3e87`  
		Last Modified: Thu, 12 Jun 2025 23:32:15 GMT  
		Size: 37.3 KB (37252 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:04355630282b1f61ea0a9e03850948cb5c8135afcfb931f0530dbdd8a77abdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.5 MB (369463904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d60a4549feed2f97e172ec89eb8f098c3b9f5e1089bdce60645fc2b837ff4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:00:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:00:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:00:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:00:30 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:00:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:00:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f1a7d9cbd13dc9489ddbc0811761abd2ab8f494c7beea6c412c38bd2a317d7`  
		Last Modified: Fri, 13 Jun 2025 02:32:33 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c47ca088d1a7df0320133ee69da8881858859f7054b67d5fbd6141e9f6bf689`  
		Last Modified: Fri, 13 Jun 2025 02:32:46 GMT  
		Size: 302.1 MB (302125403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dad79c0aa1d4a1a9869d612c5599c57461904f0beb24bf87b1caeaa72990a3`  
		Last Modified: Fri, 13 Jun 2025 02:32:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec4d3e00e91ffc9950d626df8e09d1eaad8aeecd29dfdb5577379221f62403e`  
		Last Modified: Fri, 13 Jun 2025 02:32:33 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366dcd52a67f70ae9733927b3e8e343c25ca8fc2d1af519c3e218c83ac69f75a`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46556941a0bf13b36e28bfdcacbe30e872cdb2ea501f2aa15207f44450ca8f85`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8195c1aecf83d92580b76b5681c69377250a64c4622f0bfa8aaba88c36b1e186`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453f50bce8fb0b94d4d85059a6057d9e4d0443a41f60330a52b8d3f441a94a9b`  
		Last Modified: Fri, 13 Jun 2025 02:32:36 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:3b5f26466722aeb9ec479cb71d82e6ff7184dc45c2c75d38e60d9ea31c86d47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc084c62cf6bfeba02b9db6c53e08c90cbc812ab08b418b4c933d2fad957e2cb`

```dockerfile
```

-	Layers:
	-	`sha256:b173b3e09d397dc383b0c3fe7b6b6cf5ba27e492fc5b398d047b10952da74f4f`  
		Last Modified: Fri, 13 Jun 2025 02:32:17 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.2.2`

```console
$ docker pull couchbase@sha256:83fe6eaa5e8cef85899851e59c06222dccd798e1d6f6229b90e2a1da37240c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:149e6085d2406a9973ace9d1d4afb3dd2d1554e324d92a354adb61ad24974c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396697175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e69865502f4cda6841a1ca5687b8d6aeedca5eaec0d52316394adfc1d5b3faa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:35:23 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:35:23 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:35:23 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Thu, 12 Jun 2025 10:35:23 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:35:23 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:35:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:35:23 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:35:23 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:35:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e3a6631e57894a1c421de2e637e7f24489c04a6e5948cb75f5273ef57bd190`  
		Last Modified: Thu, 12 Jun 2025 22:53:39 GMT  
		Size: 39.7 MB (39661832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f351a55790e07ff75dc8d76201f7b57c08068e072b8378907db7c9ebc2c81b54`  
		Last Modified: Thu, 12 Jun 2025 22:53:39 GMT  
		Size: 926.7 KB (926731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fc9441290157b7c30765026d43b40e99c9cf299f38fb402d9ef2b04c5754ad`  
		Last Modified: Thu, 12 Jun 2025 22:53:39 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f5a041eb7fdc23b5865232072f0bdfe297c528fc5babe65b07456f6a77a75e`  
		Last Modified: Thu, 12 Jun 2025 23:33:00 GMT  
		Size: 326.6 MB (326570428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2553ad7cef9301c048388e9c0536fd87cb87f18cbf6e069e2a87a439848ae7`  
		Last Modified: Thu, 12 Jun 2025 22:53:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39270993daa999ac87c80adc2f5c23088750c4ab20d108615d61072ae7c63a`  
		Last Modified: Thu, 12 Jun 2025 22:53:39 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06db4d5e0eb9ea34f1bd5bb0247d8601811d5a0e6fef8084b94d89c7b4c6cf26`  
		Last Modified: Thu, 12 Jun 2025 22:53:39 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34c86deecb1ef3bd7762e82a0a026cc13e0655271478f1de9466cea68160bc0`  
		Last Modified: Thu, 12 Jun 2025 22:53:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7827b5916c229a8f83222cf00a5e36d67805d5a470748733515e8e76fc3564f5`  
		Last Modified: Thu, 12 Jun 2025 22:53:40 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9add43c4fae696f20ad685bd9ffc3306cbfcab18cd737b4aa91db3f2b37fce`  
		Last Modified: Thu, 12 Jun 2025 22:53:40 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:ae4b866c4154ae1ee466e543d7bb776df2807265919346ce8b2e1b8add8e769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982c45571339dc40c2796efb213dc4da23901b08f7805dcb3545c30fa1521094`

```dockerfile
```

-	Layers:
	-	`sha256:80eabb0e6ac3f86c98ad26157828a165c2027cfc678badee58f3175b5d5c74d7`  
		Last Modified: Thu, 12 Jun 2025 23:32:19 GMT  
		Size: 37.3 KB (37252 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:a8a18f219d98581437e83e8bbe4fc041300ce184f9dd47d2b9b3c62f174a16f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.1 MB (372076515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac5f396b427e901453f9685c83b956ba9b55bb8456b5fe78c4d12f8d2f82c03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:35:23 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:35:23 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:35:23 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Thu, 12 Jun 2025 10:35:23 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:35:23 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:35:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:35:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:35:23 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:35:23 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:35:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ac08d0b02fce56ea099487577951722debd0a378b57bb7e6efbe224f9a91e6`  
		Last Modified: Fri, 13 Jun 2025 01:18:04 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2ba6379e92e1474ce33f03902af489cb9181c8d9cc07aa0d7908ba48ebd430`  
		Last Modified: Fri, 13 Jun 2025 02:33:33 GMT  
		Size: 304.7 MB (304738015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cbef586541e31dcffee037625a70b3ccae62972e9b33a188e41a9b5cf1352b`  
		Last Modified: Fri, 13 Jun 2025 01:18:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e02e4f944f1c83555cc7c7d8d44a7490d6a3f781b466ea0c179be6564ffe641`  
		Last Modified: Fri, 13 Jun 2025 01:18:10 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd796d9fa2239687527cd296f47b2e73217086a13a933062dc714eb5203e386`  
		Last Modified: Fri, 13 Jun 2025 01:18:13 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003e2c5159325070842245859f4e18e5684aef234c9cdbdded489a6046e03e1`  
		Last Modified: Fri, 13 Jun 2025 01:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0618af1f72b821ea5df2814550b206957d8a57787942a81e1cfc942a99b68fe`  
		Last Modified: Fri, 13 Jun 2025 01:18:18 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11133b71999680bdf8b0379f3433ddc8e6bed734642686be39c679437d830ae1`  
		Last Modified: Fri, 13 Jun 2025 01:18:22 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:02063474db161580f8f47b0f89774c6c00e70f4885ac141afd89cda18f99f864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c043f9ba4a21cba9474141e042a95ae574a59d4554d33f4e54771699db1f628e`

```dockerfile
```

-	Layers:
	-	`sha256:293a9acbc9e6db049d95fd14ecc4fc0336b71cc85cc5fa7b0b8b7c9c558d9172`  
		Last Modified: Fri, 13 Jun 2025 02:32:21 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:a8b9c73893e0ea8e92c7572750cc72109699d679eed006f5619151e8d41fc739
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:1bb4113c68ac536fc0fccbb6d075ebf581e9f367f14e96a6c51f6f9212e3a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401235480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e5f097bb07985d17366bedd49780165e7edae103c1f8ce5b734a05c6538cf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:54:55 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:54:55 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:54:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:54:55 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:54:55 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:54:55 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afa078af841314ff548ba6e0cda8bbb83c389b01d91607b0f46921d1161a0a6`  
		Last Modified: Thu, 12 Jun 2025 22:53:34 GMT  
		Size: 39.7 MB (39662967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb2e9d71200b41ec8772e457447047b3e3eee1cbe8c58f73a51f0180dc34218`  
		Last Modified: Thu, 12 Jun 2025 22:53:34 GMT  
		Size: 926.7 KB (926680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb671a6ebd1f8cfbe7b2fa6251e8fad648723fd2de3066c7b21c3e954a55885c`  
		Last Modified: Thu, 12 Jun 2025 22:53:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff9fc089897c83480eb9a5aaaac75dcef0ab48cb8ef0bc3ef5463a61bc646a`  
		Last Modified: Thu, 12 Jun 2025 23:32:52 GMT  
		Size: 331.1 MB (331107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edd253a9fe4f87e84bee0e4af96829d587cb461684558bcf1fd4ea1e895738e`  
		Last Modified: Thu, 12 Jun 2025 22:53:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f0ee9e819f635c8012db6225821be48614b64c81b9e453c0e9072e3a0c0f2c`  
		Last Modified: Thu, 12 Jun 2025 22:53:33 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd333bf99cb3e0f907e7f2654e3a11570f31d41d339d6c098920c32a3e98a9fb`  
		Last Modified: Thu, 12 Jun 2025 22:53:33 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba246f4da36bdd9237ad37ad9ac91509883abf6896713844c960f7959fdebdad`  
		Last Modified: Thu, 12 Jun 2025 22:53:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a418d74445bb4e26ce3783bcf201bb85b48ec8069eb5a1fc8087b3f0244ed4be`  
		Last Modified: Thu, 12 Jun 2025 22:53:34 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc677471f0f056e9af64d9629051a57021fd998de85cc7c5d372bd1faf35bce7`  
		Last Modified: Thu, 12 Jun 2025 22:53:35 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:fc0a3a3f871070a557a9881e3c74b720d4c0941a2420d4771dc139c7689bdb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a0e765ba47c7c9327f762b09373c2d340bf86707e79db5fda9784b344c2bf3`

```dockerfile
```

-	Layers:
	-	`sha256:1138c0c933d303f9cda64d715ba8280596412b458d4539639bbf90cf50e270f3`  
		Last Modified: Thu, 12 Jun 2025 23:32:24 GMT  
		Size: 37.3 KB (37251 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:e152cb7a1284f16202dc9d27b02bcb3270c12b42e11d428e50fbbf500fd5aa75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380233983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ece4781bdfccc2c42a5f0f709bd3acd13374a2a668b2c7fd6615f7aae1891d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:54:55 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:54:55 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:54:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:54:55 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:54:55 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:54:55 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7225995e6aeda7d8d6cefa253946fca1cc19c902662fef5b83c27c174b915eb`  
		Last Modified: Fri, 13 Jun 2025 00:30:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2002eb07d8c90114647b848a21c510f729dec2f7706bdf6b70f3485850eabd4c`  
		Last Modified: Fri, 13 Jun 2025 02:32:42 GMT  
		Size: 312.9 MB (312895479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6db542afb8393e107b4ab249822f5331a12f788938bd8004893c4cf038b320`  
		Last Modified: Fri, 13 Jun 2025 00:30:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34077ce2382dcf6bc95910cb7e1e82ed9ff179fb36fead054aea964ff2b084`  
		Last Modified: Fri, 13 Jun 2025 00:30:59 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866e513f9aad45a061925cbccb5bb5f877c2c42e75e75fdefd829309da8e3faf`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bb8d3500f42272b9e328c05b264d1d8e892f016c9e371048ab4ee630e9c151`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10aa73de5fb85ebe122f78a6d6950040c56d47a768da20f88c958a88c4f5f4cb`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3b1ad9372cdc6b29918034eaf671b1c6e31b958aba3f4ecfa33cb3fc0b7aa9`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:23d73a089cef8800ca1c7888c00e11a98dac659acf67670f4bb66c677406c64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b385745c4bcfe82631c76ce3fb9b30e0d95fa249ff33a38b080f023e2cb442`

```dockerfile
```

-	Layers:
	-	`sha256:ae38743940edaa9a4f9b036dfbd3d09274b2710fee33e2c68f6e052b50792277`  
		Last Modified: Fri, 13 Jun 2025 02:32:27 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.6.0`

```console
$ docker pull couchbase@sha256:bd46dce15b21f00fd4dbf509a7751b62153f7fee7d7f9d5a51a53446fa4ded54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:6b07bc4d22080c3953d4f5978ec91ec6d22e23414a45096f9bec35f98a2ed919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (419960373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002d3ebfd8219fd2f0f2ccb8322ec2550ec2ede1003a6e26a40f40ff0ca4a6f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:31:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:31:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:31:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:31:30 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:31:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:31:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b03d98297cc38a443efd99f01320186009a5a295fa6c49cb246849feb35b70`  
		Last Modified: Thu, 12 Jun 2025 22:53:43 GMT  
		Size: 39.7 MB (39662185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea77eea3a30e2235dad6a616e8235fce75e4e562b0b54df3fd8ca74ed82585a`  
		Last Modified: Thu, 12 Jun 2025 22:53:28 GMT  
		Size: 926.7 KB (926677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e5752e35e7fc9e1127fec3d74e58a811d011d504410b5d2c61e72ab7f6488e`  
		Last Modified: Thu, 12 Jun 2025 22:53:29 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dec065f52fb6e81e3b2ddf0277c1e03b9726b6a673f9a95b0e8550f7cc53e6`  
		Last Modified: Thu, 12 Jun 2025 23:32:55 GMT  
		Size: 349.8 MB (349833336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ebac61a2a85b42389f2867163c7f70577b3bd34c57852176226c03be284a`  
		Last Modified: Thu, 12 Jun 2025 22:53:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8c95845b73bf6a2c43b56973cd31a3a49f355ce48e97d493936a1bf6d8abdf`  
		Last Modified: Thu, 12 Jun 2025 22:53:30 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d22ea1d9fba16d6c73adef07f8ddafbfc5b38f0d5afa162e9693b6d7876cd5`  
		Last Modified: Thu, 12 Jun 2025 22:53:30 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ecb2df0194a13004e032e0d793c1b36c9c560c40f044bf06e344a85003efcd`  
		Last Modified: Thu, 12 Jun 2025 22:53:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45454ed7c42a240fbd8bafcb746165c75c6e06830210c90d78d99a46ceaf403f`  
		Last Modified: Thu, 12 Jun 2025 22:53:31 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301379a5b8cda0e7d01d8ecfdb1645425e3835dd7f7c19959ec1391e88cbbb56`  
		Last Modified: Thu, 12 Jun 2025 22:53:31 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:0fcaf67706c9d72ff840c51cc421f94ff1b444b4b0f53b04436ca04dc34c2752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97cbd03c9ec274c864d85b1ff8b1bbee194ea4561e55335423cafdd009f86a3`

```dockerfile
```

-	Layers:
	-	`sha256:4b3817f4950ed4493f3b597b592e03056d421b2d330765f3869a1bf9d7952b41`  
		Last Modified: Thu, 12 Jun 2025 23:32:29 GMT  
		Size: 37.3 KB (37252 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:53c06ce187bc3c64d8a39fd1500204ac7d0a4bcb6d424c4a35db4222149397a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400708204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcde1835d6030e1bf5c96c13ee2373c208f36da31f760968a1aa163628e14e8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:31:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:31:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:31:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:31:30 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:31:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:31:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae30acbc3f8af9b40fe37c4226589be7f6bb56e244c0f5249677bcaa36a20b`  
		Last Modified: Fri, 13 Jun 2025 00:27:09 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2384be9b2669a53b8813eaa237221019c06b1fe04d1ae549814a8938ccfc10`  
		Last Modified: Fri, 13 Jun 2025 02:32:53 GMT  
		Size: 333.4 MB (333369702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6ebc92cefa1f6f63e2779b9d93a1a05ed09716b356c4e91b0dbd9299eea7c`  
		Last Modified: Fri, 13 Jun 2025 00:27:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab05a16a0abaab25102e554bdb02630e5bbc8dcaf837acd7fb213abcc102410`  
		Last Modified: Fri, 13 Jun 2025 00:27:13 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ecd8ccf6341c3d18a4642bdcae9d2e4a8ca0f77b95532ba1c82cfee4fd2e77`  
		Last Modified: Fri, 13 Jun 2025 00:27:16 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5a9faf88d0a1d13ad62584492a2142d554e57799dc9084a7e3ccad38cc7afc`  
		Last Modified: Fri, 13 Jun 2025 00:27:18 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e565fdf24e2569945e9ef1c04b41675d2d7ad75fd35558378a952dfcbb5b6ae`  
		Last Modified: Fri, 13 Jun 2025 00:27:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a327e18d69be829d0968738ece5eb97ab458bd9860c3b441d198c6cb90c971b`  
		Last Modified: Fri, 13 Jun 2025 00:27:24 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:08a3aa94b09be9d92bd1c9772dcbb9a17742ad407ec2493943380ebe22ec657e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3007f918fbae712b4d85a1ee2d2ac45a8666feb97c6072f687a9c05eb6dc798c`

```dockerfile
```

-	Layers:
	-	`sha256:ca0ff933b34f92c630e197259b8281954cb7ae9afbf3737b7de97e2f10715847`  
		Last Modified: Fri, 13 Jun 2025 02:32:31 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.6.1`

```console
$ docker pull couchbase@sha256:5966f0c2d321e8fa52ff42e4f8f30721d53213b2384574e7273aaa3363d7722d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:ae92eec50c8344eee9ec0ecd7b4d7407c36daafe3ca66ba5a0ae8f3b59581dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (419974142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94e6378527be12858e17f7781a9c4ba6bfe903fe875060d6c8a58fb8e65b9eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:40:31 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:40:31 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:40:31 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:40:31 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:40:31 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6ac01f224511bf7f1856637dd6b11b210101a6cc273fe9c0894f0e9109a98f`  
		Last Modified: Thu, 12 Jun 2025 22:53:43 GMT  
		Size: 39.7 MB (39662200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ca3aa854a62486cbeb88cbd68ec34e50336aed040ac992c14ad771275151b`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 926.7 KB (926674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253115d6642fe26b2dd6c76057db7d1492eb4ce70fb2333ec76976078d6c974f`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2bee851e7ecc10a5f4523300397da9badb6b5973db0745d2af56f3220d8c0`  
		Last Modified: Thu, 12 Jun 2025 23:32:59 GMT  
		Size: 349.8 MB (349847083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5991c11c75dfa100df22dfcaf93bda7cedf1a8cd4a849de820c6027684d059c`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be40716a5abe70a2c74d03a8d8bd6b0567561bdccf786f253ddb6823b4e0c1ab`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1927373b5e2edac1d3d394295ca2e42ce5e8dc38e488dc58fbb5073c141d0ffb`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7139af2cdd6430113123ca8cc20abdd252fc0c57d6de9b835ffb11d7f5b9a913`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd244474f66484c7bf389c7a384900ab2982f32710711e6b62c992b83b095a`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4790857e1cc2dad01c5da2bffd3d1dab5d6c2d096b70dec4545bc41e3b0d0f68`  
		Last Modified: Thu, 12 Jun 2025 22:53:42 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:bd00b7d93f6e7c8b11e84a8f1210d4a4af9495b961483989eb54bee943510972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5663061b70c75e0409411172fcfdd428553d25bd66898d20440d1d3c2cc484`

```dockerfile
```

-	Layers:
	-	`sha256:9d7812bf3466e8611e00395aafc1cf07b5eb7c2c364e3e1581ea4857af59b825`  
		Last Modified: Thu, 12 Jun 2025 23:32:34 GMT  
		Size: 37.3 KB (37252 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9736ccdcae9798fb3e4e1a91b9a159ee8ca4ac86edc039b58eb25944ee81ba84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400736273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e30e51e7989e40908b240818dddb6ffc0ae1376f870139c8c0acd7c8f3f7c76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:40:31 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:40:31 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:40:31 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:40:31 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:40:31 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae94a5889a1006ca13b7345f78dae66b03f64b5bb68bcf3b4f4c23200de8099c`  
		Last Modified: Fri, 13 Jun 2025 00:19:35 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93ee289ef8c4bcccca4a7a96166b515f9e9e1ad385ce00a1154201520c53f4d`  
		Last Modified: Fri, 13 Jun 2025 02:32:55 GMT  
		Size: 333.4 MB (333397767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1359acc2446940c6086e7f11af00269429ee617d6ca15dfb7b2ed416966dc25`  
		Last Modified: Fri, 13 Jun 2025 00:19:35 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a60a6fd5236bf39d4a98db56953554a570fb1651c39baee6088e592d7cf5c`  
		Last Modified: Fri, 13 Jun 2025 00:19:36 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75edc02e07c361185a3aac75108f68b7e8d0a2155cb3c95bd011d6bd68947d1`  
		Last Modified: Fri, 13 Jun 2025 00:19:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a692ada1b67452d038f3c9ed970db08e29cde99a7df2bd6b9459f127db5117`  
		Last Modified: Fri, 13 Jun 2025 00:19:36 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1475eccfc7472153d45c3cf039788fc6949644ec8b394e9d7111b51c4182a0`  
		Last Modified: Fri, 13 Jun 2025 00:19:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0b02c29e8aa2e383f15e4062b97700e7c10b2f5159845d7fb7ca7f965dc50`  
		Last Modified: Fri, 13 Jun 2025 00:19:37 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:7abaaebf365abac291e3483fd68312c032d147df22c81bd81bed6eeffcafe040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cd1aaa791c209c999627d508f55164ec00c505426213d52ceb62478876c347`

```dockerfile
```

-	Layers:
	-	`sha256:91fa887cb604e1474577160ee84af8cb22c8a9b4e966ef13eab0b5a870bacc5f`  
		Last Modified: Fri, 13 Jun 2025 02:32:39 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.6.2`

```console
$ docker pull couchbase@sha256:48e35fcf9e73451a9526fd5697f879eed69bf9a9b62bec456bc7b074ea036de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:a465b4c12e610f072fd9838cb1df2ef084a21531ee48e8056e85534d8611598b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437367529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c95d88ccedd175a637eff7de500807beee1b9191fdf24506043834c693d01a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:48:47 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:48:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:48:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:48:47 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:48:47 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:48:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719b2d0f6e6600a5c02260fd376ba8f5e8eb14ac221831278ab240457e79ba18`  
		Last Modified: Thu, 12 Jun 2025 22:53:20 GMT  
		Size: 44.5 MB (44462800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56e8abc0a604a00aa8b0ca3933bff077eff98a62c16be32f381edd1011734ad`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 877.8 KB (877846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2ed01b960a1385d9060ada80c03ffca841fe279ec57c0b17527e286dfbb37`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdb84b55eb00e5f4427e4f04a98a26d163ad8bb74aaa4ee48dee95e7ba64529`  
		Last Modified: Thu, 12 Jun 2025 23:33:03 GMT  
		Size: 362.3 MB (362304635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de830b84b0f72536fc94a2ebe23fdc73f9f03c46698f8390aa3ac5a7a142bf45`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd32a0a0ef72f57b36b0964340a1535cee8e4a114168b70c63ec501983c665`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73794f0e0dc14cff65f19ee795a9543c714e2007c2c9c75b84804c19e4529cb`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3367ce543f5bd3336152240754e4e757d5e8c12084562c147658b5dd52eee7c`  
		Last Modified: Thu, 12 Jun 2025 22:53:19 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d6c241ef65284a7660d1df9e05cf2524397e2526dfdc4beb6371b8c8c3407`  
		Last Modified: Thu, 12 Jun 2025 22:53:20 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a4faf0c5f1c7e5f849554821b0b0b2b3f8af38d274cf279068abc83ac8004f`  
		Last Modified: Thu, 12 Jun 2025 22:53:20 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:9b4b9e574d7d1a10d45c5725beacf35c192f9882f815ac2c3c9653e6d69a63c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec44b1ac0cc4af95c76f991317231dc86fd196f913fb0cc12f78d760eb9cddc5`

```dockerfile
```

-	Layers:
	-	`sha256:8363411207df39d3da4df28b8caa481312f0fd5da40b92feb0236c449484d9c5`  
		Last Modified: Thu, 12 Jun 2025 23:32:39 GMT  
		Size: 37.6 KB (37562 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:529cadfa7f282a6f4209052573e37888b0f4e3d9ddb7af0f6d7818d969c158bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415466415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541fb5c6a463a41130bf4bad43e2d3370958137218ef8c73c2e4ffd0e48f92f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:48:47 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:48:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:48:47 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:48:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:48:47 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:48:47 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:48:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107df1885da6b3f0d704e6528f98f7fa3c94661b8f92990d84afdcb07a1bc0b`  
		Last Modified: Fri, 13 Jun 2025 00:12:58 GMT  
		Size: 44.3 MB (44276800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc711ea2f9a6417737f414cef7ac703989f3b88829d303e343141988a94d9f`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 765.0 KB (764954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83108333862d5447811f7b4d905a8b76f816da52e0f98cb855e702050111e57`  
		Last Modified: Fri, 13 Jun 2025 00:27:23 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127ae6f7bece4442cfb90a34e08dd7b86f0659245b4df43ae9ec21aec9da7218`  
		Last Modified: Fri, 13 Jun 2025 02:32:27 GMT  
		Size: 341.6 MB (341565849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf074eb0b15323eea4141088891e6f9264deb3a9bc93712fcf2382160fe7d59e`  
		Last Modified: Fri, 13 Jun 2025 00:27:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b545a3e97d88b6f5ae04ef927396e373e728f529f0d538618954c70381fdb5e`  
		Last Modified: Fri, 13 Jun 2025 00:27:28 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c78e44756dc61413dc8dc073a7f922ee71067d7cedec59f8bee24eb574cb683`  
		Last Modified: Fri, 13 Jun 2025 00:27:30 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10d1da6ece402f8be63612fe5fd4f36d68514315ac22b2450dc8bb5bd64434b`  
		Last Modified: Fri, 13 Jun 2025 00:27:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747b2806c5c459f261703be62e9066f43fdf205b27150ca52c16335e2061fab1`  
		Last Modified: Fri, 13 Jun 2025 00:27:36 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c738c0e8ae9593cf9ebe0c476a62f14ab03e438963809be890fe44405040a0b`  
		Last Modified: Fri, 13 Jun 2025 00:27:39 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:e27e70edd5be21d9d9c66a4dfc1fb0bb0f44b2cdeed33e509d63134bafeecb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276f16eb921503fb8d69fcf3df04ce5d31bfa1f3a6fb8f2e7766f327c668707f`

```dockerfile
```

-	Layers:
	-	`sha256:d942961a411e25b77b2b048ee8bf6b3603e5a54c8c43fe5a0e9e0d098bd5fb16`  
		Last Modified: Fri, 13 Jun 2025 02:32:11 GMT  
		Size: 37.7 KB (37747 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:ed940813ca0f960529d855c742f4372df0e88b0ade7c0679627878e42b6c4924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:813b49e0ef39898d3faebf195415d335281419b36e9e91bf735b5f7e343bd056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.7 MB (794747783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ffca8857d13518cb9908e5b399639ad3252e6a8cedbfbdbd81ae23dde24b27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c3b3cacce9f37e529d00643dc6a7356b93b7d570405de6a0c61641956cbc26`  
		Last Modified: Tue, 03 Jun 2025 14:07:29 GMT  
		Size: 39.3 MB (39303163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dda7d77f72011a4ebf049e73e839994a45f1e0354ec21466733d34be426f15`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 926.6 KB (926575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf7924979a5479a138d955d08a263461036a06e7ae36502d75c3c538b2ceb3`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0988595feb9082d9db0ef1f794d362bafef150552c279ccbef7d19658e7245`  
		Last Modified: Tue, 03 Jun 2025 14:08:18 GMT  
		Size: 725.0 MB (724979867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b1e063f9f2404c773cd3c78b32f368fa15f399dc40dfb9f672cf164f335f1a`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bea16e78db287004b1ad579baf90c6b57e09cf51ddc0d96a0310218cd724e1b`  
		Last Modified: Tue, 03 Jun 2025 14:07:23 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2709a0a231e86cd0d2106017eb8e7f72cd40b9437fa35ee1d4b905ccb449ea8`  
		Last Modified: Tue, 03 Jun 2025 14:07:23 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082fb5c7ef2892c9a9fe0f11aa63bcdb5f588076c0cc5d8f95ecfa7aebe54ebc`  
		Last Modified: Tue, 03 Jun 2025 14:07:24 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254548277f51a3a7ba0b0bb147b391c1bbb5c6d00278719e96c50b077a7401b4`  
		Last Modified: Tue, 03 Jun 2025 14:07:24 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124a32eeb718d8c54c6f29c2cfc25b213993e9c7c18a2aa9f78a6fc3406b8c8`  
		Last Modified: Tue, 03 Jun 2025 14:07:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:1daaa4381959c4b4ad2f72a92916db538dbbaa3abec64a39c63885b05dfd0d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15a75a67b82da4a16cbe101895e937cee932dc19cff9438f2168fbc00d96b39`

```dockerfile
```

-	Layers:
	-	`sha256:33308da65b82e8843d44557e4599ddcc303a72f6765b43c1b91b30528910a4f5`  
		Last Modified: Mon, 09 Jun 2025 09:43:47 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:98e455037d80a274b6cd74cd39f5af3e415f82701681c0bec5e79741e3870fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.4 MB (763408090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248c506b8cd15abac9233058c8c0eb3b712c0cb0af360622488f453792122ef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffde452cdb09fa506c9cb01e48875a79d2ded94d9d6ddd3f83c385acea1eb61`  
		Last Modified: Tue, 03 Jun 2025 16:23:38 GMT  
		Size: 38.8 MB (38849499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c55621952ece84f3edc704718bb4859c7e103a8964f6844479de0c663696207`  
		Last Modified: Tue, 03 Jun 2025 16:23:36 GMT  
		Size: 770.8 KB (770806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9129adffdc0253ebbaaf1fb32ef66c49ad8caae70fabd05c02f825d48b70a3`  
		Last Modified: Tue, 03 Jun 2025 16:23:37 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c25687cb69cd4f05d93b1b6b36d4e2ae9b3ec616d633182a417b035ec7587d`  
		Last Modified: Tue, 03 Jun 2025 16:23:47 GMT  
		Size: 696.4 MB (696427022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2472d3bcb419b1c988d37f3335bca984f97e4761e92591bbd90cd6c310c3ec0`  
		Last Modified: Tue, 03 Jun 2025 16:23:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86103da5720e37d892f6759b260e4e107cc473a6bdb28fd91e56fd9c0874ec`  
		Last Modified: Tue, 03 Jun 2025 16:23:40 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb1c195d48e7e38da8cf8ed94d652eac554674f4dd6a11e3b3f5e2a5638e5f`  
		Last Modified: Tue, 03 Jun 2025 16:23:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245cae7b9c382625baa4aa92f8cbad7a51be6eeb8699cb27fdea759f77a321b7`  
		Last Modified: Tue, 03 Jun 2025 16:23:41 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd96e7c64ea0cd990e8b0a28cfafefa13e66d5770a6b4936f2be9253cf4028a`  
		Last Modified: Tue, 03 Jun 2025 16:23:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80e30ef682957a3d400e3cde48f2ba445546fe6d766b773fced5cff5cc0d584`  
		Last Modified: Tue, 03 Jun 2025 16:23:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:4420ad1d2cc33c840698e68eba16d59df4d23079db1a823d3190554adce826ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d235a4a034c854c1f1afba39ea87e6a6bb8556d36d3122f53e96399cdbf05ed4`

```dockerfile
```

-	Layers:
	-	`sha256:7ef6c92eff7f2075083657443152388b0e1d290e559404824f0a8cf72af0bd01`  
		Last Modified: Mon, 09 Jun 2025 09:44:31 GMT  
		Size: 36.6 KB (36640 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.2.0`

```console
$ docker pull couchbase@sha256:5903fbd69888f93c4e30651d4cdf027e58eb6a14e2e339c32f89ccfab2d67e10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:31f88212bceb31fad149a4ee4054bd7a6ffdedb50a839290a6633e15c7ae3b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.8 MB (698757280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50849322570fae9771a13f147ca945000fe7b3b38304065fe2049f293dd1eb57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:23:17 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:23:17 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:23:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=b44a4d8e577613ad027dbac9830e6123deb7bda22facefe687d6b6e98c86ac66            ;;          'amd64')            CB_SHA256=2fd31b46a6df5ed9c85d3a6cadfb0214e3f928c14ff0b03e6a24652700128328            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:23:17 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:23:17 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:23:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc07d2a16bf1e0137d7d77f6eb59d22890f7e9dcd4bdbd1ec051c27b67aa0d`  
		Last Modified: Thu, 12 Jun 2025 22:54:25 GMT  
		Size: 39.7 MB (39663052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399f8bb9e64b1b0321b2f53a1db86a12287c0bef4ba447710cecd24286701c16`  
		Last Modified: Thu, 12 Jun 2025 22:54:23 GMT  
		Size: 926.7 KB (926735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0dc39fbb9a867beade04f06e2cc150de4bbbbb0b2844407479f8f2ed1ca79e`  
		Last Modified: Thu, 12 Jun 2025 22:54:23 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dd0ac1184b561d815a9953efc83829d67d584575af81793890e011acdcdf72`  
		Last Modified: Thu, 12 Jun 2025 23:31:50 GMT  
		Size: 628.6 MB (628629308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd4c2dce965d4648509cf2e03d3a9b30c33e79d40e8210eaaf08250123a63da`  
		Last Modified: Thu, 12 Jun 2025 22:54:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3056f8515988a338339951438cbd7ae7c24261d04eb6fa5e096ac9ddfc5f19`  
		Last Modified: Thu, 12 Jun 2025 22:54:23 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83519ace6d1861c8ad3ee0fe6c437da8084fbe5e0d842c71fab653a16ad903a4`  
		Last Modified: Thu, 12 Jun 2025 22:54:24 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02bed1bcd48eb6123ffbf42969b31630aeb92a29270dd06dd40185bf64209f3`  
		Last Modified: Thu, 12 Jun 2025 22:54:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de802a1c967cd99c41cd12b7ce383dc6e74e7c727397e4bf6e767a030373ac0`  
		Last Modified: Thu, 12 Jun 2025 22:54:24 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9add43c4fae696f20ad685bd9ffc3306cbfcab18cd737b4aa91db3f2b37fce`  
		Last Modified: Thu, 12 Jun 2025 22:53:40 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:e0871753bc0f82b84ce35c0fe3d670f4384a1f8c6304433c772b33a952abbff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e44397b7ab2d39b3a87471f4869554b5012ec813de86b35342b1ed12f4804ef`

```dockerfile
```

-	Layers:
	-	`sha256:d73250c7c6746e800b969548d9c9ec657458595d975011eabfb1a77f0a38316d`  
		Last Modified: Thu, 12 Jun 2025 23:31:19 GMT  
		Size: 37.6 KB (37564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:19e4731c7fc0bf9b784e5649eef54d7c7627111bf22d2a2d68875f116c22f2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.6 MB (670589921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9b8b4d060e236c19415d44b751093d96f1ab4feb1d6f4eab3cf3fa3de1aedf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:23:17 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:23:17 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:23:17 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:23:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=b44a4d8e577613ad027dbac9830e6123deb7bda22facefe687d6b6e98c86ac66            ;;          'amd64')            CB_SHA256=2fd31b46a6df5ed9c85d3a6cadfb0214e3f928c14ff0b03e6a24652700128328            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:23:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:23:17 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:23:17 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:23:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e6a2429701c4282f51b3d41383366f0e0e9478774dcf1548795cd1503d09c`  
		Last Modified: Fri, 13 Jun 2025 00:37:49 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a4284e8f893f30000e9945d7f0f12f3bf73edf168be902b77483663725f87a`  
		Last Modified: Fri, 13 Jun 2025 02:31:55 GMT  
		Size: 603.3 MB (603251419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202962f366f1c09efd638bde89504c0a186539fc545d4aad32bd3c0ca26e682d`  
		Last Modified: Fri, 13 Jun 2025 00:37:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ddf16aec84e5a570869254dd33a78289ecabe8147264fa5f84572ef58a5275`  
		Last Modified: Fri, 13 Jun 2025 00:37:49 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf927e6bb267bd0019abcc802c82853fac854a0a65b3758f2c68804fa5ff38`  
		Last Modified: Fri, 13 Jun 2025 00:37:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd4c8ca44a9f0a4049875b9f507704670e6c85ebf6393b3826e43205cfd9750`  
		Last Modified: Fri, 13 Jun 2025 00:37:51 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32191ea4d2ab2d929c82de5a66ac0a34a945835d9caed7faf11c49a65f04876`  
		Last Modified: Fri, 13 Jun 2025 00:37:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d886b2fe8965d7f67d3b2bd1e2f1f0c55d56878d0c45fcb93b08fc9b9f0bbb0`  
		Last Modified: Fri, 13 Jun 2025 00:37:51 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:9bca4527c87a69dab17ffb14a0fd23fd6146dd7aaeaeefe622c0a5637ca4a581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f1116659811c1e9960737da2b9c38c648587643d8ae3b0546eceacbec58541`

```dockerfile
```

-	Layers:
	-	`sha256:d93c696fa04f4fa167fddbdeb06bbcac20dab59dd10091edc8b3f2cb5929ea7a`  
		Last Modified: Fri, 13 Jun 2025 02:31:20 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.2.2`

```console
$ docker pull couchbase@sha256:8fa3a7d527f44c905cf8814cd979cc72ddbc00af175e1c03f4cf24cecbc35916
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:a19ec58565546640ce8da4ac8b0e0497d40eaf4ecb5b88bc9d05633bc4d6989c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.9 MB (703930557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4138389afc9331760e16d223619951f7ee9e35b71c2908426c0c75c61183233c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:32:06 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:32:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:32:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:32:06 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:32:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:32:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f107907d53e2361344dfc4357ed319d478ba4b6f9887ee23afba17e518916eed`  
		Last Modified: Thu, 12 Jun 2025 22:54:44 GMT  
		Size: 39.7 MB (39662068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabaa524eb5ff279a762749c414210ccc99844adc93606e3c015527962f0ac10`  
		Last Modified: Thu, 12 Jun 2025 22:54:42 GMT  
		Size: 926.7 KB (926688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7c0fb24f91c6cc3996a50c59d93f19a70ba469f8880e388fa76bc1f39f859`  
		Last Modified: Thu, 12 Jun 2025 22:54:42 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ba7cab0bd2d2e1c28b5ce8a2505a30d64515b1d87bd6ba4f7fe0bcba74d3ef`  
		Last Modified: Thu, 12 Jun 2025 23:32:30 GMT  
		Size: 633.8 MB (633803620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0a628e0db4d8c44f66fd8747a09914ffe9d6cb37ed6e56d9239090edae5c52`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bed21221646d551c31846945d48cb58743f3bb6eee0c86479df6c7ed90c280`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80478c4edacff4457e1dd268637ef6815d811ef0758eda8036ff2d4e798f6839`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec7c0dfcc59e9a3413516b8adfb4b0ff66c88d423be768c31104bee25efbbf0`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843f0de77d8204f29306599e736b20ed821768ba72baf61618faf7df519008f6`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fc1d36fa5094a22cf3d3ba7f00b59dd9a7a347b4d4bf9ce9f1e023ef56592a`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:bff2c164c8649a3eb3302805491042c3fff28f9e85ccb626d72107457077fc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63800db6e89a8e49a61f95f5c865d8200ad220f377af01ac3248c614af1553a`

```dockerfile
```

-	Layers:
	-	`sha256:3f06e294a709aca3d5765f412553f9225c8c17dc5225dc7bf12fd0aa15b23a3f`  
		Last Modified: Thu, 12 Jun 2025 23:31:24 GMT  
		Size: 37.6 KB (37564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:69cb59a0585d6fc61cc8432c6575bcb8045615d2079a557c233757a55ab0bfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.2 MB (674187907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e032e0f3158bb51e95e910074122a2cb9e38a330302b3b6c539d4d42839d7901`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:32:06 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:32:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:32:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:32:06 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:32:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:32:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880c8d6ebca9e0e7c4d467d832f4b1d938f72516eb584d074f42f0b8f45680f4`  
		Last Modified: Fri, 13 Jun 2025 00:34:32 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc7ee46123cebee8a6bb90ca9c58c0de87fd6f25263de693ad44cf17ef1f3ba`  
		Last Modified: Fri, 13 Jun 2025 02:31:46 GMT  
		Size: 606.8 MB (606849403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64658e2dc30c74c06bbe96a5c5fd241d93456d8b726c936b7f9e7ca6c7b8f09`  
		Last Modified: Fri, 13 Jun 2025 00:34:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7bc1f28314c75409c3d28bc791fb6cc221ddbd1250831cffe947fc4d364a43`  
		Last Modified: Fri, 13 Jun 2025 00:34:33 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f6ebe51b1da8caec5732f4de23ebda30d137f9967d5c3feed8e01413b7a1a0`  
		Last Modified: Fri, 13 Jun 2025 00:34:33 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0658dbcc92c8ac5e3947cd8c7378a559753835ceda224080c04ede07898d61e2`  
		Last Modified: Fri, 13 Jun 2025 00:34:34 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c1e02c7d88ca7164d6154a6ce2ac4ce4f394fc41cd899189494b618c26b08a`  
		Last Modified: Fri, 13 Jun 2025 00:34:34 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613317a29d35bbf6faa4a5f65cc11fc68bbf95d194b15c4bd1993dc022169d95`  
		Last Modified: Fri, 13 Jun 2025 00:34:34 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:009649c3d3b88b6065017755213d92b937fbcd28937a202828f0653ea7a47c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39e434665044faa844699cf8bc9742608f68068db63844fb5c8b4743121426f`

```dockerfile
```

-	Layers:
	-	`sha256:b26f3122fba0af356d59af6cd73e4225c4a537cafa5729c03a10175e013d1535`  
		Last Modified: Fri, 13 Jun 2025 02:31:25 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.2.3`

```console
$ docker pull couchbase@sha256:550275517f9d321fcb70440250be1fb2a71ba7658657259ec49a7f4f0cdec43c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.3` - linux; amd64

```console
$ docker pull couchbase@sha256:b9c4574fd7e2dc46d0c7cd70f79c468215b4ede7f9d3c9dee6640d76cbe04e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.1 MB (705089528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fb79c0ed302f92da770cfc314d25e048162c2d369834c30ac23ba3ba98c9a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:43:25 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:43:25 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:43:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:43:25 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:43:25 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:43:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada5f9d92ce31847d28cc65155b4d53cd20e2f0feb5a9d5e50c19c8ea9f04de5`  
		Last Modified: Thu, 12 Jun 2025 22:54:18 GMT  
		Size: 39.7 MB (39662267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f314f9540cb794c1c6d458e1c5f696fe026d2d715097c190b30e7656707201`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 926.7 KB (926685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054899b4bd44e21e80a0d93a198b3bcacf9adf41b06c62539f375563dd1f5bb0`  
		Last Modified: Thu, 12 Jun 2025 22:54:15 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f52c53be83b3e824a8be981e1c5c25afe66afcb330385e6e51d05e5f57b0815`  
		Last Modified: Thu, 12 Jun 2025 23:31:52 GMT  
		Size: 635.0 MB (634962399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3c64516be992ab915a2c3d74b9b27bd3249fe30e76b4d6a2799b81b786338`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd47933b20250284cae5e8a1e485588451b695747dfb1dcfc50aecf9955648df`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b75ced0b490b0ca997a028238b3eac14b014f850a60efd2be72f8eecfc03ff9`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35357947bdb507a86a00385bb50c039cb291f15813b89c22aec603cdd030ea4a`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e84b08a01e1e97c41c412010ef812dca02afcb323749f13edaf66bf3dec69`  
		Last Modified: Thu, 12 Jun 2025 22:54:17 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0837de8b7a88598dcb5ba1b9c4fe396fc7f9a57a1ade64fb0c33bcc6af6797`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:7517f8c9972ae7994bcf9c8182617637ecb8d0c77d8374d154126cde2a74dffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7281b0cab61409727f7dbface688f9f01e5bc2dcc2a9ef911b73b58baa9df917`

```dockerfile
```

-	Layers:
	-	`sha256:7f669c94346a931f2e501b4241623e529f92e7d6c0865efee5baa5636a5d5876`  
		Last Modified: Thu, 12 Jun 2025 23:31:29 GMT  
		Size: 37.6 KB (37564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:835ef4188c9e1cc3cb06b1e65bc042720c185f17dbb75cc2b867bdaddcd0ed65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.3 MB (675253927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ce254586553c6c98f546f193c1626ad9f359c108fc052c57c1ff90da8ee4d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:43:25 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:43:25 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:43:25 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:43:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:43:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:43:25 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:43:25 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:43:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be109c36b0e255091c2d780f7db672d5b6fc8fe0f7ab9164e258a5f446a91bcd`  
		Last Modified: Fri, 13 Jun 2025 00:32:48 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e70616205835ea0633debc70736ee3d01a7fe72d43013c46e7811967538780`  
		Last Modified: Fri, 13 Jun 2025 02:31:55 GMT  
		Size: 607.9 MB (607915424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0e08cbe2004368f4d8974246897045bd6d8761c127a063fbeb5f568272a598`  
		Last Modified: Fri, 13 Jun 2025 00:32:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fe7d1528be1bf0b503995df2ab0a8eb29a4cccea314a6dd14744210673e3d8`  
		Last Modified: Fri, 13 Jun 2025 00:32:49 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f146aceda8052a9f8409d6374ed514f1d53fc46448e8db4632d64f11df9083f9`  
		Last Modified: Fri, 13 Jun 2025 00:32:49 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8a3feab1251e318361368d25badd5dc0cad00bfecccaa6d0c046ffb3f0172b`  
		Last Modified: Fri, 13 Jun 2025 00:32:50 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee224b845d5d87f19370b3f0e7ec67a4ab798d5b4ad9b8e41d5e81fe3146013b`  
		Last Modified: Fri, 13 Jun 2025 00:32:50 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7d4a1d12267d591c99b9fa616589b9730f0ec09926bc0eacebf7d172040b42`  
		Last Modified: Fri, 13 Jun 2025 00:32:50 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:c30d945c5f67530a7627ed709594297971de2fa94f6962224c2a5296bc94de43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de65943784d2b98ee26854777d127dffec7fee01c275f2db70cd304c0a6c0141`

```dockerfile
```

-	Layers:
	-	`sha256:921f03453f34a3761df8e54f39847677821e4cb28ccbd7d4129675842ba8f277`  
		Last Modified: Fri, 13 Jun 2025 02:31:30 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.2.4`

```console
$ docker pull couchbase@sha256:774bd2b4bf41c702c65f084f4f670e97a4b781315051687e575b0ab29f8001a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:f7f16ac118809c4f8a10b20345a8caa4a052c26326b5ff8abd882c8abca2e46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.8 MB (675793697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776a783f098ead05ee73fdcc18d992e66d5b626933ec029c4afaed371409d74f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:50:29 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:50:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:50:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c675d9e2a355cca833c9c12f85585e92a4d1cd95858d79e958b507f9ba1a4349            ;;          'amd64')            CB_SHA256=0f5edf6c011df25e172ae54c6bbe5f83be6a3c24e4e23b25e77d5079262c30ca            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:50:29 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:50:29 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:50:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f4a1a05bd5e8ab1925e2531c695347c04cc0bed559a2fe2aa59de644fc21a`  
		Last Modified: Thu, 12 Jun 2025 22:54:21 GMT  
		Size: 39.7 MB (39661582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08ffc457d1e7964b3047bb444141afe1fcf9b17f9b65a23b8355691f5cc717f`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 926.7 KB (926717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807b824192ab90051a1350760e8290d36d293c7929e2340056f8d8d1ede213c0`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4f33dd97ad1a831264c25619854d00b047def12c8a15fe532b4b93a7c13d7f`  
		Last Modified: Thu, 12 Jun 2025 23:32:49 GMT  
		Size: 605.7 MB (605667215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9d628d1fccc94e229852442cbf7b76fc43606526be191d9a30a2b1b2f4e3ad`  
		Last Modified: Thu, 12 Jun 2025 22:54:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec373d2b6db9e083cdc0206e441423a547bfd02603db62a0b405f92fae7b4790`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba056eb399368f8df6abca629cfa9e7c8eb6125b3af12c4592e8a193ca8781b4`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f145641e3cc3822389c3e05dac06116dc5dae92c781a70eb4cce7e330ad410`  
		Last Modified: Thu, 12 Jun 2025 22:54:20 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d9b5e2fa4b6458fd448b043e779225ebb78095d0758e2a6c1684a9e4d9ba9`  
		Last Modified: Thu, 12 Jun 2025 22:54:21 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0837de8b7a88598dcb5ba1b9c4fe396fc7f9a57a1ade64fb0c33bcc6af6797`  
		Last Modified: Thu, 12 Jun 2025 22:54:16 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:9a6b939d937491150a341383da6d4f028885a79928a73c3c4af7e2c17ed5cc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c1f8b6cbdde81dab7c8fcb898acbf496927dd6922c10776128be7f4393be9a`

```dockerfile
```

-	Layers:
	-	`sha256:76f2699312d87698b3674d6091a7082b24bd3bab904fa82c91076b12f70c91d1`  
		Last Modified: Thu, 12 Jun 2025 23:31:34 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:5792ab3afa35ed4e807c300a3608c4d8550e026e333c70ebbb263400da20231b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.7 MB (649745090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dd259c4a7b6388c3c3ca68e804d50e8e1a217591615407170b715c4a78225b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:50:29 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:50:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:50:29 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:50:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c675d9e2a355cca833c9c12f85585e92a4d1cd95858d79e958b507f9ba1a4349            ;;          'amd64')            CB_SHA256=0f5edf6c011df25e172ae54c6bbe5f83be6a3c24e4e23b25e77d5079262c30ca            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:50:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:50:29 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:50:29 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:50:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4280655c3ce47770e575d428dff5ba5cdd53d48c389eb4ba18fe4950c6a404b`  
		Last Modified: Fri, 13 Jun 2025 00:29:43 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a8b0b3dc230785bbef0f2886729f0f68729b71bfe5069c99dde096adf7affc`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 582.4 MB (582406589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97836be91af5aee9698364a4fad3fa9f65fe65d4bd38424913f722fe8a1213ba`  
		Last Modified: Fri, 13 Jun 2025 00:29:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1b9abb614800a250234bfa8ceb39021077c57e3103e19684dedd705ac4680a`  
		Last Modified: Fri, 13 Jun 2025 00:29:43 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fba3cad805715f80566d8b56d1d5f5029be0cc5319ce9c077dbe615f784e06`  
		Last Modified: Fri, 13 Jun 2025 00:29:44 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eb118d2535fa9ab96c9e9970001de0a7df37c2aedee1c930c42dc80c37465f`  
		Last Modified: Fri, 13 Jun 2025 00:29:44 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518d49e34717ea6a7c01c0e9e4e2ebea6ec73a369b84a8e1d29542ca9e142bff`  
		Last Modified: Fri, 13 Jun 2025 00:29:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e92531b82f1c31f3c3b00dfbd685be2b91332f556e268541986c903999a47ac`  
		Last Modified: Fri, 13 Jun 2025 00:29:45 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:1117a0f938cb2f7c92d023f344aefc7d1df75423074fbd23ae62f3c8f3e3ba2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91eac438b40af1b0f4b0215c7586777c2305858a300342389c7c3ec33418dc1`

```dockerfile
```

-	Layers:
	-	`sha256:76fdd5aebb347ec4ab0b42be59fcba0d943574d14fcf334889b5103982707738`  
		Last Modified: Fri, 13 Jun 2025 02:31:36 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.2.5`

```console
$ docker pull couchbase@sha256:d174c71343bbdb954628bec9a74f3e37a2c9198e8b3dc9bad50478030846fc46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.5` - linux; amd64

```console
$ docker pull couchbase@sha256:56678afa56e7da69f4cf4d476489f6ebc22a15e519b7c3e4393249db566cc4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678279523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9f675fee53eaf67aead3b22c0d18a97b7ed7e3ac16629537286fe53297e948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:00:36 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:00:36 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:00:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:00:36 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:00:36 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:00:36 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259d186a8bdd83bb89e0d444cb03b56a1e25bf56ed2e496d40195fca06f8bae8`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 39.7 MB (39661916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b258415211893d2d2e0d02a524af2a738b49a7303359fa172238f36f177d4cb`  
		Last Modified: Thu, 12 Jun 2025 22:54:11 GMT  
		Size: 926.7 KB (926716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b4ef514e0271d07ba46219bd0e07151c260af86c0d717e6c5f6c196c46c12`  
		Last Modified: Thu, 12 Jun 2025 22:54:11 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b296622690961c3f744e23d8266f8d62a8c80c107d39997a6f0aa41eb81f2f7f`  
		Last Modified: Thu, 12 Jun 2025 23:32:48 GMT  
		Size: 608.2 MB (608152710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969f38e48ae02d2fe72e25a676365cae707fbb75291516fe090cfa3e8c411e6`  
		Last Modified: Thu, 12 Jun 2025 22:54:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbbdf3feb1c0617158ded53b7fa2aa3574ce4a294dc996fd17d62f3fcbde744`  
		Last Modified: Thu, 12 Jun 2025 22:54:11 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dd91a1307cb8b92c952790b18e9bf4138e9eeaca97a26ead9f3ae47ffd6aba`  
		Last Modified: Thu, 12 Jun 2025 22:54:12 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42c96e2aaf713fa9e532fce9973aee27509f6c51f4d5c0452eb56f148885443`  
		Last Modified: Thu, 12 Jun 2025 22:54:12 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255a8d83296df84ea1e84b47617c0b9bbb41d3ecf32f110e7035a1ee18eb8cd`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c3ae3afe347e85a46598fd71f89156b61f6518b159107365db731dedcf00f`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:803599731311bff99da51b127a742301f6c6bb6b6432d497c8d55ce04b090987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4366bf0a6162c7782a626e3b7ae3f47b7f52bea2c9dcc03931248bfe99a1b8`

```dockerfile
```

-	Layers:
	-	`sha256:6cad51b844d2f9117f9b29cb970a1aa66c20bf8a1de146a302e25ce9a663ca58`  
		Last Modified: Thu, 12 Jun 2025 23:31:37 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9956f793cc285b892120ffaaef4b0674486986839bc205bfbc9b26e3afc76af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.8 MB (652756203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e996757cf2f5c835b76636ac79ec65b13a23b29d813499b0a6b63f4007ea47a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:00:36 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:00:36 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:00:36 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:00:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:00:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:00:36 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:00:36 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:00:36 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d58a1caf4430f01f3389631ea92dce68c0a7af74e66486367affad12ccaa3d`  
		Last Modified: Fri, 13 Jun 2025 02:31:47 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527e3853254046d9e3058ca7cc0d785216e5ef80a2d9520fca1ab6e51cd1ea96`  
		Last Modified: Fri, 13 Jun 2025 02:32:03 GMT  
		Size: 585.4 MB (585417706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bd09b87be592878f22afbd2557b25d8e379bec0f3d8b5439e6c3c6058176da`  
		Last Modified: Fri, 13 Jun 2025 02:31:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024bb0ad9203da930466096a81737cd1f6b41db672a2d1fe5587ec58da33bcb`  
		Last Modified: Fri, 13 Jun 2025 02:31:47 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a796ec98540c8a5c9fe97aa52546d18d70419ba6e3cf59c20f1735c1a81709d`  
		Last Modified: Fri, 13 Jun 2025 02:31:48 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55268ffa42bac369cdb34ebeae96d03e168ea91d1594454b2f31023c3a44ef73`  
		Last Modified: Fri, 13 Jun 2025 02:31:48 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433b82c078a32135e74a6aaf4c5629dc411fd704957480ae1a45023010d9d036`  
		Last Modified: Fri, 13 Jun 2025 02:31:48 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560bd650008423fd05009af2592dfcbe053ee5cd8b375f2d0bb21cd0911399e0`  
		Last Modified: Fri, 13 Jun 2025 02:31:48 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:ecc07ddba6315269ebb5b9da50afa0d25260c1a8ce089a227b6852de6bec50bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a4a65a47a93213b385f5a244f0bab47cc77c75f72efd2b7ea60fe3b596aa63`

```dockerfile
```

-	Layers:
	-	`sha256:4b81e96754f1bc8b1b3d50f95120e8fe6652fb52a08459ec4d0fdd6bd4fba397`  
		Last Modified: Fri, 13 Jun 2025 02:31:40 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.2.6`

```console
$ docker pull couchbase@sha256:3fd8451d44022d9f59ee18ed378ca550d30c292b98ef3571a796d37cc2f592e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.6` - linux; amd64

```console
$ docker pull couchbase@sha256:742742c2b9462ff5228bd6b543c73a5228def3131c68084ee3ce57255ca480be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.7 MB (690668356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff663744ea006c54fb586c0520424611bf4d66992aae61c30c96aafe101ed29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:07:10 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:07:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:07:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:07:10 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:07:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:07:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6342502ed45c496fc9a772bf28dce27961b7f3f260815b8c9bc998c905ed0949`  
		Last Modified: Thu, 12 Jun 2025 22:54:37 GMT  
		Size: 44.5 MB (44462513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e119535dc9d9cd9b87bb7f9f480283d921f6e1fd9995f68a8df6b3dae2afdb`  
		Last Modified: Thu, 12 Jun 2025 22:54:32 GMT  
		Size: 877.9 KB (877888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8080ed5fe938e91c6fb2cf13df2c6774d671673dc21f86303370c6826fbfa0`  
		Last Modified: Thu, 12 Jun 2025 22:54:32 GMT  
		Size: 3.7 KB (3729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa01ec3e95beb8d8829a4ca55d4f1686ef293b72d9199314aa9ec1e972c4b1`  
		Last Modified: Thu, 12 Jun 2025 23:32:34 GMT  
		Size: 615.6 MB (615605698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3dc2fd94d56840efabe44416d9d3cd55577edf187a3534a96b66c0b1be9954`  
		Last Modified: Thu, 12 Jun 2025 22:54:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463b5f2c01b7d56a91294b84e569e56c7bc8141e015416fecf9ea580f176884f`  
		Last Modified: Thu, 12 Jun 2025 22:54:33 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fea10eaf0607de29318d5121d71e889e9bdb509e93e78f697e779b8a62ac8`  
		Last Modified: Thu, 12 Jun 2025 22:54:33 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0341c875eca6c4eebc54ca023e7ae23dba967372aaad35d4cd97ade0f30f0b24`  
		Last Modified: Thu, 12 Jun 2025 22:58:09 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76f5055fc3ff068332267dfdcea771ce824827b8ac180e2b1f933eb706360d`  
		Last Modified: Thu, 12 Jun 2025 22:58:14 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9add43c4fae696f20ad685bd9ffc3306cbfcab18cd737b4aa91db3f2b37fce`  
		Last Modified: Thu, 12 Jun 2025 22:53:40 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:9c299b47aca350a282338de4edf9aaf24f5c7b56250aca5fa2c704505db1081f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6421b0be3156000fa4bb38046e52c19cbf71ed14181b771285ed0e77d7e5da`

```dockerfile
```

-	Layers:
	-	`sha256:fdd92a35fd8b2955a09e81f54efb29a1bef36480b164e39b65b7d54e11bacd15`  
		Last Modified: Thu, 12 Jun 2025 23:31:44 GMT  
		Size: 37.6 KB (37563 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:985ad2a08187025ea9197de6243c81a89771141824f14905defd6e2f03e0b957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.3 MB (666288345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f03666a59a56c5d115ab45383c6da0da0c639749c4e61e55491bf48ef7291b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:07:10 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:07:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:07:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:07:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:07:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:07:10 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:07:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:07:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107df1885da6b3f0d704e6528f98f7fa3c94661b8f92990d84afdcb07a1bc0b`  
		Last Modified: Fri, 13 Jun 2025 00:12:58 GMT  
		Size: 44.3 MB (44276800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc711ea2f9a6417737f414cef7ac703989f3b88829d303e343141988a94d9f`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 765.0 KB (764954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc15ffe6674bf89403fb61246091c14f2e20302789955bb712245f5a24042e7`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 3.7 KB (3727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab95f41f0304173102959b4f235cc5bf12709ba2379afaf549082acd66f6fcd`  
		Last Modified: Fri, 13 Jun 2025 02:32:09 GMT  
		Size: 592.4 MB (592387770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0cbe9d7cf3571e27db243e40d61c2e7ef30ddd94fc428741b9176a61c5278b`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1312fc0ee350d9939d2b925311037ee43918449530d6611dcc6482054bb39db3`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4494771efad92b1a50b90a330adb0bbcf3d4c823f58fcee7e527b88a9df13bb1`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251d1bf68f500d8378177ebabb098f2166cc199528abd0776ddd57d7b38b457b`  
		Last Modified: Fri, 13 Jun 2025 02:31:56 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9a5adc90956c563c0ba63196c5a7ccc3e528b8e1ce5dacd4d9ca3b9bc6b3d7`  
		Last Modified: Fri, 13 Jun 2025 02:31:57 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e075a806a76ca9b6cdf03fcd5251343c000b62798bcf9080fde2ab478c7d81`  
		Last Modified: Fri, 13 Jun 2025 02:31:57 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:dada07c68a212e50ac190654e1ea53302990f03753c5dbb133a5dd4df9b23d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e51134cb0b31baa48fb289d421680b0ddea0f511945554609d996919eb070a`

```dockerfile
```

-	Layers:
	-	`sha256:f813ad93b40c677407c5ce0c3a52c492c834209d20f0f865c6c750d34b4a125c`  
		Last Modified: Fri, 13 Jun 2025 02:31:44 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.2.7`

```console
$ docker pull couchbase@sha256:49ee943706e38117af05bf4db9d743a02616e9fdd710da5e236d5d3f8ae9f49c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.7` - linux; amd64

```console
$ docker pull couchbase@sha256:9ab200319bac14c9d5b401fb6f18c432754a58027bdea17e236c85ee6c61260a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699262059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6049f97f9a10641a71c296c9030df4ddcbf0bf78be28f6698ade254cd9ea7a80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:11:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:11:37 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:11:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=00115e7e10447a1f2e16aedad43cc33205a30e546e0c881e6dd8703bf8b6acf9            ;;          'amd64')            CB_SHA256=40e45a65a78bf5c9bea0f0d16a1c2e3aab3704aaadd41dccc2d8db2308f30fcd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:11:37 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:11:37 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:11:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b059b2065a301b689a97e29a44f7740d103b4eb6062ba13a205aefd3fb9a8edd`  
		Last Modified: Thu, 12 Jun 2025 23:32:13 GMT  
		Size: 44.5 MB (44463012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c19d4b0a4a35ae5cfa235ab8a8b079e5ba8c0c57888045a9b8c22d03cd6a18`  
		Last Modified: Thu, 12 Jun 2025 23:05:15 GMT  
		Size: 877.9 KB (877913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f7aeb36e17d659bb6444331d594dc893c6076cdf7d4ba344d88e4eaf29909c`  
		Last Modified: Thu, 12 Jun 2025 23:05:20 GMT  
		Size: 3.7 KB (3726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8334a679699f1eb83955fef259a53d1db4957a35db8a0cd6cad5c6ad446102`  
		Last Modified: Thu, 12 Jun 2025 23:32:22 GMT  
		Size: 624.2 MB (624198884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a7837b180f9156c6abb8a2b1318f536ff15830b273ea41afa31708736dcdd0`  
		Last Modified: Thu, 12 Jun 2025 23:05:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ee17442969f3e1824dae9347fb3e51add7325a448fa74e3a15d689bd9ce6ed`  
		Last Modified: Thu, 12 Jun 2025 23:05:27 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83a19acd1280865a5fa48949e03d150ed69d014f1d34105e38b11589c5d598c`  
		Last Modified: Thu, 12 Jun 2025 23:05:33 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686c2c2a20b0e3e8a0911e53ea126b38be748b671e3e99544e754c360d6b61b5`  
		Last Modified: Thu, 12 Jun 2025 23:05:36 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d356a8ffb6bb90dec436ff189c1d71ae4f92cd468a55d61d9ade75cb983afd7d`  
		Last Modified: Thu, 12 Jun 2025 23:05:38 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a4faf0c5f1c7e5f849554821b0b0b2b3f8af38d274cf279068abc83ac8004f`  
		Last Modified: Thu, 12 Jun 2025 22:53:20 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.7` - unknown; unknown

```console
$ docker pull couchbase@sha256:545b1b87718b8b5eca43417ae3dcf7cb53ec17894f57a3258028ce74df44c7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d995ea0d11c1c46c8f241f8c8e5fe3dae8979e13a5216219badca20860d2c3`

```dockerfile
```

-	Layers:
	-	`sha256:c4469ec1a0b391765f5dcacb1d23d5921657fc7aa6818014cac7c64a8c24804b`  
		Last Modified: Thu, 12 Jun 2025 23:31:48 GMT  
		Size: 37.6 KB (37564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.7` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:425d1b1f7c5c4464b1028b3ca0b0c8936f8607f4c4696bbb3f6cb02b4b136ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.7 MB (677743552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aff41b5d201a1751b1977c5dc671bf6f2238a2eb330f3bf134ddae53b1b861`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:11:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:11:37 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:11:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:11:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=00115e7e10447a1f2e16aedad43cc33205a30e546e0c881e6dd8703bf8b6acf9            ;;          'amd64')            CB_SHA256=40e45a65a78bf5c9bea0f0d16a1c2e3aab3704aaadd41dccc2d8db2308f30fcd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:11:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:11:37 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:11:37 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:11:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107df1885da6b3f0d704e6528f98f7fa3c94661b8f92990d84afdcb07a1bc0b`  
		Last Modified: Fri, 13 Jun 2025 00:12:58 GMT  
		Size: 44.3 MB (44276800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc711ea2f9a6417737f414cef7ac703989f3b88829d303e343141988a94d9f`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 765.0 KB (764954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be692b5118b612d6baf9aa9056ae5efd493c5e9807362896fe797727feabfffe`  
		Last Modified: Fri, 13 Jun 2025 02:31:59 GMT  
		Size: 3.7 KB (3726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96b46f030472e3c9887d60e529d203e2520faed550d9e2f820d457bdcf3404`  
		Last Modified: Fri, 13 Jun 2025 02:32:47 GMT  
		Size: 603.8 MB (603842983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396b6c8f201c323bbc9732984f221b5622b737aff275bf06a986f02258acc0ad`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd221398619cff3d7fa1480346668e9bfb337326486382f1231e73d97ad53d2f`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a28a2a71946b0b6ea40d615326d40c20df71d7595c9b0359180ac902139be`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6737f3f4e13bc3f3b9bf2d3f96dcced60fd3275060344ba64cbc8555d6bae58`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb8ff10d43f845e6eef6a3054eb46190dfd8eddb8e6a159aa2775c4ca88d6cd`  
		Last Modified: Fri, 13 Jun 2025 02:32:00 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352df11691fd4077f6ca6af024d7f8aa6ea677c4504fbab1b06b704f01d38ce7`  
		Last Modified: Fri, 13 Jun 2025 02:32:01 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.7` - unknown; unknown

```console
$ docker pull couchbase@sha256:99b5fcabe832d4ce7387079d20afa4755e3539e19572543fecb6438ade41bcd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b23d66c20d413a34a2a2917605e4b394df2e4a2f13aefed99bfca7b3ff95bdc`

```dockerfile
```

-	Layers:
	-	`sha256:fa81e88d6461ac706ae299513ee2ea65e25f206d666958092773eb4582c787db`  
		Last Modified: Fri, 13 Jun 2025 02:31:49 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.0`

```console
$ docker pull couchbase@sha256:fcdc4b32e4a6fa8c0330e23fae5df21725096777296bdd98b57e826e5a5d91cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:8c58435ff60d6ef66d0df41857332d957c1eaec67d6d0e8e2b16b9e87b20af1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 MB (760173247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07541be50814b75b453f83cf2c5215da9d0d51cd2f57dfaa0f004921cb713d2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:28:01 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:28:01 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:28:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:28:01 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:28:01 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:28:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672f48fbd7973400f2aa7ee2ef624e3a15ea0781a2654c7a044f350fdf17254c`  
		Last Modified: Thu, 12 Jun 2025 22:54:47 GMT  
		Size: 39.7 MB (39661820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28913960457f71b38567d7c306bc339d2ad81b0b7f5210c70b4edb0bf9dc2ee5`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 926.7 KB (926716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd74d520bfdd7cf7cfe25896e800591b136144f982501697ff8bcbcd38cb2b5`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9701b9399e309603581d5df8ef5e32b0f2752ae43079e46a818f09e7aedd28ff`  
		Last Modified: Thu, 12 Jun 2025 23:33:19 GMT  
		Size: 690.0 MB (690046534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28482dcd9d94263ad7efdc8a71c830dca382188b456a02624ea3a20612fae067`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d788221dba99727f03e93703d08373582b49fa74c4ac61ff458c14503c1c1c5`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfa9e9407ba3b9fb4e6ebe7e8d31d8e47967a45746cefb3ec4ec49aba051e18`  
		Last Modified: Thu, 12 Jun 2025 22:54:45 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd6ab5b325f510f1ce8dbd588ab0457038dbf53499ce740e276fa94dc09019a`  
		Last Modified: Thu, 12 Jun 2025 22:54:46 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf340e6775252fbf2d20f2fb23fa52506e0cb8a185c9d580669c4430796bc99a`  
		Last Modified: Thu, 12 Jun 2025 22:54:46 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bfbcb12390eeca93aa3653d2f55e92e73bb0a1159a0d7ba30fb236dee9e976`  
		Last Modified: Thu, 12 Jun 2025 22:54:46 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:ecb47bfff99767f6d0b2681b141858e110b451420e58abc6f890fdc3851701e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90439dd8b70e239fbf144f025e3ccbf63b171ec41eb6bf8be20a4ed2f05e0b3b`

```dockerfile
```

-	Layers:
	-	`sha256:db5f59511b1df4122c7565e668ce3c5155126bbe6b2e19ad6f80ac3e1f8abf8e`  
		Last Modified: Thu, 12 Jun 2025 23:32:45 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:8aa182e860c5d2fdae1dce2eb4dfecdde355f8e0823c365876b567ecde85c320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.2 MB (732246834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3da683fc3547b0359304a7bdced0a6dd595e2047f786daf9d62042b4122f7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:28:01 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:28:01 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:28:01 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:28:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:28:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:28:01 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:28:01 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:28:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949b410f178786e3a791e34cf4caa97ce01371746eda082846015d5e4bfc5eb5`  
		Last Modified: Fri, 13 Jun 2025 00:21:34 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0ce8ac50e9fefa9df2b0402b19bd806c1297ccd96d66aca9b10bbf8ad213ca`  
		Last Modified: Fri, 13 Jun 2025 02:32:17 GMT  
		Size: 664.9 MB (664908329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd7861f610f7e4584905c7c272843e2b1a1ae6981d2b0bc418ce2ede67d2e38`  
		Last Modified: Fri, 13 Jun 2025 00:21:35 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42df63d6ebe20b4d802f3f893389db5ef4ee0ed02f7b186f5668f73e96da20`  
		Last Modified: Fri, 13 Jun 2025 00:21:35 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fc61264ad0267e54e0910f263ab8cb3838aa7bb8b0db75ca61a75833bb6e8d`  
		Last Modified: Fri, 13 Jun 2025 00:21:35 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9942a900a81e9dca916e1454757318862359d7181423fde8896bd270142abb1`  
		Last Modified: Fri, 13 Jun 2025 00:21:36 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd42223f51d5c494334523a198291ce7578154ad3085aefbfe3e060cdd1781d`  
		Last Modified: Fri, 13 Jun 2025 00:21:36 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c67a232a421feb9116d5357eb6b5003c276f1f04eb3f90a38f46a012da195a`  
		Last Modified: Fri, 13 Jun 2025 00:21:36 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:c3816aeeefa647e9ebd9d312ff2bbfa7f276eb960b90685be3ad0698f5b3bc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9aa755623c51b01c98cb273ba0b80c0956d36f7699eba462521fd7c327f349b`

```dockerfile
```

-	Layers:
	-	`sha256:ca5806b4c12d660a22550e39e8ace2e7f285891c1df2c7aeba9204d39001a268`  
		Last Modified: Fri, 13 Jun 2025 02:31:55 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.1`

```console
$ docker pull couchbase@sha256:38dbc5eca6a2c7c3c3ec3c9680da757421e2c238a493027c1a7f562c5742741c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:fd607b754f44fd8718d872e3b45bcd1e76ef6eebf9b05a9e4629a0266198fb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.2 MB (760198848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88590696426d49a5e2ef00e0861ae0e665c412c6aa436537c48c48a7fece5fd3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:37:02 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:37:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:37:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:37:02 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:37:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:37:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e39031db150ce656cf9ca6a0fca0d064165dd6a74217a23da76bad5995bfcae`  
		Last Modified: Thu, 12 Jun 2025 22:54:15 GMT  
		Size: 39.7 MB (39661970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d673779b83adf8b8ed2f7c68fa1df646fb53d3b619954f75d59e15a37debc3`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 926.7 KB (926658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2cad75f5e35fa7ea4bce1e8e5c4b23fcf9fa5d28474f4e42771faf47d32dc3`  
		Last Modified: Thu, 12 Jun 2025 22:54:13 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93292503745e1d91b7f00658690ebd8a1d02145bace63c37f5fe52f8ed1aabe4`  
		Last Modified: Thu, 12 Jun 2025 23:33:28 GMT  
		Size: 690.1 MB (690072039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfd485997df4612e9271e8f31669df600f763072a758d987e5afc0f86193ea4`  
		Last Modified: Thu, 12 Jun 2025 22:54:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd51eb2052c1eb2d677d57128e7762a6eb1f6c48a891f970477f7b9f1458be7`  
		Last Modified: Thu, 12 Jun 2025 22:54:14 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d11ccde910c127552791c99203152099a2417683047e77bebc89180c6f35`  
		Last Modified: Thu, 12 Jun 2025 22:54:14 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e49970b2b2fffc8fdfaf2d63094df41f865fac6816e401c97a35b959ad3f3c6`  
		Last Modified: Thu, 12 Jun 2025 22:54:14 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523793682babdfbae10abf450f3190d11461e112acf046c32680165d7fcd4fa6`  
		Last Modified: Thu, 12 Jun 2025 22:54:15 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4790857e1cc2dad01c5da2bffd3d1dab5d6c2d096b70dec4545bc41e3b0d0f68`  
		Last Modified: Thu, 12 Jun 2025 22:53:42 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:66c869bfef0ca748e17a02c857574bd3f707cef9b3a9ce9fc582c2c55cc1736c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55f0c7fc2c3d0d7abd95872dbac356d2ca9c2a989f57fb78949ffffc5cadd57`

```dockerfile
```

-	Layers:
	-	`sha256:1957712fb032d050690aca408537e8c8960e0653a4da3c222d190a8f1083d0d0`  
		Last Modified: Thu, 12 Jun 2025 23:31:59 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:260465c69f1cd94cf6f05661a6d176e0783fb656e94869a1233809de36f1e499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.3 MB (732256190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e97c6fb733cd8bfa1d849447c25b1f7d38c7706ccecc11bcda6ca0bf65ac1d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:37:02 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:37:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:37:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:37:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:37:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:37:02 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:37:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:37:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302123858fb97709374ed5f0a5ab03a0219ce73bfed4421d66e809c51ede908`  
		Last Modified: Fri, 13 Jun 2025 00:18:17 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0cc7effa53c5c55e7f2b8e111b5a7057dd11323e57cf6c97a12541e41444c`  
		Last Modified: Fri, 13 Jun 2025 02:32:56 GMT  
		Size: 664.9 MB (664917689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41824fa2fdb6bb2e9ba7fa544931671742b7045afd9c67cdb3782f423f006e8a`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc4a03842852c17e967ac5342dbe8ecc31e0fc62c8c99a10566483dc37e359`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1116f3e3f0afa1e47a10b485a5638452fb0f8f2f3c7ca563131dad136a6e794`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1ba829865135a6eb347d14c978f3846c7dcc664d707e99982a0cc01d2bee32`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6855c02d059c04f5c3b6f05e056955193e06f87fd490af65ba3e0aaa2b1e601a`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4265ecdce870e125cf87962388458ab697ff852085339a7cdf2ffc3d255f56d`  
		Last Modified: Fri, 13 Jun 2025 00:18:20 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:20a9fae29b2197bf9a658d76becac93535d9ddd4e8eef22084975309941b4845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd06b10f8c873d09f7052d7ff1daca1afcc0d9754dc447c7b41a53780955637`

```dockerfile
```

-	Layers:
	-	`sha256:1f3813e8bd608e8b8863d68fe18dde3eaf5b1070c18c30f16a8a5186edfd938c`  
		Last Modified: Fri, 13 Jun 2025 02:31:59 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.2`

```console
$ docker pull couchbase@sha256:617e8e93866dc72fd505053eb1f60a516394d4868899f5463b05917eefc4256f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:ca8cf49e12246337a3b8147313915822dbfc50fe0a042e175603dc75947c84b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.4 MB (774351777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced95db906874cae18d89890bea37f4bf27f61bfdf32976e1e5dabaa8f203371`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:45:24 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:45:24 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:45:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:45:24 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:45:24 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:45:24 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3882126313fe1a25b4825da041ace7b8bc7f7f228a6bf588d2bfb1df9c26a6e`  
		Last Modified: Thu, 12 Jun 2025 22:54:09 GMT  
		Size: 44.5 MB (44462796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0b40090f76c753c8eb038cc192fd505dcd942fd017c63f9284b488639deabb`  
		Last Modified: Thu, 12 Jun 2025 22:54:07 GMT  
		Size: 877.9 KB (877910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e0be32a665300ca61ed94fbb4d98c09fae2b720fcac15146d4533815ef41fd`  
		Last Modified: Thu, 12 Jun 2025 22:54:07 GMT  
		Size: 3.7 KB (3727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5546dc435c89078d16707ace865c3703a6cf5765bb3bf611d51a4c1cd56feb0b`  
		Last Modified: Thu, 12 Jun 2025 23:32:29 GMT  
		Size: 699.3 MB (699288816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f307ccfdf77152847509050292006e6c2d72069c62bab7be9970c9f3735ed8`  
		Last Modified: Thu, 12 Jun 2025 22:54:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a16d1afa31985697405cd913acb67158cf5d39ad047b0693f698f310ae31c0`  
		Last Modified: Thu, 12 Jun 2025 22:54:07 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882d677decc39c0d8272e63c8c284b8d6deef4c3b4575894e24f2ff64914e2eb`  
		Last Modified: Thu, 12 Jun 2025 22:54:08 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d83b82cb36dfe0db3592c2903209c0a5d165040c2978a985bdabb3c05a4010`  
		Last Modified: Thu, 12 Jun 2025 22:54:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c66aeed2ad9a7c37ef2a926d6ee819ef13ed6511bc8ea514b34a2f44de76fd9`  
		Last Modified: Thu, 12 Jun 2025 22:54:09 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b27bfad1805a8c209119f1e44b896c0c244c2de1e7e3c7339b1b2450db66de`  
		Last Modified: Thu, 12 Jun 2025 22:54:09 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:02169ee36208c613bf0e0fd62fc043b027417bc7a77cce80c714d71e32b15951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316ded06288cd67d9131d05bed503c06f902304d5ec28bd9bdd5e9c915692e2a`

```dockerfile
```

-	Layers:
	-	`sha256:7b4c1ac3ba72f9ede95c0ff77413394a8c783c768f58fdbf2a827d6919a56531`  
		Last Modified: Thu, 12 Jun 2025 23:32:02 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:777def477daf718cd43c2fe39ea247038cdb937f737415ecbed02fcae2d9bdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.3 MB (747295599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410c68a8d54c5f897ab48ed8400db7071641c92174401e08439812353542925a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:45:24 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:45:24 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:45:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:45:24 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:45:24 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:45:24 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c107df1885da6b3f0d704e6528f98f7fa3c94661b8f92990d84afdcb07a1bc0b`  
		Last Modified: Fri, 13 Jun 2025 00:12:58 GMT  
		Size: 44.3 MB (44276800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc711ea2f9a6417737f414cef7ac703989f3b88829d303e343141988a94d9f`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 765.0 KB (764954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3155b24d9b7071433303d6350d6fc960f85472c86fc383cdef620190cda64385`  
		Last Modified: Fri, 13 Jun 2025 00:12:55 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c87b61fccd5893ae49bf8b33baed55acbf276491c523f51007b8224445a02d1`  
		Last Modified: Fri, 13 Jun 2025 02:32:59 GMT  
		Size: 673.4 MB (673395035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39920de859b77d1cd52a94dd38594ebcd62fa3b1d73aeb61d7617163239b3ef9`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7503cd2524050cb4857d3586ba56d7c7e1bb40915a798e7d19feb2614a4cedf9`  
		Last Modified: Fri, 13 Jun 2025 00:12:56 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7475c3a523104cbb21edce6e8460f41e07e2c97d1e2869f502e183c41078d9`  
		Last Modified: Fri, 13 Jun 2025 00:12:57 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12176b6ca9a5d1d52bb1659bdda87d6cfc0f434fa710467f473f83a65850944`  
		Last Modified: Fri, 13 Jun 2025 00:12:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9301660eee6c297fa23b70bcd066146ea1c2765a8ee7257db66c0ceb81eb18`  
		Last Modified: Fri, 13 Jun 2025 00:12:57 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8aa3b6a7e8cf2952ee27ebc80f9422015e0bafa123fe7dc5e6900fba74b5c36`  
		Last Modified: Fri, 13 Jun 2025 00:12:57 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:78be8969caa00accb9b2a0240c07b3ff5d0b70d83e903d76b9cd0c40b285d64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcc774416e8ff563d50b87dc0c71edb3336ae5f3e57527fb6d2294632100a3e`

```dockerfile
```

-	Layers:
	-	`sha256:f58d47e20a743f295b24c671b3b88096e32179a313d9750e4073caa93cf859c9`  
		Last Modified: Fri, 13 Jun 2025 02:32:04 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.3`

```console
$ docker pull couchbase@sha256:f29225ff3d52cf9e793c27af4e0f89305b9d4897393ad9ad95a58138174abc98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.3` - linux; amd64

```console
$ docker pull couchbase@sha256:aa8da6957cac0f4690685fb729577c16aba6bbb8d8d2dccdc4c9ef2aa8e71227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.0 MB (768950880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab146357bae23f7b2666a91639ed99a88e26c8de3bedbef971ca996f7e0adff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55222b70d50b4c6ab08b229e868de57bdcd2cf94c8d2c8398e6a4079077dcb9`  
		Last Modified: Tue, 03 Jun 2025 13:59:26 GMT  
		Size: 39.3 MB (39303165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c44a8a81960048f337df5b1d2876d8db39f18a4d15a3652130caf651b08584e`  
		Last Modified: Tue, 03 Jun 2025 13:59:23 GMT  
		Size: 926.5 KB (926489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be96b2f62cb9e476616bb01bce73aa8b42b17c8c5e969b09b4edf1d7d3de221a`  
		Last Modified: Tue, 03 Jun 2025 13:59:23 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97bbc27af356991c02b775de2a194b0df095827669c832a76b9cd06f84ed2d3`  
		Last Modified: Tue, 03 Jun 2025 13:59:52 GMT  
		Size: 699.2 MB (699183043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f479e0fdd5d97f5cece894147abf8af640f3ed7ce7e7419afd5d3f5a60dc41`  
		Last Modified: Tue, 03 Jun 2025 13:59:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d119f621afc395f502b91ae991e509cb492c9338e4eec703caa06b5e30936abc`  
		Last Modified: Tue, 03 Jun 2025 13:59:26 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aca629660826303ac3e396bd9341711a53aeaa0a031ef68dd693af3fd87a1fa`  
		Last Modified: Tue, 03 Jun 2025 13:59:27 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef38953cfff5bef3c935f2169b1743906082dbf2fb8b74f611e042da5ac7e3f`  
		Last Modified: Tue, 03 Jun 2025 13:59:27 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87451e6d0a03ea5f6b6ef031f00864f9d885fae621b018b3857a1642a6827f`  
		Last Modified: Tue, 03 Jun 2025 13:59:28 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ed3a9fdf3ad7d37e36b9b22b9f67105408285bda2f1d71474d608818ffc48c`  
		Last Modified: Tue, 03 Jun 2025 13:59:29 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:322632fd79638a00ccb5750f721f5caaf09923c652f75b0de915dbf8a8a77038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6cfccdee9d1c6a9bc88d654804bb8c3428b18aa879a2fb1b17f5b799112b7c`

```dockerfile
```

-	Layers:
	-	`sha256:30550a622610d3e98a55f0f5f2b57e34d0343539f397186bd92e3b89baede131`  
		Last Modified: Mon, 09 Jun 2025 09:39:41 GMT  
		Size: 35.8 KB (35816 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:2a759f1ddced1a6fa2c8e68facc4d053231438860e9cdcdd7cf57367e34e8793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **740.3 MB (740276108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1438957e900bdb6e7d66a195bbdbe773851563b8b124ae48e27dcdf30d4d58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b154720591954ca83cbc0b928875845debd45fcdd5096534cf440f0fc16986e5`  
		Last Modified: Tue, 03 Jun 2025 15:24:45 GMT  
		Size: 38.8 MB (38849664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e244477b78cc71a61574fae065b6dbb60f35a58c3a4e8123349f9a4de88d428e`  
		Last Modified: Tue, 03 Jun 2025 15:24:47 GMT  
		Size: 770.8 KB (770780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f050eca393d797b23ce8cea8082de1b24b4bd73065997fb4d1c2b0a29e96b86`  
		Last Modified: Tue, 03 Jun 2025 15:24:59 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edabb57d607c5dc7ed3962162bcfda1afb083299ef68fe8e2c50654ea285c266`  
		Last Modified: Tue, 03 Jun 2025 15:25:16 GMT  
		Size: 673.3 MB (673294899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14145d888a1bab86b49550c932bbea8dea33f4ebbfad7bbac7d60e597f8ab9cf`  
		Last Modified: Tue, 03 Jun 2025 15:25:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765fac2fa5480dde9bec86cc095ce940692600d829cabf3884d7eabd3796b78c`  
		Last Modified: Tue, 03 Jun 2025 15:25:43 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1695ab1a7319c572db06621456ebae651bf501a56c9885bd151a821d87f55b`  
		Last Modified: Tue, 03 Jun 2025 15:25:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3163f0787aaf49e308ce31c8a9c615a7553238f268061ad5a9e384f680f05a`  
		Last Modified: Tue, 03 Jun 2025 15:25:47 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297edacd09fccc9c8389aff7a9c110bafa3829928be377cd2659efeddb151354`  
		Last Modified: Tue, 03 Jun 2025 15:25:49 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5da48f4d40906bddeb8b543559f8ea3eb0c46a4828d857f33e339d9447dcd8`  
		Last Modified: Tue, 03 Jun 2025 15:25:50 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:f6317c5cbbface9b95a038df62e43852366f11f2370ea9c3605eed5580d0005d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad297eb02eb69ded13d1a799d9a42c81f55abe5085c62da7e65fe50657fea7`

```dockerfile
```

-	Layers:
	-	`sha256:b938abe563324a7bba451c43857a95da7ea9c4f2c2cfb99fbef902036889ff38`  
		Last Modified: Mon, 09 Jun 2025 09:40:23 GMT  
		Size: 36.0 KB (36001 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.4`

```console
$ docker pull couchbase@sha256:fe89075e364455e25a09c2c4cd663b9a579453001db64a990bbd83cd960a2b37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:8f17595567e2af921ebed345cdcf762f537705085ae15113800ee5f50877cc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.6 MB (771641867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c86687d7d93b858d8527ad737c86b9225a487026572d223ebf063a0c4937b99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Dec 2024 01:31:34 GMT
ARG RELEASE
# Wed, 11 Dec 2024 01:31:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Dec 2024 01:31:34 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b474f1da5b847f8b8cff69cc18bcb780f85d2ba869bac4f7f648323563e45c96`  
		Last Modified: Tue, 03 Jun 2025 13:38:35 GMT  
		Size: 39.3 MB (39302774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f20a70270ad90fb3501c9902d7c99ebe44d6a33de8a7ea07e69583eb02bbed`  
		Last Modified: Tue, 03 Jun 2025 13:38:32 GMT  
		Size: 926.5 KB (926503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50bf634fe340d52f8fb091e69a599bc3ee4f5710f8ad5f213c85bfe5ffc1e80`  
		Last Modified: Tue, 03 Jun 2025 13:38:32 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce17fcdb19e9aff9c1fcd3d1ecddb2723802122963934355d6c0f88554834bab`  
		Last Modified: Tue, 03 Jun 2025 13:38:43 GMT  
		Size: 701.9 MB (701874410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765a02c753fa411a3804a288d48202488cf820caeb9b5ce777863ff992250f0e`  
		Last Modified: Tue, 03 Jun 2025 13:38:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae846ae6621a11dc987bcddfda7a153e60d56fbef47fd950bf14ef4971672a2e`  
		Last Modified: Tue, 03 Jun 2025 13:38:34 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0402ec5fb7e687854b511c872d1ce6e362c43f98d1035bceb09a946292abcee8`  
		Last Modified: Tue, 03 Jun 2025 13:38:35 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b080d8344eb228c851803ba32c22a556f02a60b141587290f2bcc7194d2b5a`  
		Last Modified: Tue, 03 Jun 2025 13:38:36 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967466dee179d250ff92503444e804444873417b8a909ddec81bdd7a710511bb`  
		Last Modified: Tue, 03 Jun 2025 13:38:35 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543636058992d931a7b6a573e54564235768a9eafc02d3a6c40dea19d634acb9`  
		Last Modified: Tue, 03 Jun 2025 13:38:36 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:d8b55ce73a114df6c730693943dd1738a033f4c660e2b96f029cf2f960ff0003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2126fa67fb09cdab45ddf4c0943bb57b980507e764dfb0c9036ccb9003999`

```dockerfile
```

-	Layers:
	-	`sha256:d0911ee5ba0070ddc6341ca142efb79f30c770863ff7000b952f2c38402a44fd`  
		Last Modified: Mon, 09 Jun 2025 09:41:10 GMT  
		Size: 35.8 KB (35816 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:fedd1c2701d8e23b1336d428397945d8b4119aa36ec90ccc5ed01eb27ff3c2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742538627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0564948e24da3752c3ceaa553bf256d8796e93697d0db8507c9ac35cb77f38fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Dec 2024 01:31:34 GMT
ARG RELEASE
# Wed, 11 Dec 2024 01:31:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Dec 2024 01:31:34 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f361a6f25d6c2f377926be0702e03dc9020fd5bb8b191d1b234a4d32f7f2e66`  
		Last Modified: Sun, 08 Jun 2025 13:16:46 GMT  
		Size: 38.8 MB (38849514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a669d8a690ed3f16e2ab00fa8214a52de719f88a9e1e23bece54c0d8baf3e72f`  
		Last Modified: Thu, 05 Jun 2025 00:47:58 GMT  
		Size: 770.8 KB (770800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646547249b04cf88edb49f635fef620c23ba8a643faa4b2ff8f1f6247ba03c22`  
		Last Modified: Thu, 05 Jun 2025 00:24:24 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231dc9ceae02aa6e40e37648f0cd1726ab1e05ca0e6d5cf8310303d28eb3d783`  
		Last Modified: Sun, 08 Jun 2025 13:17:13 GMT  
		Size: 675.6 MB (675557549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a737d39bc61fc15decf4a2e6b29f1be076a506471159bb2c50c4fd933be76e0`  
		Last Modified: Thu, 05 Jun 2025 00:43:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf90132ee89615a36b1c5f37e5291641a7498672275061c547648de3279a9eff`  
		Last Modified: Thu, 05 Jun 2025 00:45:14 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628447a14c4cbea637f72796599c3b120b714280782c7e3e012e69333ab23f41`  
		Last Modified: Thu, 05 Jun 2025 00:25:41 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f94330626f2e359c1997d6b178c6a0c03978e1eae9f5dae1cf57e49f947c8`  
		Last Modified: Thu, 05 Jun 2025 00:30:54 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a470098480b27d22a01494dce12c03aa32cc5a1232d45ab02f2d77f95a223ed4`  
		Last Modified: Thu, 05 Jun 2025 00:29:52 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445bc610a57d7b990415ad150673af0cacf1ef671b638809c4483d45669140d6`  
		Last Modified: Thu, 05 Jun 2025 00:28:59 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:6703008d78bb7f76b08aa148b9bfd3a24385c6047c5d1d98054b9e2ec9300240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e515c7ee094b3b0f61b49f64b6429f6324995d1cb7d3f9bc02f640aa6912628`

```dockerfile
```

-	Layers:
	-	`sha256:e6e734518b1d52aafc2675f97053ab22cd46ff7e007efc3f8bac926d313cfe71`  
		Last Modified: Mon, 09 Jun 2025 09:41:49 GMT  
		Size: 36.0 KB (36000 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.5`

```console
$ docker pull couchbase@sha256:53cabb59e0a6ccf313b0c626342857697bb7d9045e7e9d0bea1f0c9c4ec2f82c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:e2a5539f374401a1ccec4e421e3458628aee15f1a0b866ffc0ad1a0d7f5af427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.5 MB (771502076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c3be3031535a1639e938ad3b16caefdaeadc1ab276da48ebe73f9aab01a2f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df6d811e414c9bc0fa90313a5ce9ee533a0db9c4658fa92afde557c0fc3b4d4`  
		Last Modified: Tue, 03 Jun 2025 14:21:43 GMT  
		Size: 39.3 MB (39303079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9ed4b23b372ec2d8be0d41054c75a1e80e784910e019d0fe86688efd3c1d9e`  
		Last Modified: Tue, 03 Jun 2025 14:21:38 GMT  
		Size: 926.5 KB (926524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862f0a3683e11cad7cc02782d6011c0e571f17f1eb5c000a8d2025a8c3893963`  
		Last Modified: Tue, 03 Jun 2025 14:21:39 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279ad3bbfca41c98ef9b4dc6d7fd9979c04720a54427c1795c640d989f850d64`  
		Last Modified: Tue, 03 Jun 2025 14:22:03 GMT  
		Size: 701.7 MB (701734298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97630b598230fa86b42fd9f6172b4193d182f5bb10a60257f790f664e2bf066b`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ac2c371a7eae27c0e3881d6f60e62b53d7b1d564b8d1bf1bd1154df49bad06`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e1fce97eec6b12373568d9298ace868e680da3666ea8a23a8d28172f70f842`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e941e9da6a51d4b21df61434f398328cae1d3dba5ed62846de65e6d5fc7815a6`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73769932534b2a83793205d49391a878725c37b62293cf84f5b21c2fb2b97d1f`  
		Last Modified: Tue, 03 Jun 2025 14:21:40 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543636058992d931a7b6a573e54564235768a9eafc02d3a6c40dea19d634acb9`  
		Last Modified: Tue, 03 Jun 2025 13:38:36 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:2b48d96ee77f7a90f1b4467865c7881530ac85ee8319590ad1131241be1e16f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31ccf954e591cd39beed8b92b87a4cfb33c75eb118a7c85eb3ac103803f7d2f`

```dockerfile
```

-	Layers:
	-	`sha256:d755417d8bac42b0e89c6a1fc7e854d6e138796faf3daeccce06eaf3c2f28ac3`  
		Last Modified: Mon, 09 Jun 2025 09:42:29 GMT  
		Size: 35.8 KB (35815 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:44df46e4dd6331d55bcdebb1b42d7456fec362b455b06643d4a9ff1b7e1d1b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 MB (742447046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c642f10baa1c1f95c4fd182c779f6de5b958cb90aaa393ba33d69699c5af3f87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb218b446475a0d4ef98ac0a6db53f42870b1da38289d0c5e60bff4e9d16e00`  
		Last Modified: Tue, 03 Jun 2025 18:33:24 GMT  
		Size: 38.8 MB (38849424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75e7de92406d824e5b74f949abbe64e88cf0040128c07c384a24c6feedd88a6`  
		Last Modified: Tue, 03 Jun 2025 18:33:22 GMT  
		Size: 770.8 KB (770794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1444fd4fe9e404a94930de4acd996527fdfffc3d0d1094277159b9d717b8406d`  
		Last Modified: Tue, 03 Jun 2025 18:33:22 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c73bb60bd14f2ccdf3877c41d2dd981c2d83ede446cbe1e2a17121cfb9e02c`  
		Last Modified: Tue, 03 Jun 2025 18:33:41 GMT  
		Size: 675.5 MB (675466064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6606151ebe3c7b0d421fb4f4e806eb2b702734d351232e2584583cc6d54f2968`  
		Last Modified: Tue, 03 Jun 2025 18:33:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21da1ebba94c5246925ccece3d1cef02b24d91428cdeced0ddc1c01d2dc30842`  
		Last Modified: Tue, 03 Jun 2025 18:33:27 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7756633777d4a877f22d181e683180b97887e1ed4c26cae124daf15f558d4a4`  
		Last Modified: Tue, 03 Jun 2025 18:33:27 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628745b3c92e6e0ac6d209b65897fcaa7d1f9fa28cab52fe71c960d7f44fa707`  
		Last Modified: Tue, 03 Jun 2025 18:33:29 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a0867532814dc2223df70637b5efd7792188339cba79d2ad041581d8bb6a51`  
		Last Modified: Tue, 03 Jun 2025 18:33:30 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a471e6d02789d12ffdd987716bed3c6161b99e00c9053e8717e40ee3e05638`  
		Last Modified: Tue, 03 Jun 2025 18:33:32 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:cf1fd9455b73fb3eec6e8c228c2937f2e4a1e2cba8de00ec717981aaa530918f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14af482de3103e7b7dfb2be6e93415a1378dbafcbf8632f23870214875f4e217`

```dockerfile
```

-	Layers:
	-	`sha256:1dbd85a2183ab607d618287882ab20aa489e848bb687bed4c8affbf4bbfbcb92`  
		Last Modified: Mon, 09 Jun 2025 09:43:07 GMT  
		Size: 36.0 KB (36001 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.6`

```console
$ docker pull couchbase@sha256:ed940813ca0f960529d855c742f4372df0e88b0ade7c0679627878e42b6c4924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.6` - linux; amd64

```console
$ docker pull couchbase@sha256:813b49e0ef39898d3faebf195415d335281419b36e9e91bf735b5f7e343bd056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.7 MB (794747783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ffca8857d13518cb9908e5b399639ad3252e6a8cedbfbdbd81ae23dde24b27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c3b3cacce9f37e529d00643dc6a7356b93b7d570405de6a0c61641956cbc26`  
		Last Modified: Tue, 03 Jun 2025 14:07:29 GMT  
		Size: 39.3 MB (39303163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dda7d77f72011a4ebf049e73e839994a45f1e0354ec21466733d34be426f15`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 926.6 KB (926575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf7924979a5479a138d955d08a263461036a06e7ae36502d75c3c538b2ceb3`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0988595feb9082d9db0ef1f794d362bafef150552c279ccbef7d19658e7245`  
		Last Modified: Tue, 03 Jun 2025 14:08:18 GMT  
		Size: 725.0 MB (724979867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b1e063f9f2404c773cd3c78b32f368fa15f399dc40dfb9f672cf164f335f1a`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bea16e78db287004b1ad579baf90c6b57e09cf51ddc0d96a0310218cd724e1b`  
		Last Modified: Tue, 03 Jun 2025 14:07:23 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2709a0a231e86cd0d2106017eb8e7f72cd40b9437fa35ee1d4b905ccb449ea8`  
		Last Modified: Tue, 03 Jun 2025 14:07:23 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082fb5c7ef2892c9a9fe0f11aa63bcdb5f588076c0cc5d8f95ecfa7aebe54ebc`  
		Last Modified: Tue, 03 Jun 2025 14:07:24 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254548277f51a3a7ba0b0bb147b391c1bbb5c6d00278719e96c50b077a7401b4`  
		Last Modified: Tue, 03 Jun 2025 14:07:24 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124a32eeb718d8c54c6f29c2cfc25b213993e9c7c18a2aa9f78a6fc3406b8c8`  
		Last Modified: Tue, 03 Jun 2025 14:07:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:1daaa4381959c4b4ad2f72a92916db538dbbaa3abec64a39c63885b05dfd0d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15a75a67b82da4a16cbe101895e937cee932dc19cff9438f2168fbc00d96b39`

```dockerfile
```

-	Layers:
	-	`sha256:33308da65b82e8843d44557e4599ddcc303a72f6765b43c1b91b30528910a4f5`  
		Last Modified: Mon, 09 Jun 2025 09:43:47 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:98e455037d80a274b6cd74cd39f5af3e415f82701681c0bec5e79741e3870fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.4 MB (763408090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248c506b8cd15abac9233058c8c0eb3b712c0cb0af360622488f453792122ef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffde452cdb09fa506c9cb01e48875a79d2ded94d9d6ddd3f83c385acea1eb61`  
		Last Modified: Tue, 03 Jun 2025 16:23:38 GMT  
		Size: 38.8 MB (38849499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c55621952ece84f3edc704718bb4859c7e103a8964f6844479de0c663696207`  
		Last Modified: Tue, 03 Jun 2025 16:23:36 GMT  
		Size: 770.8 KB (770806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9129adffdc0253ebbaaf1fb32ef66c49ad8caae70fabd05c02f825d48b70a3`  
		Last Modified: Tue, 03 Jun 2025 16:23:37 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c25687cb69cd4f05d93b1b6b36d4e2ae9b3ec616d633182a417b035ec7587d`  
		Last Modified: Tue, 03 Jun 2025 16:23:47 GMT  
		Size: 696.4 MB (696427022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2472d3bcb419b1c988d37f3335bca984f97e4761e92591bbd90cd6c310c3ec0`  
		Last Modified: Tue, 03 Jun 2025 16:23:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86103da5720e37d892f6759b260e4e107cc473a6bdb28fd91e56fd9c0874ec`  
		Last Modified: Tue, 03 Jun 2025 16:23:40 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb1c195d48e7e38da8cf8ed94d652eac554674f4dd6a11e3b3f5e2a5638e5f`  
		Last Modified: Tue, 03 Jun 2025 16:23:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245cae7b9c382625baa4aa92f8cbad7a51be6eeb8699cb27fdea759f77a321b7`  
		Last Modified: Tue, 03 Jun 2025 16:23:41 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd96e7c64ea0cd990e8b0a28cfafefa13e66d5770a6b4936f2be9253cf4028a`  
		Last Modified: Tue, 03 Jun 2025 16:23:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80e30ef682957a3d400e3cde48f2ba445546fe6d766b773fced5cff5cc0d584`  
		Last Modified: Tue, 03 Jun 2025 16:23:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:4420ad1d2cc33c840698e68eba16d59df4d23079db1a823d3190554adce826ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d235a4a034c854c1f1afba39ea87e6a6bb8556d36d3122f53e96399cdbf05ed4`

```dockerfile
```

-	Layers:
	-	`sha256:7ef6c92eff7f2075083657443152388b0e1d290e559404824f0a8cf72af0bd01`  
		Last Modified: Mon, 09 Jun 2025 09:44:31 GMT  
		Size: 36.6 KB (36640 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:ed940813ca0f960529d855c742f4372df0e88b0ade7c0679627878e42b6c4924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:813b49e0ef39898d3faebf195415d335281419b36e9e91bf735b5f7e343bd056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.7 MB (794747783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ffca8857d13518cb9908e5b399639ad3252e6a8cedbfbdbd81ae23dde24b27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c3b3cacce9f37e529d00643dc6a7356b93b7d570405de6a0c61641956cbc26`  
		Last Modified: Tue, 03 Jun 2025 14:07:29 GMT  
		Size: 39.3 MB (39303163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dda7d77f72011a4ebf049e73e839994a45f1e0354ec21466733d34be426f15`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 926.6 KB (926575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf7924979a5479a138d955d08a263461036a06e7ae36502d75c3c538b2ceb3`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0988595feb9082d9db0ef1f794d362bafef150552c279ccbef7d19658e7245`  
		Last Modified: Tue, 03 Jun 2025 14:08:18 GMT  
		Size: 725.0 MB (724979867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b1e063f9f2404c773cd3c78b32f368fa15f399dc40dfb9f672cf164f335f1a`  
		Last Modified: Tue, 03 Jun 2025 14:07:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bea16e78db287004b1ad579baf90c6b57e09cf51ddc0d96a0310218cd724e1b`  
		Last Modified: Tue, 03 Jun 2025 14:07:23 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2709a0a231e86cd0d2106017eb8e7f72cd40b9437fa35ee1d4b905ccb449ea8`  
		Last Modified: Tue, 03 Jun 2025 14:07:23 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082fb5c7ef2892c9a9fe0f11aa63bcdb5f588076c0cc5d8f95ecfa7aebe54ebc`  
		Last Modified: Tue, 03 Jun 2025 14:07:24 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254548277f51a3a7ba0b0bb147b391c1bbb5c6d00278719e96c50b077a7401b4`  
		Last Modified: Tue, 03 Jun 2025 14:07:24 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124a32eeb718d8c54c6f29c2cfc25b213993e9c7c18a2aa9f78a6fc3406b8c8`  
		Last Modified: Tue, 03 Jun 2025 14:07:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:1daaa4381959c4b4ad2f72a92916db538dbbaa3abec64a39c63885b05dfd0d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15a75a67b82da4a16cbe101895e937cee932dc19cff9438f2168fbc00d96b39`

```dockerfile
```

-	Layers:
	-	`sha256:33308da65b82e8843d44557e4599ddcc303a72f6765b43c1b91b30528910a4f5`  
		Last Modified: Mon, 09 Jun 2025 09:43:47 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:latest` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:98e455037d80a274b6cd74cd39f5af3e415f82701681c0bec5e79741e3870fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.4 MB (763408090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248c506b8cd15abac9233058c8c0eb3b712c0cb0af360622488f453792122ef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 20 May 2025 00:08:02 GMT
ARG RELEASE
# Tue, 20 May 2025 00:08:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 00:08:02 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Tue, 20 May 2025 00:08:02 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 00:08:02 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 20 May 2025 00:08:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 20 May 2025 00:08:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb
# Tue, 20 May 2025 00:08:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 20 May 2025 00:08:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=21b348be14c30e39658e9378ed62750806a20946677866d5859ac426df0e6486            ;;          'amd64')            CB_SHA256=43992488e154a87119a7ffb738de92b3364f5b1bfcbdd958e757e87762076ed7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 20 May 2025 00:08:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.6 CB_PACKAGE=couchbase-server-enterprise_7.6.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 20 May 2025 00:08:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 20 May 2025 00:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 00:08:02 GMT
CMD ["couchbase-server"]
# Tue, 20 May 2025 00:08:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 20 May 2025 00:08:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffde452cdb09fa506c9cb01e48875a79d2ded94d9d6ddd3f83c385acea1eb61`  
		Last Modified: Tue, 03 Jun 2025 16:23:38 GMT  
		Size: 38.8 MB (38849499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c55621952ece84f3edc704718bb4859c7e103a8964f6844479de0c663696207`  
		Last Modified: Tue, 03 Jun 2025 16:23:36 GMT  
		Size: 770.8 KB (770806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9129adffdc0253ebbaaf1fb32ef66c49ad8caae70fabd05c02f825d48b70a3`  
		Last Modified: Tue, 03 Jun 2025 16:23:37 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c25687cb69cd4f05d93b1b6b36d4e2ae9b3ec616d633182a417b035ec7587d`  
		Last Modified: Tue, 03 Jun 2025 16:23:47 GMT  
		Size: 696.4 MB (696427022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2472d3bcb419b1c988d37f3335bca984f97e4761e92591bbd90cd6c310c3ec0`  
		Last Modified: Tue, 03 Jun 2025 16:23:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86103da5720e37d892f6759b260e4e107cc473a6bdb28fd91e56fd9c0874ec`  
		Last Modified: Tue, 03 Jun 2025 16:23:40 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb1c195d48e7e38da8cf8ed94d652eac554674f4dd6a11e3b3f5e2a5638e5f`  
		Last Modified: Tue, 03 Jun 2025 16:23:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245cae7b9c382625baa4aa92f8cbad7a51be6eeb8699cb27fdea759f77a321b7`  
		Last Modified: Tue, 03 Jun 2025 16:23:41 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd96e7c64ea0cd990e8b0a28cfafefa13e66d5770a6b4936f2be9253cf4028a`  
		Last Modified: Tue, 03 Jun 2025 16:23:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80e30ef682957a3d400e3cde48f2ba445546fe6d766b773fced5cff5cc0d584`  
		Last Modified: Tue, 03 Jun 2025 16:23:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:4420ad1d2cc33c840698e68eba16d59df4d23079db1a823d3190554adce826ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d235a4a034c854c1f1afba39ea87e6a6bb8556d36d3122f53e96399cdbf05ed4`

```dockerfile
```

-	Layers:
	-	`sha256:7ef6c92eff7f2075083657443152388b0e1d290e559404824f0a8cf72af0bd01`  
		Last Modified: Mon, 09 Jun 2025 09:44:31 GMT  
		Size: 36.6 KB (36640 bytes)  
		MIME: application/vnd.in-toto+json
