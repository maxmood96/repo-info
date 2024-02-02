## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:70182190fdfabd29a6d11af3fc68ac36d1c7a5adaa884edc2f6ba3cd74fe1a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:bb312088ddcfcfd587e1e3988e2f247a8175c149e1146ff2132cd811115f1fa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346402442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd35a256e57d081d1b2ccd79da3710d081cb3624b43030eb8213274639f3e7ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:33:30 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 02 Feb 2024 01:33:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 02 Feb 2024 01:33:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 02 Feb 2024 01:33:55 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Fri, 02 Feb 2024 01:33:55 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Fri, 02 Feb 2024 01:35:23 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Fri, 02 Feb 2024 01:35:23 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 02 Feb 2024 01:35:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 02 Feb 2024 01:35:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 02 Feb 2024 01:35:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 02 Feb 2024 01:36:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 02 Feb 2024 01:36:06 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 02 Feb 2024 01:36:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 02 Feb 2024 01:36:06 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 02 Feb 2024 01:36:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 02 Feb 2024 01:36:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 02 Feb 2024 01:36:07 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 02 Feb 2024 01:36:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 01:36:07 GMT
CMD ["couchbase-server"]
# Fri, 02 Feb 2024 01:36:07 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Fri, 02 Feb 2024 01:36:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747381025e958c41554b8b195053d166fdd604e312c6843f58551c90afd0b5e0`  
		Last Modified: Fri, 02 Feb 2024 01:38:35 GMT  
		Size: 6.1 MB (6112069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839d85dc1c59cddee14633646bb02e00e1b53b2e523679e54d1257b2450808f2`  
		Last Modified: Fri, 02 Feb 2024 01:39:32 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431ff452c3b97f294913853d207292d30a2c1229111e123813100452c3ae820a`  
		Last Modified: Fri, 02 Feb 2024 01:39:59 GMT  
		Size: 313.1 MB (313080945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b586760a18eec5e2ab63a5801ddd332626e8502b437595fa47f71ce26cb879`  
		Last Modified: Fri, 02 Feb 2024 01:39:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1505760ee5970b41f635483223614d7cc3cff8b29785d5ecf68bf3716446ecf7`  
		Last Modified: Fri, 02 Feb 2024 01:39:30 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f47b7573babd29369129e51113fc92f45ce5992a247ff97abeb3894a7d4bc40`  
		Last Modified: Fri, 02 Feb 2024 01:39:30 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069ab4030b2d9eb418336577b0c4d0be415bb2a13162c8e2c95b67582dff521d`  
		Last Modified: Fri, 02 Feb 2024 01:39:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79b7e3d84315bd10169be3057810a7e7ac8ade52964a938387bfdd0d5a0bc1e`  
		Last Modified: Fri, 02 Feb 2024 01:39:30 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ca7d8ac7f414eb7bab95401479ae509ffeef82e256618b88791cea61492b48`  
		Last Modified: Fri, 02 Feb 2024 01:39:30 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
