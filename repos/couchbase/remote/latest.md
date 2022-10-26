## `couchbase:latest`

```console
$ docker pull couchbase@sha256:de814bf9d211e4e8bed47b4f30b9a6bb9ed5d37f54419f2dd5f03a6c41367fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:c5d5e613e63ea9db16594563e58bd9ed20fa725d57e05bb3b15e448e4e86eda2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600055587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61ee8695acd2fabfeaf9c36a80a27f7f47b59b8935394da7f5e6282982f778a`
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
# Tue, 25 Oct 2022 15:57:44 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2
# Tue, 25 Oct 2022 15:57:44 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb
# Tue, 25 Oct 2022 15:57:44 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 25 Oct 2022 15:57:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 25 Oct 2022 15:57:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 25 Oct 2022 15:58:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1c7c757cf8aee87b98c96ffea1c26f4c98b6e0c053d966c8e760224030d98477            ;;          'amd64')            CB_SHA256=26fd9ae8585e0ea6637d4f1b492ed637dcf06d664a49d369e1faf0782327b3ec            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 15:58:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 25 Oct 2022 15:58:48 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 25 Oct 2022 15:58:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 25 Oct 2022 15:58:49 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 25 Oct 2022 15:58:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 25 Oct 2022 15:58:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 25 Oct 2022 15:58:50 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 25 Oct 2022 15:58:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Oct 2022 15:58:50 GMT
CMD ["couchbase-server"]
# Tue, 25 Oct 2022 15:58:51 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 25 Oct 2022 15:58:51 GMT
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
	-	`sha256:59bb854befefa6e7044798c56d5fefec1df188159b7a828006b108061583b651`  
		Last Modified: Tue, 25 Oct 2022 16:05:55 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef8813a4118b27310b9f2ae576098f0466002f73051bcd0c41d87881230456c`  
		Last Modified: Tue, 25 Oct 2022 16:06:53 GMT  
		Size: 565.2 MB (565241167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b6110a6e0a8a011e9d06d1f4b393b98e95b2e8e8321f19f97fad5ad647200e`  
		Last Modified: Tue, 25 Oct 2022 16:05:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84133c50c5a5257de7ef7c9fbc238971b91d3ba82a3030cb7f4689d17b149da8`  
		Last Modified: Tue, 25 Oct 2022 16:05:52 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3ff0f1e05f7f5027f3506bb9ba0d33c4e42c326c79db87cfa282126baf4ee1`  
		Last Modified: Tue, 25 Oct 2022 16:05:52 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a36162db4485c16b1a4ce5339d76ae9f918e6fc78e016ed8f47bb9ed78e1654`  
		Last Modified: Tue, 25 Oct 2022 16:05:52 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0b25ea9c9f233887e0cca0dfb333cc923bee89c184696fdcc87876b76cf1de`  
		Last Modified: Tue, 25 Oct 2022 16:05:52 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642d1e5f8827027f015fbd8f55f82fe2e4a79d720bf61cf26b8870ed3ce9ebfd`  
		Last Modified: Tue, 25 Oct 2022 16:05:52 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:latest` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9a4888c0ce9651cb27020be56956c4fd3fe39cd7160fdfd8b70ca2566d34f73d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.1 MB (574088800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf41ad4fdd68f8d6b24fcded6b8c122c9dad0c51bb24da871bc1d1e539178035`
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
# Wed, 26 Oct 2022 01:04:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2
# Wed, 26 Oct 2022 01:04:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb
# Wed, 26 Oct 2022 01:04:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 26 Oct 2022 01:04:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 26 Oct 2022 01:04:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 26 Oct 2022 01:04:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1c7c757cf8aee87b98c96ffea1c26f4c98b6e0c053d966c8e760224030d98477            ;;          'amd64')            CB_SHA256=26fd9ae8585e0ea6637d4f1b492ed637dcf06d664a49d369e1faf0782327b3ec            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 26 Oct 2022 01:04:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 26 Oct 2022 01:04:57 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 26 Oct 2022 01:04:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 26 Oct 2022 01:04:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 26 Oct 2022 01:04:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 26 Oct 2022 01:04:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 26 Oct 2022 01:04:59 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 26 Oct 2022 01:04:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 01:04:59 GMT
CMD ["couchbase-server"]
# Wed, 26 Oct 2022 01:04:59 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 26 Oct 2022 01:04:59 GMT
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
	-	`sha256:42689a7d037c118c8f80945e03eb3fd86160497a905592fa09c4ad52760b2b37`  
		Last Modified: Wed, 26 Oct 2022 01:06:04 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea073f8f3543b1e17d23d96c5ddee5e7e0fa40de1d6e740361a8db5b0684d9a9`  
		Last Modified: Wed, 26 Oct 2022 01:06:44 GMT  
		Size: 540.8 MB (540828733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449cffd4bc6ce1b1fa337cfb7fd331588a756d55d794a7fb1889959450bddd77`  
		Last Modified: Wed, 26 Oct 2022 01:06:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef5720f1eac34c77d45c499a897539d9df7a9cff9361429069c9fab9124685f`  
		Last Modified: Wed, 26 Oct 2022 01:06:02 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e51ea8f00f9893468229bde542313cf22eb5fa1412a6339966d9ed593d8431`  
		Last Modified: Wed, 26 Oct 2022 01:06:02 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcca3cf917e817b273da193851219e829d9f191e5ea52aa12cbf6747d214cb4`  
		Last Modified: Wed, 26 Oct 2022 01:06:02 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6780a517c5f36d3b34dcd2960ba09ade2a87ef09b5da610cd9f50c1124df15`  
		Last Modified: Wed, 26 Oct 2022 01:06:02 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b05bbb83aa2d245e2d34a933fdd2eeef43dbb905a169074d507b4b11dadc5d`  
		Last Modified: Wed, 26 Oct 2022 01:06:02 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
