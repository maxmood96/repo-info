## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:ac9b63fbfa48e4dc0711dcd108ccea9415d1679894a5b5530aae598e22774453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:17eae305c2df6eb111bef0fb8a0bcd7195609492c04a25d8e2c2ccdceee4bb5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366178850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321fcefc2565f64e35a20447b14d15f71235ac9d3c1ecf39131f7964ed846bd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:52:57 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:52:57 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 02 May 2024 00:52:58 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:52:58 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:52:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:52:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:53:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:53:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:53:49 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:53:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 May 2024 00:53:50 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:53:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:53:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:53:51 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 02 May 2024 00:53:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:53:51 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:53:51 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:53:51 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d8dd6aa076fe85827f46df8b7cf6f7bc1b849b0804a4bd22f27595cf982cfe`  
		Last Modified: Thu, 02 May 2024 01:03:05 GMT  
		Size: 6.3 MB (6286683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b8f7a018d846c72bff254f148f3d9385d3265b2b7667e2571370c3886f8d1c`  
		Last Modified: Thu, 02 May 2024 01:03:03 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5032c9742ff624376ca7a290579ab0e72dc7cfb2902653ba72368c838542e881`  
		Last Modified: Thu, 02 May 2024 01:03:42 GMT  
		Size: 331.3 MB (331303499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92d947a16d69ff06e7d7f3854a51b6772f89c186e856d7d183443cada3cf515`  
		Last Modified: Thu, 02 May 2024 01:03:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc0dc23492d0cdb83d79b615ca2faeb18666a16fb1ceb73114aad7bd1c87d9d`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881cf5ab867f00075d058ea49cfbd1c4621399c7d0941edab77c165e9802e3aa`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bdf67406549d428ee8055a70abb8b9640918329ed9b6a144ba7a102b5e9c1c`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37229c0ded9e5f371cdbda1d0f510e70ea9a308f60e64075cdc8b40b2309b7c1`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8887bffb1c0d0e424d77c77bf7fe2195f0fe9bc9221da146c38356c7d55f99`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:6fb3e3f26d0c44be19c4a06b8875ba7e5f751da9955efb7ff90118c934dfca43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346405276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe4fb9ced9c98750469a71c3347991d4a6cf16c15da2f17058c9bbcafcb8f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:11:57 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 25 Apr 2024 22:11:57 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 25 Apr 2024 22:11:57 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:17:35 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 25 Apr 2024 22:17:35 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 25 Apr 2024 22:17:35 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:17:35 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:17:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:17:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:18:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:18:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:18:17 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:18:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 25 Apr 2024 22:18:18 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:18:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:18:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:18:19 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 25 Apr 2024 22:18:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:18:19 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:18:19 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 22:18:19 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9520c4b30446c55e7e55d09aade902332430a20e44eadd7edd756de5a6d4e25c`  
		Last Modified: Thu, 25 Apr 2024 22:23:25 GMT  
		Size: 6.1 MB (6111742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d3cadef398b30067970c4a9a98a9d25cb43ce59648df37c6f4f2628d420c51`  
		Last Modified: Thu, 25 Apr 2024 22:23:24 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e72fd37f317985fbd2e50e39f4178e7c7073946b823d91a71d8e211e516c7`  
		Last Modified: Thu, 25 Apr 2024 22:23:51 GMT  
		Size: 313.1 MB (313082150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c859515bbe31c894885dbcbe8da04cd4db5e5ad50eb5fa8732030e0d6190e5a`  
		Last Modified: Thu, 25 Apr 2024 22:23:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9002c48188cc168da831617d05893204c46f5701644faf776aa74d04d802e2`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d2c686ffc07fa68487a93eb51eca25c8e817f3edfdca5bfc41bcc9e9750afd`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5004c86d977cffc1ef2c3d0d31ba81f3d3667820838817476bf5a427bedefd1a`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e53aa1fb690498ac8a56d7a7dabd020013cd971d20e45ac0164c7c7a8543278`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329ae614dc0c88662e80836a8e7525b3206b2f0ad196b425c4400e84c7f0fd5a`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
