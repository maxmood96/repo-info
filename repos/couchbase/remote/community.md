## `couchbase:community`

```console
$ docker pull couchbase@sha256:04963c42cc969e10ac65b2b10440a6f47a1843a096b95f65ad5b76dfd799f5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:5f484445a5900acf8e71b8f876f3c3b7279ddc1b532a6702747376daa756bfda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.6 MB (346613498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9823ebdafdc5997247e04ad88c8f59e850f0a49d5f12523d952058fb991c26e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 15:57:13 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 25 Oct 2022 15:57:13 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 25 Oct 2022 15:57:13 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 15:57:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 25 Oct 2022 15:59:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Tue, 25 Oct 2022 15:59:06 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Tue, 25 Oct 2022 15:59:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 25 Oct 2022 15:59:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 25 Oct 2022 15:59:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 25 Oct 2022 15:59:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 15:59:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 25 Oct 2022 15:59:53 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 25 Oct 2022 15:59:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 25 Oct 2022 15:59:54 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 25 Oct 2022 15:59:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 25 Oct 2022 15:59:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 25 Oct 2022 15:59:55 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 25 Oct 2022 15:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Oct 2022 15:59:56 GMT
CMD ["couchbase-server"]
# Tue, 25 Oct 2022 15:59:56 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 25 Oct 2022 15:59:56 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c363d586f4d6eee662a9e0f273458c615ad1280fafe8bdffd8aaf8bcce83e523`  
		Last Modified: Tue, 25 Oct 2022 16:05:58 GMT  
		Size: 6.2 MB (6232224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebbdf9f99e206b2327ed1000fdf20137f8fa2d3a2e1bbac52b6264df5ec10b`  
		Last Modified: Wed, 26 Oct 2022 16:50:08 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750116979b41a809a900b153358d87859bf6adf0900c8a5fade44d43ff933c88`  
		Last Modified: Wed, 26 Oct 2022 16:50:51 GMT  
		Size: 311.8 MB (311799071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f0dfc7f3733059787ef8c04bcedf5cdbbd2b9703f5caea401c72a34ebc4c86`  
		Last Modified: Wed, 26 Oct 2022 16:50:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27edd04c0861d10447d01a8bad9cb9a007dffe1fdec5227880c423eb6716e5`  
		Last Modified: Wed, 26 Oct 2022 16:50:06 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff84f0a4b9bc8feff37bb7d11114a312f11c38db9b2b38dd9a8e4c84fd6f0b`  
		Last Modified: Wed, 26 Oct 2022 16:50:07 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede1d8728c1920be414e737f5396b6fe5ebc393b20f600a75b7badf5b7646b0b`  
		Last Modified: Wed, 26 Oct 2022 16:50:06 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cda2592fbf33f0953ec7b89643c8173f0cb4100e2b1a74675bf0a4ea2c58132`  
		Last Modified: Wed, 26 Oct 2022 16:50:06 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d320f81cc782b48641b14c0e479ca962c22bde6df135aecde18dec1c3954ee80`  
		Last Modified: Wed, 26 Oct 2022 16:50:06 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:2f33a48159264361e561cd91383fa5caf9571e38c748204a101ee3d5fb4d23ee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327287005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2873d3986a53dacc76add471a133090d2ba282b976f59209079cbb4b98221dad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:03:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 26 Oct 2022 01:03:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 26 Oct 2022 01:03:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 26 Oct 2022 01:04:06 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Wed, 26 Oct 2022 01:05:11 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Wed, 26 Oct 2022 01:05:11 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Wed, 26 Oct 2022 01:05:11 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 26 Oct 2022 01:05:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 26 Oct 2022 01:05:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 26 Oct 2022 01:05:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 26 Oct 2022 01:05:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 26 Oct 2022 01:05:44 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 26 Oct 2022 01:05:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 26 Oct 2022 01:05:44 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 26 Oct 2022 01:05:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 26 Oct 2022 01:05:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 26 Oct 2022 01:05:45 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 26 Oct 2022 01:05:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 01:05:45 GMT
CMD ["couchbase-server"]
# Wed, 26 Oct 2022 01:05:45 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 26 Oct 2022 01:05:46 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69873e33ecff1a1e0610419e7f10325c069fab1df9314e8aac62d17307806a3`  
		Last Modified: Wed, 26 Oct 2022 01:06:05 GMT  
		Size: 6.1 MB (6059698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85885eb367904d1df9d95279b28fdc48aec37f0d76f3f502f6f18d13ca174e82`  
		Last Modified: Wed, 26 Oct 2022 01:07:03 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8cf8dda76465be8b898111b87b06ed3de8116ffe7c62b1ba3c6508cfc51f19`  
		Last Modified: Wed, 26 Oct 2022 01:07:29 GMT  
		Size: 294.0 MB (294026940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46dfd409edf748867674a21db8d085c320e67e76c5cc2c5e33f20719aa89ad6`  
		Last Modified: Wed, 26 Oct 2022 01:07:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb370a5bd6d9b95bf80be88ad3744c9228fea4baaed1b7a274b9481f1b3c6c2`  
		Last Modified: Wed, 26 Oct 2022 01:07:01 GMT  
		Size: 742.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cef3105bb0575f2569480d8c156d9439f6a7f3e67344b944a79e54774c8b404`  
		Last Modified: Wed, 26 Oct 2022 01:07:00 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b883b2cdb33b3f0c43ac915354bd61694ca28eb3fd54660b47bdd5df7de93cba`  
		Last Modified: Wed, 26 Oct 2022 01:07:00 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c0c929056280d69ef668cb6fc451cc69cd8cc271060b97df65265405bcb5c1`  
		Last Modified: Wed, 26 Oct 2022 01:07:00 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05dda6eeaa273d177fa841fb2ef279528f0cdb7dacda379ee7b81f64f41b9d14`  
		Last Modified: Wed, 26 Oct 2022 01:07:00 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
