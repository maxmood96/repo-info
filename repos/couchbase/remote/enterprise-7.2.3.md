## `couchbase:enterprise-7.2.3`

```console
$ docker pull couchbase@sha256:f720c09a8e90af2fa2b8cfd7279c541f6c0248806f9254f4cb5d2d6ea6c71897
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.3` - linux; amd64

```console
$ docker pull couchbase@sha256:b165203ed62b7551b825a44996c7ea767dd1ea667ce960415ce92de18b0e9607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.7 MB (668739314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47efa68d6806a27868de405c0dfc35cc8aa373fa43cc60b69748d084997b6a2e`
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
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
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
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb492f6449a689c96846489d9d6aea35f69e0f7cbb51aa58b208021ee5c2196`  
		Last Modified: Fri, 09 May 2025 10:06:11 GMT  
		Size: 6.3 MB (6295171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5243c16aeb431183bd04d57429f3fdd2ca6d4055374e14e71c4ab73e3a80b6b2`  
		Last Modified: Fri, 09 May 2025 10:06:09 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd05972464db0a464aba60454c011aa837e788cbc4f7fff54d08de975495b7d`  
		Last Modified: Fri, 09 May 2025 10:06:30 GMT  
		Size: 634.9 MB (634929449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667bb99e42e09e955ca63939465fd55757f90e9d87b9c64bd6a1ae84eb76189c`  
		Last Modified: Fri, 09 May 2025 10:06:12 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1cad7eacff6ecbe6e50e7ed45f467644bfbe86cae65542ffbe4d67319713e0`  
		Last Modified: Fri, 09 May 2025 10:06:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fbfb6bd6c0bee7d36dc63a2fcf44790719f211f65a3d6f23661fb70304801b`  
		Last Modified: Fri, 09 May 2025 10:06:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284c3ce920f8e48e90d27d8b2b87b1b1e705903b60d130671d038ae7b84d7e69`  
		Last Modified: Fri, 09 May 2025 10:06:16 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b1564d2b3596dff73f3a248eee32e4da13bdffaed82204aa17aeafd7a915c1`  
		Last Modified: Fri, 09 May 2025 10:06:16 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9368e0e3975059fa7b2fe439208579f9893f7c4f26867cafad1f53029798159`  
		Last Modified: Fri, 09 May 2025 10:06:18 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:767bab43d62320904db8356f0142bf84447c22e481cc3d228aa4b91cf5133eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 KB (31813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1102eb8ceaa31342618f7bb4836042a3986f5e01b7fc906da1851f154da6a0c6`

```dockerfile
```

-	Layers:
	-	`sha256:751936bdc3fb17e82c3b1e25569a6a9fd98d25d8f12956b5fa2058441e044766`  
		Last Modified: Wed, 09 Apr 2025 01:14:43 GMT  
		Size: 31.8 KB (31813 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:abb9fc49c01a719eb64bbce1b8f91e85931cb3cb390e7fed787b00d01a4c0954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 MB (639988815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbdc8487492b14e9abbf20e8b8932bcc6b50a175d3d8a2f5fd500a0e9a2bdc5`
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
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbd3b6d8b3dd5d4ede9235b28df451d880e2947c78240a111c0abd42143dbaa`  
		Last Modified: Thu, 08 May 2025 17:33:02 GMT  
		Size: 6.1 MB (6124748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d6c125928ceaf1416f296770cc77aad8b3f52a2fd4165bcc9e6a54c3e1c50e`  
		Last Modified: Sat, 17 May 2025 10:52:39 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9691cd43c89df6f92f91cba1aa27d474e45a5e4385a17a68fe4a8ff291450a`  
		Last Modified: Sat, 17 May 2025 10:53:18 GMT  
		Size: 607.9 MB (607882089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6cbb7967ce430e4397b821e6958ea05ba20259dc56a86fb648a3e677f4361c`  
		Last Modified: Sat, 17 May 2025 10:53:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b22fa648e2f01af33622c7d214319dac997d3b56787e7994e3e469d24e928e`  
		Last Modified: Sat, 17 May 2025 10:53:04 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bdfa24750b5b766438b1890eb00fb2db59e851266d85c0f7797556687eef63`  
		Last Modified: Sat, 17 May 2025 10:53:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1e8c1e906ad74f687ec3517058fe4a05a326ab4ca1d5ca9a8fe97fb13f8c83`  
		Last Modified: Sat, 17 May 2025 10:53:06 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c27a436b186c8ba2fc4bf571e5a154657415e439a8428ceaf7c5ff9a90ad8c2`  
		Last Modified: Sat, 17 May 2025 10:53:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04a36b40986bf26d84a6a1638c8055840e26b98048ed0601cffa51841997785`  
		Last Modified: Sat, 17 May 2025 10:53:08 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:011773e6e580d7da0a36f8fbaa653d2c6d29c07feff0eba246429f3dee016e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 KB (31983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c57c0124c1cbca553f9c966b1d93e1022f2fba567ff7564a694b4fcd016b11`

```dockerfile
```

-	Layers:
	-	`sha256:84fdbebd0c0d529b92d0b83c33b4ea3cf38654995487184f178cbbafd6edb15a`  
		Last Modified: Wed, 09 Apr 2025 06:49:40 GMT  
		Size: 32.0 KB (31983 bytes)  
		MIME: application/vnd.in-toto+json
