## `couchbase:enterprise-7.2.3`

```console
$ docker pull couchbase@sha256:4d8ac06dbf8b01f9ef8a76e378de5e8def904fd82a2e318d763001f646e51ac3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.3` - linux; amd64

```console
$ docker pull couchbase@sha256:335f06a1088605f92eaaa8e0c438228967b79fa0461b04d2e108e5b6d535ec7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.7 MB (668734268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956f621a801957461b704d8395c8f74a4ebd66720e3815d275a3bd9a683a9de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 09 Nov 2023 23:59:34 GMT
ARG RELEASE
# Thu, 09 Nov 2023 23:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 Nov 2023 23:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 Nov 2023 23:59:34 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 09 Nov 2023 23:59:34 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 09 Nov 2023 23:59:34 GMT
CMD ["/bin/bash"]
# Thu, 09 Nov 2023 23:59:34 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 09 Nov 2023 23:59:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 09 Nov 2023 23:59:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Thu, 09 Nov 2023 23:59:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Thu, 09 Nov 2023 23:59:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 09 Nov 2023 23:59:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Nov 2023 23:59:34 GMT
CMD ["couchbase-server"]
# Thu, 09 Nov 2023 23:59:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 09 Nov 2023 23:59:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049dfaa837725beac57f1300eb8f3d26760563f4356d63ab86f01e1e72ab4717`  
		Last Modified: Tue, 25 Mar 2025 18:26:50 GMT  
		Size: 6.3 MB (6289506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9c3261b82d7fdabaafd77214663007361379d82d0e14d1b9c94891f8d2a318`  
		Last Modified: Tue, 25 Mar 2025 18:26:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633cea641812a240b9c902a8cf2cbdab7fed682bdefb3ece7a37d27098e2bd04`  
		Last Modified: Tue, 25 Mar 2025 18:26:59 GMT  
		Size: 634.9 MB (634929391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6464f58bbd9b24b7520524bfe4b17450dd6ce48fa9964845e651a20635a33067`  
		Last Modified: Tue, 25 Mar 2025 18:26:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247a5d35aad0b3d92fd10da138757b909f75a27498028965415b426b82aa472`  
		Last Modified: Tue, 25 Mar 2025 18:26:50 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41fafd3853159e499fcc339a959de9d45e94a960d6f868b6220c46f6589e7ce`  
		Last Modified: Tue, 25 Mar 2025 18:26:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e33769dfddef9d50821a4722eaa50a7bbb890247d00a56ae206af7602777765`  
		Last Modified: Tue, 25 Mar 2025 18:26:51 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bee93bfe8d9873587618f6de3d0e5d0f207eb809dc0850e4836331673561556`  
		Last Modified: Tue, 25 Mar 2025 18:26:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5e0f2050bdf85d4646b09ed1b2913715e27f8084742fd4eca798f903155c26`  
		Last Modified: Tue, 25 Mar 2025 18:26:38 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:edd2e9a586d65d1f6217b6de3942b64bd347cfdab310e4988fda0285baee4cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 KB (31813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d3872d29ef04d32c224d2f6108ad35d03400509a67ba3cafbac6f69e91347`

```dockerfile
```

-	Layers:
	-	`sha256:de03377e5a06134717b4241af09754395d93aeaacd835f90f8d2dbeadd5c1241`  
		Last Modified: Tue, 25 Mar 2025 18:26:50 GMT  
		Size: 31.8 KB (31813 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:2e3578fb1a0e128e8988c7b216a2fb7289ae981c56320947d3a002012270809a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 MB (639979812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22dd079a660afcec7668ddd24fb64a372e6a66d3821bfc0b0e68564132f4d50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 09 Nov 2023 23:59:34 GMT
ARG RELEASE
# Thu, 09 Nov 2023 23:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 Nov 2023 23:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 Nov 2023 23:59:34 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 09 Nov 2023 23:59:34 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 09 Nov 2023 23:59:34 GMT
CMD ["/bin/bash"]
# Thu, 09 Nov 2023 23:59:34 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 09 Nov 2023 23:59:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 09 Nov 2023 23:59:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Thu, 09 Nov 2023 23:59:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Thu, 09 Nov 2023 23:59:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 09 Nov 2023 23:59:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 09 Nov 2023 23:59:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Nov 2023 23:59:34 GMT
CMD ["couchbase-server"]
# Thu, 09 Nov 2023 23:59:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 09 Nov 2023 23:59:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dd044daf6d9cc36978d222f8fb06b0a5d31fdd6c8aba41f8febf9e74e58ed3`  
		Last Modified: Tue, 25 Mar 2025 18:51:58 GMT  
		Size: 6.1 MB (6119387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfa153c4eda2f67dcba1e4a8a62803d8ffc06bd7fafa177e258311e6414c97b`  
		Last Modified: Tue, 25 Mar 2025 18:51:58 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f927bd666e1353a18f7816a6caef72b62647ca0a44bb18a826f8d621ae479c`  
		Last Modified: Tue, 25 Mar 2025 18:52:13 GMT  
		Size: 607.9 MB (607882291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b00a5a3639a308f51553a50357611c1a0b2eb19552afb58efdc1f85d8a9a662`  
		Last Modified: Tue, 25 Mar 2025 18:51:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f409856c6f4a928d6eb9252bebe602bc6ba4fa6d8ea2d700509fa3a62b557b67`  
		Last Modified: Tue, 25 Mar 2025 18:51:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c58bba06780b441366c494bad64c8a12692d46eaff516c666d909a56341392`  
		Last Modified: Tue, 25 Mar 2025 18:51:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940ee93371be785f42d94416c86dddf0c978c681d027738d86e0051db7724bbe`  
		Last Modified: Tue, 25 Mar 2025 18:51:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaf6a55e5a4d9cdc0a525799e52aa23cbb2be21f029f2247d3a09e6bbce7841`  
		Last Modified: Tue, 25 Mar 2025 18:51:59 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15182621b9e1fb8f98eaf14ceb4a9a92c687369738b2aa1d4253f597332df8c`  
		Last Modified: Tue, 25 Mar 2025 18:52:00 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:49d4124312c962d6771e802aeac2695b7410860ce1dd22c8acae084b03e142ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 KB (31983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c00b3ae68d397e5669fca29cfc7032bdae28a5982ca7800295d9370d921bbc`

```dockerfile
```

-	Layers:
	-	`sha256:944e28930eba54429ed521dd2094b8ab7501ce01c44cdc258c74f851eb243194`  
		Last Modified: Tue, 25 Mar 2025 18:51:57 GMT  
		Size: 32.0 KB (31983 bytes)  
		MIME: application/vnd.in-toto+json
