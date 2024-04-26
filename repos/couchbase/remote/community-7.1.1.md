## `couchbase:community-7.1.1`

```console
$ docker pull couchbase@sha256:49182ee1ae0cbe6105f7aa3950984afa8265341525798e96634b4b4dc4131e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.1.1` - linux; amd64

```console
$ docker pull couchbase@sha256:81ae93286f9a68b39e639d16d92a89d85e7d2ec2a58dd18ea26bf80ef9b56cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.7 MB (346675717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6132460ea6e5c6fa20f637174cbcf56cb7e29b24c770a1eeedcd8edfbf1280e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Fri, 26 Apr 2024 00:17:11 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 26 Apr 2024 00:17:11 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 26 Apr 2024 00:17:11 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 26 Apr 2024 00:23:49 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Fri, 26 Apr 2024 00:26:29 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Fri, 26 Apr 2024 00:26:29 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Fri, 26 Apr 2024 00:26:29 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 26 Apr 2024 00:26:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 26 Apr 2024 00:26:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 26 Apr 2024 00:27:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 26 Apr 2024 00:27:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 26 Apr 2024 00:27:17 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 26 Apr 2024 00:27:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 26 Apr 2024 00:27:18 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 26 Apr 2024 00:27:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 26 Apr 2024 00:27:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 26 Apr 2024 00:27:19 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 26 Apr 2024 00:27:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 00:27:19 GMT
CMD ["couchbase-server"]
# Fri, 26 Apr 2024 00:27:19 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 26 Apr 2024 00:27:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905b9f5ca2a463183da118b09302ea43e0707e2f34db20749deaa5b4ceef76eb`  
		Last Modified: Fri, 26 Apr 2024 00:33:49 GMT  
		Size: 6.3 MB (6286737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a784ddf06d3f8073561d1e5e28ad45d6fa07931e2854fab694b5bf5406f46924`  
		Last Modified: Fri, 26 Apr 2024 00:35:47 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f9ef60eac3ee803ef630ef3df68de87735de66d76a5bb680186d1ecdabe95d`  
		Last Modified: Fri, 26 Apr 2024 00:36:22 GMT  
		Size: 311.8 MB (311800013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648e1713930cb34061dadcd43624306e04684303c8f6b2148e9db61e50768951`  
		Last Modified: Fri, 26 Apr 2024 00:35:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ad414ad9dd5080d4163e2272eb87144cdf90f7ba6a22e2cfd219f5af41941`  
		Last Modified: Fri, 26 Apr 2024 00:35:45 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee3573781e7e244e07bc2a8eb2808c2379f08c74d9b453529ad2ef48d9da649`  
		Last Modified: Fri, 26 Apr 2024 00:35:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17524d2b5f9e276ebaba5dda833fd803689a7ebcd20f581555fa83e2391f6edb`  
		Last Modified: Fri, 26 Apr 2024 00:35:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbef0ad468736cbf8e94326dc427a6938d07d4263bc9d516f91a13310a3be4e`  
		Last Modified: Fri, 26 Apr 2024 00:35:46 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4f289708da836c5bbe77d72d9e1d82d0df5eaf59f66ffb483673b359cb91f4`  
		Last Modified: Fri, 26 Apr 2024 00:35:45 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.1.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:4459d72ebb55b26681a8734dc67e13878e8ad87fc10dcc02fe156d4abc213651
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327350360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5161b6d1590874806fff96c9d9f4bc3bf11f81ddeb6a2f248e7e3f07d2991b`
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
# Thu, 25 Apr 2024 22:19:48 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Thu, 25 Apr 2024 22:19:48 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:19:48 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:19:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:19:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:20:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:20:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:20:29 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:20:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 25 Apr 2024 22:20:30 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:20:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:20:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:20:31 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 25 Apr 2024 22:20:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:20:31 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:20:31 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 25 Apr 2024 22:20:31 GMT
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
	-	`sha256:ec0de0cc0c2b704eeeca14d03692602909b397cb69e5029ebe445998c8c68c6e`  
		Last Modified: Thu, 25 Apr 2024 22:24:51 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d912f3773aa0c4a5d6d21593e27407c0c047f94d3ad34cafb05a786e6c2a5c5`  
		Last Modified: Thu, 25 Apr 2024 22:25:16 GMT  
		Size: 294.0 MB (294027237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab92b8ba87eca29301269f72132a51a7449b7273bb5254767681413db9d7cf`  
		Last Modified: Thu, 25 Apr 2024 22:24:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080d59de1d4383700ac7a9639c8b001e13076400082a73e70535e7da223cdc85`  
		Last Modified: Thu, 25 Apr 2024 22:24:49 GMT  
		Size: 740.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807864382c6ed15f1b063929e7dd898190bda4b8098394257f9317ec2787e4a3`  
		Last Modified: Thu, 25 Apr 2024 22:24:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac52b84909c20a845c227cb379122907cd93b233bc56917e10adbb701dc91e8`  
		Last Modified: Thu, 25 Apr 2024 22:24:49 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700dfafa8122fc14bde9c3dc2827bc9ed7b82f45fde5265ff053ddccd4978ab`  
		Last Modified: Thu, 25 Apr 2024 22:24:49 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee965786d39c13834357c7c597216fd3d4033231e7036d4db35a5d4159b4c1`  
		Last Modified: Thu, 25 Apr 2024 22:24:49 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
