## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:102cc2c5401d87ee78d4fc04ef9bf1cc57e3e17d5e9fd2661ff18c13004cf705
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:0430ba736a625b8850cfaa2de6e7c0e66854dc62f6cd3702869a2579bda7c8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401083895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd66ce087b8489a34bb08fd07d7cd2115143d29323668c26aca9f1bf62a27b1`
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
# Fri, 15 May 2026 21:12:30 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:12:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:12:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:12:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:51 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Fri, 15 May 2026 21:12:51 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:51 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:14:13 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:14:49 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:14:49 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:14:49 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:14:49 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:14:49 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:14:49 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:14:49 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:14:49 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:14:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:14:49 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:14:49 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:14:49 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b4d64f82c03937e66443d14a7af4e114acda668cfe6f940c63274cb4393a2`  
		Last Modified: Fri, 15 May 2026 21:13:59 GMT  
		Size: 39.3 MB (39307598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317d7e0a407ffd90548026b86020f5200040af817079fd4e040c6ab1b89cefd`  
		Last Modified: Fri, 15 May 2026 21:13:58 GMT  
		Size: 926.8 KB (926766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587941c1990733f9b215f5f1e69704add1bd11f195d00ef181237b2617813cd5`  
		Last Modified: Fri, 15 May 2026 21:15:20 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d166e12851a378c48457ecc89f6175475ee0ae2a5bf7fcc57f0b91b305d94555`  
		Last Modified: Fri, 15 May 2026 21:15:27 GMT  
		Size: 331.1 MB (331107663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9598a0568e79b4dd1fb659104032a8201f8a747a018807fa5b0d80c1a91fee09`  
		Last Modified: Fri, 15 May 2026 21:15:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fc9d23e1ef695ff1dddf22521a05c2e08a737d891371fe6e030d60acd020f2`  
		Last Modified: Fri, 15 May 2026 21:15:20 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b54e36e5389408da7a0a621470790d56da82157b598ad6e1cc061b7bc49ffc`  
		Last Modified: Fri, 15 May 2026 21:15:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee5af65331d193ca75a5b21c44c1cb2b655fcc2ac04e95848e4bac52b6bf95d`  
		Last Modified: Fri, 15 May 2026 21:15:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5ffc8a0d406320088279be10485e06cbaf44e3250b392fecf0deeabb184e2a`  
		Last Modified: Fri, 15 May 2026 21:15:21 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd86df376ad70d195f63054c0b01818912b35b7e61a73db9c4bccc8d68e1c79`  
		Last Modified: Fri, 15 May 2026 21:15:22 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:5e21d44449b0ddcadd8600c867115ea8526cb7eb2dde475a86431d1d80bddfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0378c485017961c156789f70a6b2e7bbdc7b12218317b87b763bd942b72ed82e`

```dockerfile
```

-	Layers:
	-	`sha256:a53fd20a77dd8a18f67446215ec70d78e7f36b2c372f96d9f24660f8dcdc9522`  
		Last Modified: Fri, 15 May 2026 21:15:20 GMT  
		Size: 37.2 KB (37209 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:2e8671a1ae7afe4fb957f37aa09456d5dba4092ba29abf00d354aea4aa192836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.1 MB (380149249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737aba4405934cd082be67c6ade6818314af3923296722e15ccc2cc3c5a5a2ca`
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
# Fri, 15 May 2026 21:11:33 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:11:33 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:11:33 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:11:33 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:16 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Fri, 15 May 2026 21:12:16 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:16 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:14:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:14:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:14:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:14:50 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:14:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:14:50 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:14:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:14:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:14:50 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:14:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:14:50 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:14:50 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:14:50 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaba7a23fadf35a60ad3cd89c98f7edea76c227e350bf36320bf1d82efe1cf31`  
		Last Modified: Fri, 15 May 2026 21:13:59 GMT  
		Size: 38.9 MB (38866771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9025a0be09ab3e0dd351d7ef500e3772832b6a7d43fed3908414da6769170466`  
		Last Modified: Fri, 15 May 2026 21:13:57 GMT  
		Size: 775.3 KB (775315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf4f003290b7580a4e033f5db98f446799c583ceded79a286d43102a6e56fc7`  
		Last Modified: Fri, 15 May 2026 21:15:21 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f25f1ad476c0ab40b3604702b3e4f9131d5a12598c7534855a955181da58b5`  
		Last Modified: Fri, 15 May 2026 21:15:28 GMT  
		Size: 312.9 MB (312895358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8218c45fe24c404d31349c5d9af8a0689c78f09f7d2f6263955497930a27e6c9`  
		Last Modified: Fri, 15 May 2026 21:15:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee00697eb8548033d74d87acb5f811f879b60245d6746cee43c82f495ac9b80d`  
		Last Modified: Fri, 15 May 2026 21:15:21 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06285da3e300e422ca01354d25fee5de06dda5d150103c6e2ac8fbb60e767763`  
		Last Modified: Fri, 15 May 2026 21:15:22 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c7928c90362bcd842f1eae588a244f393f5f01b35ac6c282c88a95d4def1f3`  
		Last Modified: Fri, 15 May 2026 21:15:22 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d74060946bcd62cd8907d0d2e8ff3b3dbd2b1cdd889bd9f3c98654a5801f9b6`  
		Last Modified: Fri, 15 May 2026 21:15:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195e7888bcbd172f769db1eaa170118e99848a324e0498ef13ab414a1050c11d`  
		Last Modified: Fri, 15 May 2026 21:15:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:e89e3c5575f1fd9c859d734c493b44802764319519f8daa8d907c5e2e3e63ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cd0c857ad34dc99ce40069b0d41485fe7a0eee1e031c8fd4a49b4a8f76424`

```dockerfile
```

-	Layers:
	-	`sha256:5662adf577b54fb5d7a55dc552fef8688ac49e949c5bd11b3863827f4d623c60`  
		Last Modified: Fri, 15 May 2026 21:15:21 GMT  
		Size: 37.4 KB (37382 bytes)  
		MIME: application/vnd.in-toto+json
