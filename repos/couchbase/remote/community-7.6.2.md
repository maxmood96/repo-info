## `couchbase:community-7.6.2`

```console
$ docker pull couchbase@sha256:64760866fe4e1bf42e1e2f9f2128f0028e6d53bfef97e00a6837ab1d00cd7234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:16801dc0aaf65a2545f26469b094a004ff241418d22a0d1e0e50256c3de90eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436739806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df34e7c189dc442c188d5da9b8988af5c822e40f47b1c808de69c3274c9a1f2d`
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
# Tue, 07 Apr 2026 01:48:52 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:48:52 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:48:52 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:48:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:49:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:49:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Tue, 07 Apr 2026 01:49:24 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:49:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:49:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:49:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:49:41 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:49:42 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:49:42 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:49:42 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:49:42 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:49:42 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:49:42 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:49:42 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:49:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:49:42 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:49:42 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:49:42 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b962f3424a524248cc25cbe7850f2648ad6fccdaeaf045b3550c69e5128e6af`  
		Last Modified: Tue, 07 Apr 2026 01:50:20 GMT  
		Size: 43.8 MB (43816304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739fc6f7ad7e3c54652511404f1f92d7a6de4bb55e91914fa81c9eee0def248`  
		Last Modified: Tue, 07 Apr 2026 01:50:18 GMT  
		Size: 878.1 KB (878123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2a5369fd349310ff5d0b19c6879e44c11b6a99a6dd890724860c794cdeeb25`  
		Last Modified: Tue, 07 Apr 2026 01:50:18 GMT  
		Size: 3.7 KB (3726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623ccd5b5dba6a0b9d1ffa57497fde287d541807844a41c475b6967cb8e5b22`  
		Last Modified: Tue, 07 Apr 2026 01:50:25 GMT  
		Size: 362.3 MB (362305003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0ccedd9d415236e8b4def4d64350276e314f39fe3fe10213cc7c34f516f073`  
		Last Modified: Tue, 07 Apr 2026 01:50:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464c9d9195428c87e78f3dc1823d92455ae921f83e4a0212c5a1e4c71448e062`  
		Last Modified: Tue, 07 Apr 2026 01:50:19 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e76e6bd6a8648eb307cffbcd9d9d2ad4763f3147d3d505371a5f1db62f0da3`  
		Last Modified: Tue, 07 Apr 2026 01:50:20 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1231b16379ae0498746bea3f4dcc16882854c2df23eeb2cc42ecbd2029a5093c`  
		Last Modified: Tue, 07 Apr 2026 01:50:20 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b467a614f2f74f119f7757b8036a4ca9a172d4bf7b82e967bc21e4115f2633`  
		Last Modified: Tue, 07 Apr 2026 01:50:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10da14f54c1513e31b8b667ab25314e0674aabafec697656f7ac17836fd1d2ad`  
		Last Modified: Tue, 07 Apr 2026 01:50:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:a0b666357f33f311476f07e3df8d62bb82ec56d9b7ad430defa1de8371d632d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fd024641cfcb018d2770ca46be5c4854565b52fd2dd3ab36d0b238d4ce3fd7`

```dockerfile
```

-	Layers:
	-	`sha256:f54c91219727f180933f6e82a8b189e4cf06ff3d67191418d30bd0f5414d4ba5`  
		Last Modified: Tue, 07 Apr 2026 01:50:18 GMT  
		Size: 37.2 KB (37209 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:cf10664c510c6bb7109a3014448ff9c5b60f5bd70969f383c483f8e624709c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414846056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a594b89690820e68cc431b46faf66813a38f9fff4a6153af104e50bc40c6c5b`
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
# Tue, 07 Apr 2026 01:51:25 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:51:25 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:51:25 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:51:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:51:59 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:51:59 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Tue, 07 Apr 2026 01:51:59 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:51:59 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:51:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:51:59 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:52:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:52:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:52:28 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:52:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:52:28 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:52:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:52:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:52:28 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:52:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:52:28 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:52:28 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:52:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3dd104b08318e696261997ddff64a10d78e16a9a8af0b9da682b38abe2123a`  
		Last Modified: Tue, 07 Apr 2026 01:53:06 GMT  
		Size: 43.6 MB (43633586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94faffc22bb1dabb9b6213dbecef9163140769898cae31ce56100913305d40fb`  
		Last Modified: Tue, 07 Apr 2026 01:53:04 GMT  
		Size: 765.0 KB (765047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6516663410b2800ebc013e254ad4bdd9a46e815b4ebbf834d210cc41fac05d95`  
		Last Modified: Tue, 07 Apr 2026 01:53:04 GMT  
		Size: 3.7 KB (3723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905bbe7eac0fe468696b25151bab888cdaa67eb307e728a9f522b53b50a765f7`  
		Last Modified: Tue, 07 Apr 2026 01:53:14 GMT  
		Size: 341.6 MB (341566443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b47d5a84452ed5355bdb0b4105fcaece7af46cdf9fc822f7b40756335620f5c`  
		Last Modified: Tue, 07 Apr 2026 01:53:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058ca25ae4e40992907ca199cd7caf9ec938ce6b9dedbd851e983eb62ccfe8ca`  
		Last Modified: Tue, 07 Apr 2026 01:53:05 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b758140e174e95f02fbfd70a6082ef1fbf2fc0fd00cc19996e69643df61947`  
		Last Modified: Tue, 07 Apr 2026 01:53:06 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac520a404524f6ed7b1d5a02a003b907e97a076c9d582369ec1a4b67ced05b19`  
		Last Modified: Tue, 07 Apr 2026 01:53:07 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d60a8ec3f0272fcb12a05e14e000c9324e229989880b7b658799c88882152e`  
		Last Modified: Tue, 07 Apr 2026 01:53:07 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41134ccd72bf8f59348118abef15e7dc459dffef68d824019f8ca087e16f85a9`  
		Last Modified: Tue, 07 Apr 2026 01:53:08 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:3ff9f608364b947282207339a6926aac66e97299fb35bf23fe6810712fe8aed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a45933b1f820b489cb91dd89d7ff1e7420bed1d92fb384b1defd1ec66cd3ada`

```dockerfile
```

-	Layers:
	-	`sha256:0db33534302152c87c60a5930ea9cb8162767a67a1414922f1051681e3e3d460`  
		Last Modified: Tue, 07 Apr 2026 01:53:04 GMT  
		Size: 37.4 KB (37382 bytes)  
		MIME: application/vnd.in-toto+json
