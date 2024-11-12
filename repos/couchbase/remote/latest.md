## `couchbase:latest`

```console
$ docker pull couchbase@sha256:dff8011f5ed177b35ca5f916a51d97c1c7c0c53aa2013988d83f1e52171ac934
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:15d79ad96890fbfb17a36dd0e36575763251246c94becd76fe056ba96c7325e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.9 MB (768925234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3a46a56717114c7d9a9e75ba5538403252161f66fe571bae33d58c09c49fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181cf9a43df8c5e399e6d27dc51b550cb7eef1030eb4a23e9f2f1afc4fad47f7`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 39.3 MB (39276283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a57105c51c8a53b98e917c2a49922367ac246740ec2c4e5cb12c63f7618cbf`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 926.1 KB (926064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289ce120bf8531c16bb73d516193c2f95d5195d73ffb2bc4161ac2a689e7b85`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d3be05b1124e4858d82f0dbf1835540b90859cd9a894e529eae5a96ced26b6`  
		Last Modified: Tue, 12 Nov 2024 00:57:33 GMT  
		Size: 699.2 MB (699182015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20c0f01b24c1dd797d45570d12038d45ea57c1ffa8455ed3b675d7cbe161415`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cb7effd6ff13e9221825c975693a2f7eaeb5eb2f265f68bfd029cd2bdf5597`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d50fafe6355c5d292618c4baa5ae1347782aa58b113f23cf81498296d6a063`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcccada2863443a2551bf883c46696463ef77ea948fd074b08889a9aca0fd53`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786b1974142cdacd50c61e47beb3bb57acbaa3a705b0ed5d6ff920a6dcc3c546`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6a45fae918ae9c11f313b88bf4891ad8aa6f31fbe5a86006ef9240c17ca2b4`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:75d8f31d7368d637a7e098f38e21b5b272747d82b4935da1fac0749e4079419d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b568b81538ac5613e925c3341db97a3e720df08305bb0dee448cfeddedd53278`

```dockerfile
```

-	Layers:
	-	`sha256:680d4d9b916a40a0d91194e0fb7dbefd7e698c3ed2567bd465065af663466647`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:latest` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:e946c69bd434360dff17a1ae8c0aab63a7f317a29cf2f27127791e9a4eecfb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **740.3 MB (740282679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3851b9155496fe9af8cbc67ff23e4caffbd71871440a790f482c22ba9dc111a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9837b35b89321c86b62c4addb2275efc6de452946a2230ae527a93ebaf64cbe6`  
		Last Modified: Tue, 12 Nov 2024 01:14:06 GMT  
		Size: 38.9 MB (38853543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fd330817e32cf64f5305421981635c23024aced95a96800b8b6ce2fb23e74`  
		Last Modified: Tue, 12 Nov 2024 01:14:05 GMT  
		Size: 770.5 KB (770459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d108e111e1445face871399f66a53e0b609b5ff77408a902bba19fac2c77d02`  
		Last Modified: Tue, 12 Nov 2024 01:14:04 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de71da94bf9d6e25f0e91a9daf9bcf94b199bac819f65b6a29e61f77169cb6`  
		Last Modified: Tue, 12 Nov 2024 01:14:18 GMT  
		Size: 673.3 MB (673295157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d99b296f051c9dc747c85dd25c8159a417848e04e40d834b284f8df97c87ee`  
		Last Modified: Tue, 12 Nov 2024 01:14:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59d212c610c18199191dbe112705bc49d5e2e984b6fb9d07b247fc49c3ce0e3`  
		Last Modified: Tue, 12 Nov 2024 01:14:06 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfb7bdaffda0c2da7179426e577d7b60142ebb643e96480fd11a5f01f4d7d36`  
		Last Modified: Tue, 12 Nov 2024 01:14:06 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec9e5848ef97d3adba7c6d08916d14fa24da401e5b27cedac89051fc43c3b3`  
		Last Modified: Tue, 12 Nov 2024 01:14:07 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdb3085b85319798414ae6966fdd5ae53da24afd01358f25793b83d7b452e08`  
		Last Modified: Tue, 12 Nov 2024 01:14:07 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb61fd3b1b4b3694f62f5143556d788d1c795cdbac69b5109a7bdb516dd57f20`  
		Last Modified: Tue, 12 Nov 2024 01:14:08 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:1f527e11d9d65304110978d5ef93ff51e65d7817c1cf1acb3db44025bbb39e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45b35e309505303c360e78d5104f12aa63359e7bc911244e4ffa3d7de76652a`

```dockerfile
```

-	Layers:
	-	`sha256:c326186959e6a2fff0a42329d862b28666f28c789c125277ea53350eb9dc99f2`  
		Last Modified: Tue, 12 Nov 2024 01:14:04 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json
