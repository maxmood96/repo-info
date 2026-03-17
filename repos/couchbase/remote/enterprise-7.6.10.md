## `couchbase:enterprise-7.6.10`

```console
$ docker pull couchbase@sha256:d52e3cbc36c7b353a0409b0c2107a9961d6aeae2259d43c38b4b68d8c52c0936
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.10` - linux; amd64

```console
$ docker pull couchbase@sha256:89b609de9cf2d37174e795734add6b75a6ae4e320e779191dff9c483a1d2dc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.5 MB (835485886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734dd73daa05b10b04515be007f8d9fc378535bdf0b8e18aa3f1749881317781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:16:00 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Mar 2026 01:16:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Mar 2026 01:16:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Mar 2026 01:16:00 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Mar 2026 01:16:27 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Mar 2026 01:16:27 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10
# Tue, 17 Mar 2026 01:16:27 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb
# Tue, 17 Mar 2026 01:16:27 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Mar 2026 01:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Mar 2026 01:18:15 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 17 Mar 2026 01:18:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=680d6833172db7691aa0f9562aa50e044214f97cd8a785b410e828a840ce38bc            ;;          'amd64')            CB_SHA256=80938b3c86eb4cf412d9eb80b6494d96d32ce90555dc8536e0fb44a884f453ef            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:18:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Mar 2026 01:18:43 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Mar 2026 01:18:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Mar 2026 01:18:43 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:18:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Mar 2026 01:18:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Mar 2026 01:18:43 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:18:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:18:43 GMT
CMD ["couchbase-server"]
# Tue, 17 Mar 2026 01:18:43 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Mar 2026 01:18:43 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea359c7bc5132ef267a1ec0c8ba9449e36363249afe55242bf1681b5f448bd`  
		Last Modified: Tue, 17 Mar 2026 01:17:49 GMT  
		Size: 45.3 MB (45283684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed06330a588fc24653cd0745138885145f45ff8474c2bbf6dcd54200066e9d4`  
		Last Modified: Tue, 17 Mar 2026 01:17:47 GMT  
		Size: 878.5 KB (878533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99582ec0354919bdefbaef51a77d2eb860ad2c0e084427271e384ecd06c4577e`  
		Last Modified: Tue, 17 Mar 2026 01:19:33 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120a46bffbe1d197e4bd0aac2b3073d28ef6fdc56c4345f59528f20e4e1cd314`  
		Last Modified: Tue, 17 Mar 2026 01:19:48 GMT  
		Size: 759.6 MB (759584691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee5d8c0fccbd8203886623493a6edf5cf22a5048d1c473a149c64e7b1636fd5`  
		Last Modified: Tue, 17 Mar 2026 01:19:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66bc46cfb08759811cad34768afcbc5596d8a43e8bc1dd7509cd4e3c1b6359d`  
		Last Modified: Tue, 17 Mar 2026 01:19:34 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fd63b54d75b297b653f2964200419f9cc7485113a635748c01cc44d378fc52`  
		Last Modified: Tue, 17 Mar 2026 01:19:35 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddef20dc1a35779da403bdfa0135b4798b8041129610c079468efa4f56906502`  
		Last Modified: Tue, 17 Mar 2026 01:19:35 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155bf6f57019256dc703774499bbe604f85ef7434cec5d32dc85c0615ea6982`  
		Last Modified: Tue, 17 Mar 2026 01:19:35 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a053b2e82cbd13baffaaaff31fdf1d0b6d89ea645e000d3397cdeaa893f4dae4`  
		Last Modified: Tue, 17 Mar 2026 01:19:36 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.10` - unknown; unknown

```console
$ docker pull couchbase@sha256:170a6d54e3ac5da59dda6b82559aee297183d64df0a46665c8142340080d621c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9ac45c6325261b1eec611c99df9bf8e12f88e77ab13569acd82a4b4b0b6519`

```dockerfile
```

-	Layers:
	-	`sha256:1d24bdd30b8da17de2ae3f1f1c8c78f038f4bb5073f1518b0dbcaaa92f624b06`  
		Last Modified: Tue, 17 Mar 2026 01:19:33 GMT  
		Size: 37.5 KB (37545 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.10` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:abd977b786b7acb05a91eda096834dcdfe68f8cf2c835e40f6bab89beef16f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **798.4 MB (798369791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5117a6d3676064ab1a733080501b3f575078b30ecda51471a68ab5eb04ea61f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:16:17 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Mar 2026 01:16:17 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Mar 2026 01:16:17 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Mar 2026 01:16:17 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Mar 2026 01:16:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Mar 2026 01:16:51 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10
# Tue, 17 Mar 2026 01:16:51 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb
# Tue, 17 Mar 2026 01:16:51 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Mar 2026 01:16:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Mar 2026 01:18:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 17 Mar 2026 01:19:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=680d6833172db7691aa0f9562aa50e044214f97cd8a785b410e828a840ce38bc            ;;          'amd64')            CB_SHA256=80938b3c86eb4cf412d9eb80b6494d96d32ce90555dc8536e0fb44a884f453ef            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 01:19:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Mar 2026 01:19:36 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Mar 2026 01:19:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Mar 2026 01:19:36 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:19:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Mar 2026 01:19:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Mar 2026 01:19:36 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:19:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:19:36 GMT
CMD ["couchbase-server"]
# Tue, 17 Mar 2026 01:19:36 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Mar 2026 01:19:36 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27dd98ff07a4275204f8327bf03548dd683db5a390305673792c0b74d16d147`  
		Last Modified: Tue, 17 Mar 2026 01:18:30 GMT  
		Size: 45.2 MB (45172818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94637b418fc0848ec414ce052180ccba993c81d9d670487fc213aebd6770bc22`  
		Last Modified: Tue, 17 Mar 2026 01:18:28 GMT  
		Size: 765.5 KB (765532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61476421704f652df0d99ad4bed3dddc806a29b29136b01d6a2b5d470b82bf46`  
		Last Modified: Tue, 17 Mar 2026 01:20:27 GMT  
		Size: 3.7 KB (3721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f8befe2f31762ea607ade3f493247ee48793e161d067ecff05140ba5616d41`  
		Last Modified: Tue, 17 Mar 2026 01:20:52 GMT  
		Size: 723.6 MB (723554744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491b1230528bd8ab55a5f0e3557da81681d09383dac4a6f6f61218c85d635084`  
		Last Modified: Tue, 17 Mar 2026 01:20:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c68ab1d89cdc9549f354199d5a222c5dbcfaebf8a930e9b5a5d8012d13ceffa`  
		Last Modified: Tue, 17 Mar 2026 01:20:27 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afce6297787884379e8b0bd1d3b696e0f99fa9dcf77df180f68ce6cd72f7bc52`  
		Last Modified: Tue, 17 Mar 2026 01:20:28 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05347ae9395ed9738488dc5a5ccca10c5805f1d918ab9103d63ffde093b8296`  
		Last Modified: Tue, 17 Mar 2026 01:20:28 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62520a56f5ea04207ce4432b83700010d79824c1dba347a234e86ecf17016648`  
		Last Modified: Tue, 17 Mar 2026 01:20:28 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64a756f57d1b7b01a5ad74a57da3bdee2df71960de2be239d2569163529b765`  
		Last Modified: Tue, 17 Mar 2026 01:20:30 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.10` - unknown; unknown

```console
$ docker pull couchbase@sha256:04c27dc70d6df43213b3b030ac1cafca4f313699df3abcc2cd6abddf7e2e4fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3e799c4e8a71cf0bf23d41be2358a5be40dc49e0814d6e324746a599083789`

```dockerfile
```

-	Layers:
	-	`sha256:87a451b71258b87d1c9acf8442059a2cb768e623c61e2f675dffff16e6b09f3f`  
		Last Modified: Tue, 17 Mar 2026 01:20:27 GMT  
		Size: 37.7 KB (37730 bytes)  
		MIME: application/vnd.in-toto+json
