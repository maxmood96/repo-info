## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:538ca8d51f155aed7f8947fb9f211c38549e5e3b0de0b85af0d94026bda5ff28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:38c66b5b289d5220a91b0870ad70d04eafa4569135b60d83d06aa494925004c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **799.2 MB (799242816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559fa4442091a711c41cab0a46dcfc4183169705c730d95351f80402b39ed71d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Aug 2025 18:24:10 GMT
ARG RELEASE
# Wed, 13 Aug 2025 18:24:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 13 Aug 2025 18:24:10 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 13 Aug 2025 18:24:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 13 Aug 2025 18:24:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 13 Aug 2025 18:24:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=8baaddc8bedc7223db7995514996d87388b23fe6f39fecac7008ee8800be64f7            ;;          'amd64')            CB_SHA256=7bd09a72ec12c4dde2b78cf5354db814b58a9723ba3ba95b370d5d2320807a94            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Aug 2025 18:24:10 GMT
CMD ["couchbase-server"]
# Wed, 13 Aug 2025 18:24:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 13 Aug 2025 18:24:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8b5ba4c2cd32ca2620ba825b2e1488bbbf2187bdf25b85bb95b09178dc1f70`  
		Last Modified: Mon, 15 Sep 2025 22:14:53 GMT  
		Size: 43.8 MB (43806774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ca6ea6e8d5845e9e07426d057187b20f898074092493744456128ee0b25be8`  
		Last Modified: Mon, 15 Sep 2025 22:14:49 GMT  
		Size: 877.8 KB (877815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b480178de04c1bc8abfe5ce66eb99343688a440c4cd2e6893c7fa07379f67bd8`  
		Last Modified: Mon, 15 Sep 2025 22:14:49 GMT  
		Size: 3.7 KB (3726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e609d856e0f76f188a0af49d96e14edc8c92c212820de09bbbb1fd1c3a125fe1`  
		Last Modified: Mon, 15 Sep 2025 23:32:26 GMT  
		Size: 724.8 MB (724827790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5853d0df4c882303b304c2c19fbcace644deee28e6fd74eee31a576ed9c16968`  
		Last Modified: Mon, 15 Sep 2025 22:14:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da2ff9b54dd4a76e97d6d931264aa5849b7a41d43ba69ab1a9cedbecbc9f067`  
		Last Modified: Mon, 15 Sep 2025 22:14:50 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925dd5e35e512b6219b2129d0dcedec135cfd423c7a7c84f63508b69c51457f`  
		Last Modified: Mon, 15 Sep 2025 22:14:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f325ea15b033a21c4db6acc40d3f10e48a0200a1429a20a339f7501e0fc42369`  
		Last Modified: Mon, 15 Sep 2025 22:14:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccac3c045ce7b43ffc238d0ea2a96df27ab606810ae96d7df4a9ef7ef59b99f`  
		Last Modified: Mon, 15 Sep 2025 22:14:50 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6b3af3d9cfdd5df708df0e216ed73a1ede9273a426cf040fd8b2538f4ac172`  
		Last Modified: Mon, 15 Sep 2025 22:14:50 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:7badc1ed5b9e704b01fbe64616c69230f48925c27cc7b2839cf3d666a37bd77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e26fddfbaaa2f7aa11086fc0dfacf35abfb29acc502ed339ec49120348aafdc`

```dockerfile
```

-	Layers:
	-	`sha256:350be1f0135c3851f4a0e3c3714dc74273b62e99adcf48e3bdd1ca27b4ca8d6a`  
		Last Modified: Mon, 15 Sep 2025 23:31:55 GMT  
		Size: 38.2 KB (38181 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:6ef84b9f29da6faad69624d16ab05a2ae5733508d5d3e1cc3807b1f01e04716f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.5 MB (769539153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ec3d95a981fc0172487a5e135591c3875b7efb40c4524c9f7a015f320470db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Aug 2025 18:24:10 GMT
ARG RELEASE
# Wed, 13 Aug 2025 18:24:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 13 Aug 2025 18:24:10 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 13 Aug 2025 18:24:10 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 18:24:10 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 13 Aug 2025 18:24:10 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb
# Wed, 13 Aug 2025 18:24:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 13 Aug 2025 18:24:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=8baaddc8bedc7223db7995514996d87388b23fe6f39fecac7008ee8800be64f7            ;;          'amd64')            CB_SHA256=7bd09a72ec12c4dde2b78cf5354db814b58a9723ba3ba95b370d5d2320807a94            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.7 CB_PACKAGE=couchbase-server-enterprise_7.6.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 18:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Aug 2025 18:24:10 GMT
CMD ["couchbase-server"]
# Wed, 13 Aug 2025 18:24:10 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 13 Aug 2025 18:24:10 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dcae5d6dc4a5bd6622ea807742fced17ab3a60962799def67e2ecc47a202a6`  
		Last Modified: Mon, 15 Sep 2025 22:14:36 GMT  
		Size: 43.6 MB (43624494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79134233a64b5129132a768c40de30b7c3beb3341f5efd7e5299e7d2f2dfb938`  
		Last Modified: Mon, 15 Sep 2025 22:14:34 GMT  
		Size: 764.8 KB (764803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a93d8ec1eda2b7ca399d314dae55b819c78174bf4962d78d0c4efbdeaca5c7`  
		Last Modified: Mon, 15 Sep 2025 22:14:34 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8748984a3c33536e407007c408db1881e822295f126bf4412926f3607c13a17`  
		Last Modified: Mon, 15 Sep 2025 23:32:33 GMT  
		Size: 696.3 MB (696281556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a241d2d17b34de96ce6d900c43c8dbc554024dc2bfc494a4f0abecd8687238b7`  
		Last Modified: Mon, 15 Sep 2025 22:14:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e41a847a66122287fa6c16ffa19829e752d3b5dd7d609f57443794a856327b4`  
		Last Modified: Mon, 15 Sep 2025 22:14:34 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50830a1ced44181704a474e65995d14aee493cc243dc45b2d6130768b5cc717`  
		Last Modified: Mon, 15 Sep 2025 22:14:34 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12ff620be47119efd41d0a52bdef7c2081c744e82909ed5e42bd91c7256c5b8`  
		Last Modified: Mon, 15 Sep 2025 22:14:34 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a172d6cbf3ec69d361cec1086eef6af798b02e7cf1b39c56fb88419f955ceb`  
		Last Modified: Mon, 15 Sep 2025 22:14:34 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac65c9c0d4358c4e047649af2de09c983bba07d2baa67715328428c1d11560f`  
		Last Modified: Mon, 15 Sep 2025 22:14:37 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:4e8d2869b20a165b03177a0eba7bfaadaeb49d932063388a9c3dd17f9f421044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 KB (38390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae42e5b4a00ef3e235524c022159936cf15e362707e1837314636ff727b0642b`

```dockerfile
```

-	Layers:
	-	`sha256:6ed317aa99634bf9d5438d62467fef06cc4b791f7dc877960a0fbcbb33161d2b`  
		Last Modified: Mon, 15 Sep 2025 23:31:58 GMT  
		Size: 38.4 KB (38390 bytes)  
		MIME: application/vnd.in-toto+json
