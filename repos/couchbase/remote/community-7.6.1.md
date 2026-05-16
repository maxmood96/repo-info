## `couchbase:community-7.6.1`

```console
$ docker pull couchbase@sha256:5ccad2d331c1cc1dbd62f01ae5070535007714cd1f6455ddba9cae9854723835
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:e09753d21e2e685bf362033ca98a2ae5cefe79dc66f56d857683e58b9d15dcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.8 MB (419821706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017728430fcaf03d5a0fbeee1fb7a5e49ba78f2b5e4cbef9c5ef8af25eb1051d`
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
# Fri, 15 May 2026 21:12:04 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:12:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:12:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:12:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Fri, 15 May 2026 21:12:24 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:12:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:14:44 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:14:44 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:14:44 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:14:44 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:14:44 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:14:44 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:14:44 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:14:44 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:14:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:14:44 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:14:44 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:14:44 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2a030eb4d0db8411328d389ba99736766ec6bbf216ed917a4acb8d7281d74e`  
		Last Modified: Fri, 15 May 2026 21:15:18 GMT  
		Size: 39.3 MB (39306785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea422956e9ea3dfa9d3b9890c7d5719909a8ba0a44d0c3b938309d1b5988fa`  
		Last Modified: Fri, 15 May 2026 21:15:16 GMT  
		Size: 926.7 KB (926722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db63270b21cce2eddce801b1d0d18d38e9fd743ab250ed4ea6d5ad0f003ddca`  
		Last Modified: Fri, 15 May 2026 21:15:16 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5803fd7f2b805dddd4003af691ff4030afc1906d71b26a98e3da532dd4aa22`  
		Last Modified: Fri, 15 May 2026 21:15:24 GMT  
		Size: 349.8 MB (349846339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d918b5132199ba1b540c5834e11973aac772aacde275160c56312484e5a52a3f`  
		Last Modified: Fri, 15 May 2026 21:15:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b486abcc3d7712c549020e40640b6bdcfe63d6e85680524d6a731fb64d25e583`  
		Last Modified: Fri, 15 May 2026 21:15:17 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0631ae802b74a5614a074f16bf78f0172ddbda749a45b049ef2cc32c8ccb475e`  
		Last Modified: Fri, 15 May 2026 21:15:18 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced439c9d4a0be751e48ded2a22c1dfe31e508f7172a16f27a82ac3f5f62b39`  
		Last Modified: Fri, 15 May 2026 21:15:19 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0250e4f83f8f6291a54e084cbd8b6f05fa363ee8b62c77e3c82c5f9c08a28e3b`  
		Last Modified: Fri, 15 May 2026 21:15:20 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbd79f10d47c48adaf4ba40ccc2de9b58cd6d4ec790a7775841b8d2d02c9385`  
		Last Modified: Fri, 15 May 2026 21:14:19 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:edf17d06c2d6b3f2411983677f663dc842455d97e3a115ebbc3b8c9e7d28966a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1943f5f8cff24c5b720e2497371edeaf096a26d88a6cfcfec771bf6ae9234f`

```dockerfile
```

-	Layers:
	-	`sha256:20773f9d63b847fda74398e0d04fcf38bcc9fd7b2e4cf7c8ae20e5479e474a85`  
		Last Modified: Fri, 15 May 2026 21:15:16 GMT  
		Size: 37.2 KB (37209 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:6940efb1aba3bc310c566fb749a90185dd5aaed51f654636058ae23dacd73d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400651930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06db18fa64738d8597f5c171961e0588d51e9c6c544aa108a01216514005265`
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
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Fri, 15 May 2026 21:13:18 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:13:18 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:13:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:13:18 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:13:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:13:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:13:55 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:13:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:13:55 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:13:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:13:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:13:55 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:13:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:13:55 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:13:55 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:13:55 GMT
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
	-	`sha256:589fb57b792f8f8ab514e257dcf60538e892345de788073142de0c6b1e219723`  
		Last Modified: Fri, 15 May 2026 21:14:31 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b34688f43218edaeb731652d8f6bb3dc1c9f1986f560ae2609c73a30da1ef3`  
		Last Modified: Fri, 15 May 2026 21:14:39 GMT  
		Size: 333.4 MB (333397966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afad5314b3a49070b439b7d511e162dec39369997d719bd53a8dd609ce7a7a2c`  
		Last Modified: Fri, 15 May 2026 21:14:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962ef3f13ffe3fe3b9b3e156105c7570c1ecc0b39152a9d091e2b0a96b73b935`  
		Last Modified: Fri, 15 May 2026 21:14:33 GMT  
		Size: 814.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1444ed39b6f5c61a29e3e351462c24907be9dbf8ad6645c50c297f9bf8afca2e`  
		Last Modified: Fri, 15 May 2026 21:14:34 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29c93b48267ccc25c8af11f85a3ba3e3547e00d63d3f27efac55d0a3ace6435`  
		Last Modified: Fri, 15 May 2026 21:14:34 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0438853875d0ccc571b1f124030eaabe063616c6d571d238fc74a38b456cc9`  
		Last Modified: Fri, 15 May 2026 21:14:35 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42128440836688ef2fe1a41dd573f62f408cfd2b23e422d2dcb073f7be4011`  
		Last Modified: Fri, 15 May 2026 21:14:35 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:f5e39c783622de3e4f0b0f8ddc192abebe9d0aa27ca66963180519595d5dfd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcd5b5d2c4f50338cc7b0b8883cc9b1b345bd75ee7afb3c9fa7cdf045a2573d`

```dockerfile
```

-	Layers:
	-	`sha256:7c887d845a65b5d850799a3fc4f875f3413ebf0f3406c6e56c71fcd38829e7dd`  
		Last Modified: Fri, 15 May 2026 21:14:31 GMT  
		Size: 37.4 KB (37381 bytes)  
		MIME: application/vnd.in-toto+json
