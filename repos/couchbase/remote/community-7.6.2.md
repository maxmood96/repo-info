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
