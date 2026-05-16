## `couchbase:community-7.2.0`

```console
$ docker pull couchbase@sha256:58562c27759990c2ce83317ab7c1d7cd99d0d46aa7f22d5b7b7729eca24858bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:d357b9f6ea08c2ab05e20769e102503bab15b56524ce9a8c66eb0036fed79daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 MB (392052582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa6575bca67db52d64c36d725c8eaece220bdfb1838c5a889f430fccbca738e`
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
# Fri, 15 May 2026 21:12:01 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:12:01 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:12:01 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:12:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:21 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:21 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Fri, 15 May 2026 21:12:21 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:21 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:14:45 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:15:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:15:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:15:20 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:15:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:15:20 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:15:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:15:20 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:15:20 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:15:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:15:20 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:15:20 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:15:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed0d454f3b629f480e75d6116710c6d226190d5398249d0207a4d4bacc91182`  
		Last Modified: Fri, 15 May 2026 21:14:25 GMT  
		Size: 39.3 MB (39307268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f438772427bd1e37be410536d6dd383a0e55356d5c1b9a6d4f8aa425a906fa`  
		Last Modified: Fri, 15 May 2026 21:14:23 GMT  
		Size: 926.8 KB (926781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ae902c88f29c384fb9d87e3ab5283e91205db1708374f4a38f6d66c72de589`  
		Last Modified: Fri, 15 May 2026 21:15:52 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddafe7629a5c98788bf6bb0817058307f33a83a536c125af5ec6cbf91691396f`  
		Last Modified: Fri, 15 May 2026 21:16:00 GMT  
		Size: 322.1 MB (322076668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d07ac5dc04fe237983d5635a65afca0e3764334b0fbbb0c4e4a78b1d022f839`  
		Last Modified: Fri, 15 May 2026 21:15:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3988b1bd1862c9786a80b7ecd7be2a78dd6dc545748d674b01f826879a0fcfc`  
		Last Modified: Fri, 15 May 2026 21:15:52 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1327236b9f52f60fcc343890e5666ca8aae76b9b2bf16e6d7c8416c9f04df934`  
		Last Modified: Fri, 15 May 2026 21:15:54 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a967f1cfa4be12afc51a247e4aedd864c2145dcb272620d27aa5ebf0898978`  
		Last Modified: Fri, 15 May 2026 21:15:54 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dac70e76b70e4f804f746b2eaeecf4911fc9953b9d82f9a0366a255357a40e2`  
		Last Modified: Fri, 15 May 2026 21:15:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8677cdab82d094b4f924906b75e5fdf13ee54e0e32e967def083526177a644d4`  
		Last Modified: Fri, 15 May 2026 21:15:55 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:bdb8e2d2fe681eb725292ad0bf46e70faa354d60bd8e8dbe9a01e575eef6f9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd2923b57c77e308234ab04014e416b5fa1c158d762951e4aa4a531b4681213`

```dockerfile
```

-	Layers:
	-	`sha256:faf9ba8d0c03e32fe753d7066484aedeea9e695ddea6c6929798227c4302064d`  
		Last Modified: Fri, 15 May 2026 21:15:52 GMT  
		Size: 37.2 KB (37209 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:05fdef8958b0bc1b7cd0c51637b070bbad53b2992161f96cd2e2fd6d1ea040e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.4 MB (369378948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571e12dd59312d21c1ac82d89f0970ba8f8d0e212d4a2b7a850912f975d0b5ca`
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
# Fri, 15 May 2026 21:12:08 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:12:08 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:12:08 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:12:08 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:37 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Fri, 15 May 2026 21:12:37 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:14:57 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:15:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:15:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:15:31 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:15:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:15:31 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:15:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:15:32 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:15:32 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:15:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:15:32 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:15:32 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:15:32 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e4177e553212251aa48bbe25e3c8f413bbd8a8c1a9813c3c8b6909c9545508`  
		Last Modified: Fri, 15 May 2026 21:14:36 GMT  
		Size: 38.9 MB (38866762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c455c5cadf8f06d9b2cb63d93e16c59b2a1a436049e75e107128eb57d9af3a12`  
		Last Modified: Fri, 15 May 2026 21:14:34 GMT  
		Size: 775.3 KB (775263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8222a36e18521ad74e336b87ffdd3f1935c5a0a859dd2bbb99327488e697c75c`  
		Last Modified: Fri, 15 May 2026 21:16:02 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ee934a322bb460e34591f4d6cbf680b23760924f4ac5e2db28ee7e153c09eb`  
		Last Modified: Fri, 15 May 2026 21:16:10 GMT  
		Size: 302.1 MB (302125118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834664609887c5251fc04e697c9d71a517af1d3e1430b5e0e4c665a82195500d`  
		Last Modified: Fri, 15 May 2026 21:16:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f021fd2531112e90a069e08d1be878b413772db2fc7da9699aeb96a2cfcfd`  
		Last Modified: Fri, 15 May 2026 21:16:02 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9856079b62c1f8c1a244e337279f1ca5401b1e68c00904cb7527ea940ec8774`  
		Last Modified: Fri, 15 May 2026 21:16:03 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb44c61da3a03c60511e15239ea46c7bd2f6ebd6bf47df9f1b64eb7d0a377af`  
		Last Modified: Fri, 15 May 2026 21:16:03 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fb4485142c3f731a55462bfa0bb6286b36f40f9171c6a5778227e94a1defa0`  
		Last Modified: Fri, 15 May 2026 21:16:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2468c8d6d81ec066605f49f1775384fb0485a07684fbb5687bb143826ce3fce`  
		Last Modified: Fri, 15 May 2026 21:16:04 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:113422b431d2bc32a5629c15f5f3627cd9a612895af5bfadece31633dc0cc4f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdc12bb1e30911b78af4cafe5ddec905568582587efcabbb5ebcfd8b0a13d26`

```dockerfile
```

-	Layers:
	-	`sha256:e205a462aaf993a38835d7e4f342cc20076bc4f994de80803d239f472a860944`  
		Last Modified: Fri, 15 May 2026 21:16:02 GMT  
		Size: 37.4 KB (37381 bytes)  
		MIME: application/vnd.in-toto+json
