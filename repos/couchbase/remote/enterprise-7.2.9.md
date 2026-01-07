## `couchbase:enterprise-7.2.9`

```console
$ docker pull couchbase@sha256:65ce3066dd1d66298afc0e1f43775dbf5e1b53eb6c18f2356fbf4d931f818720
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.9` - linux; amd64

```console
$ docker pull couchbase@sha256:7c245224f620104df4376d1161d1a1acaad19d6db39e6a10c601dc6cc0e1c0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **714.9 MB (714893460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567e47717cd6433f84fa2b4bd5a79c28242fcc0731544666742256666a73757c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 23:36:13 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 06 Jan 2026 23:36:13 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 06 Jan 2026 23:36:13 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 06 Jan 2026 23:36:13 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 06 Jan 2026 23:36:38 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 06 Jan 2026 23:36:38 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9
# Tue, 06 Jan 2026 23:36:38 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb
# Tue, 06 Jan 2026 23:36:38 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 06 Jan 2026 23:36:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 06 Jan 2026 23:36:38 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 06 Jan 2026 23:37:03 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1f894b910a15d727c7f7d1c2daa3b3e0d4107dc4d6aff5f353aa501006875e31            ;;          'amd64')            CB_SHA256=af822187cd62b562b54d46df3f8b1161a1e7ee753ebf9a22e3da2d74ddf644f8            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 06 Jan 2026 23:37:03 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 06 Jan 2026 23:37:03 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 06 Jan 2026 23:37:03 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 06 Jan 2026 23:37:03 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 23:37:03 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 06 Jan 2026 23:37:03 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 06 Jan 2026 23:37:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 23:37:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Jan 2026 23:37:04 GMT
CMD ["couchbase-server"]
# Tue, 06 Jan 2026 23:37:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 06 Jan 2026 23:37:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b4982bd7f2b678645c1e699d56d610244a5afa12245ee17b4b03a1abfa6d98`  
		Last Modified: Tue, 06 Jan 2026 23:38:35 GMT  
		Size: 45.9 MB (45945714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2299f82bb358ac8508e9e7eba8568bc4fc7390b61fdcad5252eb0b2b9351eb65`  
		Last Modified: Tue, 06 Jan 2026 23:38:30 GMT  
		Size: 878.8 KB (878775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baafd7615d695193236e68ea287d6824386b5cddcfd80b968d72a1045b62d22a`  
		Last Modified: Tue, 06 Jan 2026 23:38:30 GMT  
		Size: 3.7 KB (3726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948eb4ce0ff2e397720ab3fa5b2d4a9e5a1a4adcf12d7ce2a73267d8d22fdf8d`  
		Last Modified: Wed, 07 Jan 2026 00:10:29 GMT  
		Size: 638.3 MB (638337291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95092f59fdd46637a711f15408f0e6844e3686730036328e99a46c7bb8d93d3d`  
		Last Modified: Tue, 06 Jan 2026 23:38:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7274fa6debd591ef8c8ca45157f3202c3022d0c8541597ee4bbce1b9f54f3c`  
		Last Modified: Tue, 06 Jan 2026 23:38:30 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fe72ad3c3138b90379729f898e197a3f2901b1220e270b4cf023cf2e21cc4c`  
		Last Modified: Tue, 06 Jan 2026 23:38:30 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6496989238184f310db07cfdae651c9e9f808f1b6497dcfc8b87ff4dc480414f`  
		Last Modified: Tue, 06 Jan 2026 23:38:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8dd72d9225f104f05d6170d6b203328d0a245b13918c9cdeb160baba6ee52b`  
		Last Modified: Tue, 06 Jan 2026 23:38:30 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022153c2b16365b134cd038006bd5b7de40430e7a2cc75e11e08894706ccb760`  
		Last Modified: Tue, 06 Jan 2026 23:38:30 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.9` - unknown; unknown

```console
$ docker pull couchbase@sha256:7d287748538d77c369ad408532ba78af9a14f7d9c410fcf54c3a2bf52b85c7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ee526294d47f2bda3592bb96f373b074700f3f0c527ed8b303bc3c22740658`

```dockerfile
```

-	Layers:
	-	`sha256:d42ed756dea37b869638c0c22ed2b340330ff78405d58f379898a28485e0d15b`  
		Last Modified: Wed, 07 Jan 2026 00:31:26 GMT  
		Size: 37.5 KB (37522 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.9` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:e40120a04abd229881404986f6bb95334cdaeddb6acfb4164f1ed6aa71d06400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.1 MB (688099072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4ba9b6cd77e82924cb2650d426107f4b5a45fbcbb26990ede77f33b319e23b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 23:35:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 06 Jan 2026 23:35:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 06 Jan 2026 23:35:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 06 Jan 2026 23:35:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 06 Jan 2026 23:36:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 06 Jan 2026 23:36:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9
# Tue, 06 Jan 2026 23:36:28 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb
# Tue, 06 Jan 2026 23:36:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 06 Jan 2026 23:36:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 06 Jan 2026 23:36:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 06 Jan 2026 23:36:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1f894b910a15d727c7f7d1c2daa3b3e0d4107dc4d6aff5f353aa501006875e31            ;;          'amd64')            CB_SHA256=af822187cd62b562b54d46df3f8b1161a1e7ee753ebf9a22e3da2d74ddf644f8            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 06 Jan 2026 23:36:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 06 Jan 2026 23:36:56 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 06 Jan 2026 23:36:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 06 Jan 2026 23:36:56 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 23:36:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 06 Jan 2026 23:36:56 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.9 CB_PACKAGE=couchbase-server-enterprise_7.2.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 06 Jan 2026 23:36:56 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 23:36:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Jan 2026 23:36:56 GMT
CMD ["couchbase-server"]
# Tue, 06 Jan 2026 23:36:56 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 06 Jan 2026 23:36:56 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79455423a48ba38182b4ab3fff3bbe9620568649dababebf9e3df761ff173daf`  
		Last Modified: Tue, 06 Jan 2026 23:38:37 GMT  
		Size: 45.8 MB (45837650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e432c5d1066091ffad4f17f5709321637c3daea8960b4235e210418deadffc0`  
		Last Modified: Tue, 06 Jan 2026 23:38:14 GMT  
		Size: 765.6 KB (765641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccd3f8ec30a5bbf12a435bc23fa62c96f66dfa6b9d47d04686ec515ffee46d8`  
		Last Modified: Tue, 06 Jan 2026 23:38:13 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a4fbc257f83be2d67a06adf66b705fcd23b4dc381951d0f0068d29d4b2e239`  
		Last Modified: Tue, 06 Jan 2026 23:39:03 GMT  
		Size: 612.6 MB (612626841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae12faf6f67389e47f9169d1341fb6f782c4b5b97fca069530f052380c69b7a`  
		Last Modified: Tue, 06 Jan 2026 23:38:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d68f8e9787fa804a8fed3e708a5b9604293e9c82ca94db7e8f5a7a8250ee6a`  
		Last Modified: Tue, 06 Jan 2026 23:38:14 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5b3720a5f1ea41eaee112051ee26b10f2235c97b77a5ba40b8a3e0a5ab9263`  
		Last Modified: Tue, 06 Jan 2026 23:38:13 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8a1dee9e5fcb92c13e10d56caa660b247885d524155fd0f425eab144229a94`  
		Last Modified: Tue, 06 Jan 2026 23:38:14 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c9b829dcb199cc01bf98f6295c86acd3ed06ac07d7c56090e409dbb64f617c`  
		Last Modified: Tue, 06 Jan 2026 23:38:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c381fd69a902fcf20bbd485571cd84a6b87155c681c193e03bdd65ed6b46c6ee`  
		Last Modified: Tue, 06 Jan 2026 23:38:13 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.9` - unknown; unknown

```console
$ docker pull couchbase@sha256:b0e1acb48aef310c0639801027c2a511b94b834ae1187dad368457f7b9c62100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebe03076c3b57d3d2c24108b577be6b620dd7b29b4e324221b24a4ef8187463`

```dockerfile
```

-	Layers:
	-	`sha256:b90b2035ea21769d44b6859b3296e9bfeb477a8edd4a04471e425f083137f156`  
		Last Modified: Wed, 07 Jan 2026 00:31:29 GMT  
		Size: 37.7 KB (37707 bytes)  
		MIME: application/vnd.in-toto+json
