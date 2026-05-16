## `couchbase:enterprise-7.2.2`

```console
$ docker pull couchbase@sha256:e1504f0ebdb3ac0b489ec1dba00ad293f82d5cdb171fcf9eec20b5ea4b220a95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:bf1555bdf0059435b029efc522d4e411d796d2283b93de3ffdc10f30d5ac55dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.8 MB (703779415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc288f6607e2277d7ec8bb19643d2da630fd6da9ec09c8ed6bacb48c85d30e77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:11:41 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:11:41 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:11:41 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:03 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:03 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Fri, 15 May 2026 21:12:03 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:03 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:14:21 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:15:19 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:15:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:15:20 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:15:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:15:20 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:15:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:15:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:15:20 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:15:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:15:20 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:15:20 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:15:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90990141e6d7563753bd81b76e64d58dbbc851ada655fd577b06e1374f2fb2b5`  
		Last Modified: Fri, 15 May 2026 21:14:00 GMT  
		Size: 39.3 MB (39306775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129e50c56e0d29c29a793398007883f832940bd7fffe8eae7a537473deb47f25`  
		Last Modified: Fri, 15 May 2026 21:13:58 GMT  
		Size: 926.8 KB (926768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdec16cfce75c89bce28275270b2dbf9f9020a90f9d8bef4182c003452c1988`  
		Last Modified: Fri, 15 May 2026 21:16:02 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b0ea4b74cd0ade50ccbad321f163ea008acea6dc9a128e263b56b20e4835b1`  
		Last Modified: Fri, 15 May 2026 21:16:15 GMT  
		Size: 633.8 MB (633804009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd0902b3593a783906cb90173b1f2a1b0c1c489cbf063eee0a51280358b7ff2`  
		Last Modified: Fri, 15 May 2026 21:16:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0e804ca62af0d070c37d9cf149855e6b5d37af411be70405b92e28a9379f72`  
		Last Modified: Fri, 15 May 2026 21:16:02 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45442496d83844a57c72f01f06268140f3de121387654dd94a6ad6558f082f05`  
		Last Modified: Fri, 15 May 2026 21:16:04 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c6ff088849b47f5d511136fdac43ec8653c82c7952ff73c238f86b7c2bd8a6`  
		Last Modified: Fri, 15 May 2026 21:16:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dac70e76b70e4f804f746b2eaeecf4911fc9953b9d82f9a0366a255357a40e2`  
		Last Modified: Fri, 15 May 2026 21:15:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cceb0f6324001590aa247a48bc1c8f79208f78b54a178001610634a0286e83`  
		Last Modified: Fri, 15 May 2026 21:16:04 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:fd27b08a3492117047bbb32cc586fbdf31d168ea7bc3b2960eef22acfb198025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5465e8065c7515b6796899024b4d3bca5231547e9163639f6867f5e8933b2`

```dockerfile
```

-	Layers:
	-	`sha256:a43b532ba6698be8f1f0d1ae0fe140538aa3263f5939b6cec0398f55cd74293b`  
		Last Modified: Fri, 15 May 2026 21:16:02 GMT  
		Size: 37.5 KB (37522 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:95571746671eeeb7b50050d7795f86e0fb832a1d27d189257e7453698cd45b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.1 MB (674103392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d19e019ef4cb1d21b4ddceec39801124ee32c5cb3d4433a518e1141bace201`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:50 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:12:50 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:12:50 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:12:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:13:18 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:13:18 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Fri, 15 May 2026 21:13:18 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:13:18 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:13:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:14:46 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:15:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:15:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:15:45 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:15:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:15:45 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:15:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:15:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:15:45 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:15:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:15:45 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:15:45 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:15:45 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ac4f8b5c12082a594f00293a99b5590825831b6cdf4b23da552629309f60ec`  
		Last Modified: Fri, 15 May 2026 21:14:33 GMT  
		Size: 38.9 MB (38866828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88879cc8c83fe48b2bdf7d488284593679c39c2e7679ad14eba4aef572a8a679`  
		Last Modified: Fri, 15 May 2026 21:14:31 GMT  
		Size: 775.3 KB (775334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090451186b665bc0f6a5213d96400e58ef41f1e37601288d549b34c5326acb7b`  
		Last Modified: Fri, 15 May 2026 21:16:27 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b677ea44de4c6597ed6bb927bc03a773d8f9d7e71ba64b4d9d285124e7c59707`  
		Last Modified: Fri, 15 May 2026 21:16:41 GMT  
		Size: 606.8 MB (606849422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaad0b1bf053c0d74781d0a6cc5ee30dd0e7d1823cf010b2344399ab816a188`  
		Last Modified: Fri, 15 May 2026 21:16:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101d65dc7444d315059b7d97cb52b04a215896ba92a299232247e316b33fbc5c`  
		Last Modified: Fri, 15 May 2026 21:16:27 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8f89e47d8b22f6d68e0c6815ca1ee8c0193d56243dda118dcf6dc16362a0fd`  
		Last Modified: Fri, 15 May 2026 21:16:29 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458d59aa10216dd975e50474de0739885780e0adb87e12b5e80ccb74fdde493f`  
		Last Modified: Fri, 15 May 2026 21:16:29 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15902d471158f45df76ec4d55f0bd8d4b159ce00fb724c57637d94b04a6f1707`  
		Last Modified: Fri, 15 May 2026 21:16:29 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8677cdab82d094b4f924906b75e5fdf13ee54e0e32e967def083526177a644d4`  
		Last Modified: Fri, 15 May 2026 21:15:55 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:512c56aaa789c1ae87b52d3d70d3f454aa4713b62f2a8580c5efd92ba3a4fbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1924454dba16376fa26f2d2d3d512ea5d5fb3c2d05bb85da2b30670df0bbb9f7`

```dockerfile
```

-	Layers:
	-	`sha256:8201628cc71deca229d1406c068be384ef7d480eb9bf3c3eaf1aefbc3d9c1d74`  
		Last Modified: Fri, 15 May 2026 21:16:27 GMT  
		Size: 37.7 KB (37707 bytes)  
		MIME: application/vnd.in-toto+json
