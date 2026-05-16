## `couchbase:enterprise-7.6.5`

```console
$ docker pull couchbase@sha256:7cf82d6cfba5cba0632e301eb663a1c66c46500ff01fce8157d1819e74a29f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:218bc770e3ce4b11146a9b1f0226ca7f43079807cd29df89e93d5efa01bd5e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.7 MB (771710423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7413d243cd908ec24e6215ca46849bde9b7c65a8bafe49986e723282054099`
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
# Fri, 15 May 2026 21:11:44 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:11:44 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:11:44 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:11:44 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 15 May 2026 21:12:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:12:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 15 May 2026 21:13:13 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:13:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:13:14 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:13:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:13:14 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:13:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:13:14 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:13:14 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:13:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:13:14 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:13:14 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:13:14 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311826ae161dd1a63f0ee5a8720b4fe1cb420e567d17dc86b9a60f290d67e4be`  
		Last Modified: Fri, 15 May 2026 21:14:07 GMT  
		Size: 39.3 MB (39307398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012944883d1bab8927bc4289e694be475ca0a77defa9a80ed0454c9f5275a18d`  
		Last Modified: Fri, 15 May 2026 21:14:05 GMT  
		Size: 926.8 KB (926789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1146f7df3a0b1a981e6d7507efb5190515ebdd877c63261b0bce5c9871a51c`  
		Last Modified: Fri, 15 May 2026 21:14:05 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dcbe119a2da017604eca379eed81b93a4608e78cdc6db22c19c54431f765bc`  
		Last Modified: Fri, 15 May 2026 21:14:22 GMT  
		Size: 701.7 MB (701734372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc3e002df2f9d16ed1a3ce2a27ce195b8768852aa8c604edeec1c29161803a4`  
		Last Modified: Fri, 15 May 2026 21:14:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2a5e223ea47f6c7776b198b5896ae759c31f2b4f721489e12d2c5843a84da2`  
		Last Modified: Fri, 15 May 2026 21:14:06 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d752ef0dd498b6fa24f68a166d4f6b5bc32dbbf3d6b6aeb439a681c089e699cb`  
		Last Modified: Fri, 15 May 2026 21:14:07 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0b416adc3de05d32d9a9c74b37d96cc15cf0a3f0c9eeb52d50d30a7e248acf`  
		Last Modified: Fri, 15 May 2026 21:14:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38553e7aa646612e156afd1d50db0b752abcf279a937bde06bf3325e47a3a923`  
		Last Modified: Fri, 15 May 2026 21:14:08 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979885acfd0c910ff0a271ceee81985e9f799482d1cb6e02cadeae4064230033`  
		Last Modified: Fri, 15 May 2026 21:14:09 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:7e7e84d2028077418185d0d0ea69a9c343410b2e6e273ee8b98241c962e08563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748b4fb785e983a7df26eb32999844e093b4cd4421813aaf90c66a0323bc7d7e`

```dockerfile
```

-	Layers:
	-	`sha256:01c30f6adafc848637d957e5b1af0b16ff62fb85bfa31a694e043553fac53e24`  
		Last Modified: Fri, 15 May 2026 21:14:04 GMT  
		Size: 35.8 KB (35773 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:680ec94d70497fec0fa26123b0ad805cbb8819df4b2f08fbf07e5cd0caf960fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.7 MB (742720196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f55a99751e5b8087ac90863105383819b31b70e4c9c9ee91fbaf5ddb73ff40`
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
# Fri, 15 May 2026 21:12:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:12:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:12:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:12:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 15 May 2026 21:12:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:12:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 15 May 2026 21:13:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:13:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:13:43 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:13:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:13:43 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:13:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:13:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:13:44 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:13:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:13:44 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:13:44 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:13:44 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967417d37a5e40db3fc37343447cdf5772320a8cdb1170b811cf50908c59fa9`  
		Last Modified: Fri, 15 May 2026 21:14:37 GMT  
		Size: 38.9 MB (38866827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85980acf0c23efd24cf6e6ad625049c33b8d22928bbd735f380231650620f7eb`  
		Last Modified: Fri, 15 May 2026 21:14:35 GMT  
		Size: 775.3 KB (775344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66df3b58d6f2845282a258bfd9b2a28197646f53f4491cd328458ca192ec6c23`  
		Last Modified: Fri, 15 May 2026 21:14:35 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e30c3f41bc11ff166bd5cf65cf05150f016c5000433367901380b4a66556e6`  
		Last Modified: Fri, 15 May 2026 21:14:49 GMT  
		Size: 675.5 MB (675466222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd4de6d862eb27766f6c918a9774f50ea533bba45534036775000df95de6f5c`  
		Last Modified: Fri, 15 May 2026 21:14:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5d2cdfbfb7fd7b0f713be6437645197891f5807dcd3fc202852761328f0a46`  
		Last Modified: Fri, 15 May 2026 21:14:36 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0722838ddda0d70a4a6b5713701d0560306f8557222dc472eb42b61f378d13c8`  
		Last Modified: Fri, 15 May 2026 21:14:37 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55986ec31e12ba47f613e648afd04cc619a41e56d6e4e216c52c59e8bf610f8`  
		Last Modified: Fri, 15 May 2026 21:14:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ea0ee32c2ea2af215febf55bf82bb4adc7d699d798f79438e6d55268955ba8`  
		Last Modified: Fri, 15 May 2026 21:14:39 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0e3985b3ca8f88641491907b502265b58390e126dd1f5d69917244005be5d1`  
		Last Modified: Fri, 15 May 2026 21:14:27 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:dca6209584a4bcf0b7679c3dc5b24ecc3ed9d356cbf19a232d0e1061d76aa2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2f383277210b4eacde3809b38f0b79a28560ed2c1bcf5a113db5ca9c84ea00`

```dockerfile
```

-	Layers:
	-	`sha256:b87cbf677470e434505ee57619bc9d37284751abcf0cf08682a9483012d6d3cb`  
		Last Modified: Fri, 15 May 2026 21:14:35 GMT  
		Size: 36.0 KB (35958 bytes)  
		MIME: application/vnd.in-toto+json
