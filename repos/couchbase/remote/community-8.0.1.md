## `couchbase:community-8.0.1`

```console
$ docker pull couchbase@sha256:e1d1c0fd6fc99bcf3daefdf0a90dbcc409cb60b3d3e821b52aa8706a65017768
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-8.0.1` - linux; amd64

```console
$ docker pull couchbase@sha256:1c8095584ed8c77fb8fe85aa4fed72f40ff26b26f5ec66c2aae5bb65731e152d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 MB (502446441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcca49476e1c25864083e04a6d240e0f1e0ebeec97167cab207f8941625ba9d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:47:59 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:47:59 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:47:59 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:47:59 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:48:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:48:32 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1
# Tue, 07 Apr 2026 01:48:32 GMT
ARG CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:48:32 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:48:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:48:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:49:19 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=ca9aa048cb12e3d89d982c3139a4d65a94f3820691435762d34d5d1117840333            ;;          'amd64')            CB_SHA256=e4dc69cb42e0e8d8de80519f18768e0b0acc683d5e1f10c609583a8f76609507            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:49:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:49:20 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:49:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:49:20 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:49:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:49:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:49:20 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:49:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:49:20 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:49:20 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:49:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b410b87f365cfc797b3f3fcb4fbeb378cce638714232ad55cf28c58e77c9fe`  
		Last Modified: Tue, 07 Apr 2026 01:50:04 GMT  
		Size: 43.8 MB (43816242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7d6fbfcc5da970ed758a4e5432e7421681f25ab5030528f010f1354ea602e1`  
		Last Modified: Tue, 07 Apr 2026 01:50:03 GMT  
		Size: 878.1 KB (878096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658db9fb1f20653e488de706c7f7f765db992231781b07d09b9bb900a8feb605`  
		Last Modified: Tue, 07 Apr 2026 01:50:02 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b61cb883891acaba433bf97c7532e666672772255f688cd2bd09f1df826984`  
		Last Modified: Tue, 07 Apr 2026 01:50:11 GMT  
		Size: 428.0 MB (428011662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b14d4b548071b356d85d9223bc0cefee8ef95e33de6c40bd40e0b558c522af2`  
		Last Modified: Tue, 07 Apr 2026 01:50:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37ffeed4b7a327f319d37d75d925ccfbf58343bffe365644e33af2c30700538`  
		Last Modified: Tue, 07 Apr 2026 01:50:04 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8165e396a83e1ad3249adec75a744f12dab301f4beffe314cb55b752959ecd60`  
		Last Modified: Tue, 07 Apr 2026 01:50:05 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1e65108a3344964509f24cd11406c4475ee19899f2af5fad76edf3d39e404a`  
		Last Modified: Tue, 07 Apr 2026 01:50:05 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f751f2dd61524b4205f886236e0064bb7fd1b422137ed1625be671318dfa1179`  
		Last Modified: Tue, 07 Apr 2026 01:50:06 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e38415858849c68430e9561426b1fef17d66693145a2d8303122d9be15bd6d`  
		Last Modified: Tue, 07 Apr 2026 01:49:54 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-8.0.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:c58b7d03be6a36f812799be4c54050aa86d17c53ecbe3a02a19096463634abab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60322f763ecaa7d7103d9541cc2fb721d51efd581bf8b4ec8a427ba257069cc`

```dockerfile
```

-	Layers:
	-	`sha256:d9bfdac1b3befb095dc30b807826aec2fbc348e026fb4ec3bd24100df4abb338`  
		Last Modified: Tue, 07 Apr 2026 01:50:02 GMT  
		Size: 37.5 KB (37519 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-8.0.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:83db24ae3f5a47bd0af4f713f03db0656290b3eb45959fdf74ad493307d80f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.1 MB (472063437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd2ae6f7fb26132e4673e492ca12fe3ee51b5ed219bff304f9eea674d1a7efa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:50:59 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:50:59 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:50:59 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:50:59 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:51:33 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:51:33 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1
# Tue, 07 Apr 2026 01:51:33 GMT
ARG CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:51:33 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:51:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:51:33 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:52:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=ca9aa048cb12e3d89d982c3139a4d65a94f3820691435762d34d5d1117840333            ;;          'amd64')            CB_SHA256=e4dc69cb42e0e8d8de80519f18768e0b0acc683d5e1f10c609583a8f76609507            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:52:05 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:52:05 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:52:05 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:52:05 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:52:05 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:52:05 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:52:05 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:52:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:52:05 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:52:05 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:52:05 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ae86a00b6403ae4940ab553c56e761247f4b7c4c1d760893d373d80afd6246`  
		Last Modified: Tue, 07 Apr 2026 01:52:44 GMT  
		Size: 43.6 MB (43633557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf0ecea2d6c1d2d789b8cad2aba7eef3dfdc7cff12e159be93b6ad1755573c7`  
		Last Modified: Tue, 07 Apr 2026 01:52:42 GMT  
		Size: 765.0 KB (764975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881ec049db91ace54215806cf0b75550046ce01bcee9d0bd537b8665fef0885e`  
		Last Modified: Tue, 07 Apr 2026 01:52:42 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482a7b6aef02fde6feb8795d40c14b2924a629a6a85ce706f1319f738e61b459`  
		Last Modified: Tue, 07 Apr 2026 01:52:50 GMT  
		Size: 398.8 MB (398783846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a23531c59491c66676241f75aa62685e544f564dfe476198ea85e9acc98922`  
		Last Modified: Tue, 07 Apr 2026 01:52:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f19b76444c08cbe3147f6f512980e2a409ea65048c63c73a0d855fb497ffa9`  
		Last Modified: Tue, 07 Apr 2026 01:52:43 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63aa7ae9ffd60490876ea2f6145a014608f184d19ff7d81a675951ffc7031d`  
		Last Modified: Tue, 07 Apr 2026 01:52:44 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c6faecec9d12e1b65d3af1ecbf4100f609ca452152c319d60b7c0165c7e811`  
		Last Modified: Tue, 07 Apr 2026 01:52:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac312607912dc4674f06c273da7b46235bc5cf3ced5c19c54ab5a425c2816f81`  
		Last Modified: Tue, 07 Apr 2026 01:52:46 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d028d527118d86fe1e98b6c7ac005cf1341d938c28baf9df57ae9b7637587a`  
		Last Modified: Tue, 07 Apr 2026 01:52:46 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-8.0.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:fba08e976f6baa2682f5964eb9a9833e2c4a428c854ddb44ffe29f57d75935dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9daf57f65af3518bca5e7c7beb3b15d82f1c19568518d5a3d9f6c88c0c05ed`

```dockerfile
```

-	Layers:
	-	`sha256:64635db47e39eddd4dcbeff77abc7fc43add9fc2262870dfa40416053d34f0ad`  
		Last Modified: Tue, 07 Apr 2026 01:52:42 GMT  
		Size: 37.7 KB (37704 bytes)  
		MIME: application/vnd.in-toto+json
