## `couchbase:community-8.0.1`

```console
$ docker pull couchbase@sha256:c04997d87e90a3f23f4a70165ca422981f55b21f5135f4aa03a1ddb0e3eb7666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-8.0.1` - linux; amd64

```console
$ docker pull couchbase@sha256:c2c896f5fbddbcb914759a2b8375ae67fb922f5079bc3ac299f7ce87971b04a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.6 MB (504579535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5d1b073c0ce7d05b0c54a62d66462819f872b930e9b82d66344b193ba94ae`
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
# Mon, 30 Mar 2026 20:20:30 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 30 Mar 2026 20:20:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 30 Mar 2026 20:20:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 30 Mar 2026 20:20:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 30 Mar 2026 20:21:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 30 Mar 2026 20:21:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1
# Mon, 30 Mar 2026 20:21:04 GMT
ARG CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb
# Mon, 30 Mar 2026 20:21:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 30 Mar 2026 20:21:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 30 Mar 2026 20:21:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Mon, 30 Mar 2026 20:21:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=ca9aa048cb12e3d89d982c3139a4d65a94f3820691435762d34d5d1117840333            ;;          'amd64')            CB_SHA256=e4dc69cb42e0e8d8de80519f18768e0b0acc683d5e1f10c609583a8f76609507            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 30 Mar 2026 20:21:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 30 Mar 2026 20:21:26 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 30 Mar 2026 20:21:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 30 Mar 2026 20:21:26 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 30 Mar 2026 20:21:27 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 30 Mar 2026 20:21:27 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 30 Mar 2026 20:21:27 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 20:21:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:21:27 GMT
CMD ["couchbase-server"]
# Mon, 30 Mar 2026 20:21:27 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 30 Mar 2026 20:21:27 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11051a9944b9e32fb9dec3afb12330c1e314fb1c1509bc106fe15e4aee0982e1`  
		Last Modified: Mon, 30 Mar 2026 20:22:12 GMT  
		Size: 45.9 MB (45948921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb4e3db89df4f40a7426ffd9e042af0d87611dee55da3c47f5308b2cccd2c1f`  
		Last Modified: Mon, 30 Mar 2026 20:22:09 GMT  
		Size: 878.9 KB (878883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dc9fa375118dc7a51265e3bf52687032b276bdddbb47b6f64d6a93ba71e353`  
		Last Modified: Mon, 30 Mar 2026 20:22:09 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67154f3c5131f889adc69080ac21bb56d5ca6f7657becd75290582ca411d9c85`  
		Last Modified: Mon, 30 Mar 2026 20:22:21 GMT  
		Size: 428.0 MB (428012748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44aaca0ea9af3a4e4ab45acd047beffc11d4436f204459494fb1a48babff1b6`  
		Last Modified: Mon, 30 Mar 2026 20:22:10 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de98fc6d2edc2c935e9e8f07371194370485905cc5ef067a9b50a6904a244717`  
		Last Modified: Mon, 30 Mar 2026 20:22:11 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48688218d4432553c80a55b09104279873a04312509f6a8139b8981f98001e3`  
		Last Modified: Mon, 30 Mar 2026 20:22:12 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b7ac6d889067c229ff982eff17a9354b47ee1c9af2a8a5bc2e73d5a61c7d12`  
		Last Modified: Mon, 30 Mar 2026 20:22:12 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc43218e69fbff9c545568ea8db636bcd5f8581de49831a94c320dd83e851549`  
		Last Modified: Mon, 30 Mar 2026 20:22:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13e48388a8c8043b66c54f7e762a5dcac454ae3a61a7127852dcb1681707c02`  
		Last Modified: Mon, 30 Mar 2026 20:22:14 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-8.0.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:53665912ed51070bf383d447857e43c975bf62acafad23af8e710694fdf59c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb7921e4d1cca54c3e918a447eb334225488c7873e1f0d1b5b66469b2db886b`

```dockerfile
```

-	Layers:
	-	`sha256:50b851931960a30739e367d5f5d90df89ea9f6bccde235e640d40c57920f652e`  
		Last Modified: Mon, 30 Mar 2026 20:22:09 GMT  
		Size: 37.5 KB (37519 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-8.0.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:084d8b648b2d5fc37b0056ad1b1a4ac7d041e3a97bc70a5df2724fa68431ba48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.3 MB (474266286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b389a2649edad9bd5286a1df26855e37b948876197e4abcc538debd9ecef6531`
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
# Mon, 30 Mar 2026 20:20:36 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 30 Mar 2026 20:20:36 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 30 Mar 2026 20:20:36 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 30 Mar 2026 20:20:36 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 30 Mar 2026 20:21:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 30 Mar 2026 20:21:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1
# Mon, 30 Mar 2026 20:21:10 GMT
ARG CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb
# Mon, 30 Mar 2026 20:21:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 30 Mar 2026 20:21:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 30 Mar 2026 20:21:10 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Mon, 30 Mar 2026 20:21:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=ca9aa048cb12e3d89d982c3139a4d65a94f3820691435762d34d5d1117840333            ;;          'amd64')            CB_SHA256=e4dc69cb42e0e8d8de80519f18768e0b0acc683d5e1f10c609583a8f76609507            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 30 Mar 2026 20:21:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 30 Mar 2026 20:21:41 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 30 Mar 2026 20:21:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 30 Mar 2026 20:21:41 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 30 Mar 2026 20:21:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 30 Mar 2026 20:21:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.1 CB_PACKAGE=couchbase-server-community_8.0.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 30 Mar 2026 20:21:41 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 30 Mar 2026 20:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:21:41 GMT
CMD ["couchbase-server"]
# Mon, 30 Mar 2026 20:21:41 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 30 Mar 2026 20:21:41 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe6d48224d15c92c543dcc67372ba29c55b4eef7988a90481e4143f566d3dcc`  
		Last Modified: Mon, 30 Mar 2026 20:22:26 GMT  
		Size: 45.8 MB (45838885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4204f4cfbdca6e63bde1d338e3b53ba5a31dfd55fc25f3bd58a7af5573b65f3c`  
		Last Modified: Mon, 30 Mar 2026 20:22:24 GMT  
		Size: 765.9 KB (765901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977bfa9cb5d84c12dfb7c452450aac93ffdad29dda164bf3772b8c5650a60557`  
		Last Modified: Mon, 30 Mar 2026 20:22:24 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ea359b0608da11242464d1b5dffda316973764fb4670b9245c7e73c0543169`  
		Last Modified: Mon, 30 Mar 2026 20:22:33 GMT  
		Size: 398.8 MB (398784802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487eb3abad6b0d16235f451e75f6bdf6146a32c89c776f517a5224b81db7e55a`  
		Last Modified: Mon, 30 Mar 2026 20:22:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba641aeae06b34b3d0d075b8d676dff28546a8781171b4461a3b245160d7f20`  
		Last Modified: Mon, 30 Mar 2026 20:22:26 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bec03f25af1bd93830202b03d50063c6b74dcd5411638fa141eaa2e9bd92e40`  
		Last Modified: Mon, 30 Mar 2026 20:22:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054255d5e22b4b5d76b089b179accfb2c2f511694b35c62f6f58874c8e56d0de`  
		Last Modified: Mon, 30 Mar 2026 20:22:27 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055c05a71e450f71567b8e8a68296b8dbe067c4b6d44ebfa62a7a72266b76dc2`  
		Last Modified: Mon, 30 Mar 2026 20:22:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2867c5b9f50b44ecf5f28238c8b4642a16aa864b39b8a330d855c2a238eab7`  
		Last Modified: Mon, 30 Mar 2026 20:22:28 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-8.0.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:fd313aeca8b85d890b5da95c356733b385834ae31aa5a4091b4040cdc01ad406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d14ae51a737fc13f119381d9a4dbe9019c0c404ebb494e128fbeded5f1b411`

```dockerfile
```

-	Layers:
	-	`sha256:76a021c5667c7332180a5d130f642a60560f1a2ed38ee5da6c50b6b6255fff08`  
		Last Modified: Mon, 30 Mar 2026 20:22:24 GMT  
		Size: 37.7 KB (37703 bytes)  
		MIME: application/vnd.in-toto+json
