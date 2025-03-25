## `couchbase:community-7.2.2`

```console
$ docker pull couchbase@sha256:595e16d459c3cbd3c1ce3cb485ef153e280ad21dd849a9dfd282a3c8d4208539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:62f151dadf2fd6337e92793113a0e35cb20aba626d1a3eb362fa7d2915ef133c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.6 MB (361639829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb146e4290888fe5f9fbbe09acf4533435e461e2540c433a8e62ba41e067864`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:25:59 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Dec 2023 10:26:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 16 Dec 2023 10:26:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:26:18 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Sat, 16 Dec 2023 10:27:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Sat, 16 Dec 2023 10:27:53 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Sat, 16 Dec 2023 10:27:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 16 Dec 2023 10:27:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Dec 2023 10:27:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Dec 2023 10:28:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:28:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Dec 2023 10:28:32 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Sat, 16 Dec 2023 10:28:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Dec 2023 10:28:33 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Dec 2023 10:28:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Dec 2023 10:28:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 16 Dec 2023 10:28:34 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Sat, 16 Dec 2023 10:28:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Dec 2023 10:28:34 GMT
CMD ["couchbase-server"]
# Sat, 16 Dec 2023 10:28:34 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 16 Dec 2023 10:28:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78735bf4de6f426e7422bf3d534899d82db0f0d2d66034d6db341ce8d26f0b2`  
		Last Modified: Sat, 16 Dec 2023 10:35:19 GMT  
		Size: 6.3 MB (6286008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c3a9d3cb6c526925edd4e69fa9d0990cb8cecddf132fcf4f86f9536a56db67`  
		Last Modified: Sat, 16 Dec 2023 10:36:28 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef661a7a9296aac37cd7bf10d5a50280d8ee10c386944e4599279a5db3b0354`  
		Last Modified: Sat, 16 Dec 2023 10:37:04 GMT  
		Size: 326.8 MB (326765439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53d388f93f0ad0ea8c540b7ed3761f85e7917e2406ab4ef76f7253b9e755230`  
		Last Modified: Sat, 16 Dec 2023 10:36:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb942f563d81c6d8b5f0476d611d0a79c83b3fb438dca2973f744ce7fca4f6`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0faf6729f915640d095fab3205ee40f6fd399158209063aba0ac8cf2546db8f`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd2f79c6cafef10a2535b7521673f3d89c42ee1d0a13134621f916775ad8d3d`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a42de1c1afb3a842f4ae40b286db8faa306721a1de89c7b755451e90e0df411`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aabf49d9c8c2cc3e7859716d2c0e97d4cad160b60232995aab7c94aff88e1ac`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:0e71cd9041434b67a8ed669b2ba28e7e22cd516c9fadef397e9aa662e83b265e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338249089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a16d4915eeab0c1d4bb08cfd5a32d421146915aae8ffa984a7977a96a9301f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:54:01 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Dec 2023 09:54:01 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 16 Dec 2023 09:54:01 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 09:54:19 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Sat, 16 Dec 2023 09:55:39 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Sat, 16 Dec 2023 09:55:39 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Sat, 16 Dec 2023 09:55:39 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 16 Dec 2023 09:55:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Dec 2023 09:55:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Dec 2023 09:56:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 09:56:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Dec 2023 09:56:20 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Sat, 16 Dec 2023 09:56:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Dec 2023 09:56:20 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Dec 2023 09:56:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Dec 2023 09:56:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 16 Dec 2023 09:56:21 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Sat, 16 Dec 2023 09:56:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Dec 2023 09:56:21 GMT
CMD ["couchbase-server"]
# Sat, 16 Dec 2023 09:56:21 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 16 Dec 2023 09:56:21 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a83d6afdb30f174382ab5039378b0bae25520129e600a54c8d3a1ee404eeae`  
		Last Modified: Sat, 16 Dec 2023 09:58:48 GMT  
		Size: 6.1 MB (6109493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9cfa47d30bfa7e8ca05f5797557a777657738f99ee228681baa7829b81743d`  
		Last Modified: Sat, 16 Dec 2023 09:59:43 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560066726de56cdbf85086fa375e8aaa3490ad7ec7b2d726168e914f159e9f0d`  
		Last Modified: Sat, 16 Dec 2023 10:00:10 GMT  
		Size: 304.9 MB (304932093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9868a5a67ca556a81eca3a8b8a376b854253e6990f23e0a1bd4f723bb3215f`  
		Last Modified: Sat, 16 Dec 2023 09:59:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2edb90f91027b3900421acd294554fa85c09bc64743aa6bd7060540ab6fe16`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2528581d204a073bc6362932f258b934d85fddd27aecd90eff2639b09ff29429`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1f3846ba9dc058b43529d7eda2a6aec9e2b0e8d3ab840b432a8b2e6aa11b57`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b305cff2a968879e35a48bd10b29792fe4c5629da0039c610ad86d19fce9b36`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f339cd1b5b19f55445503e45222e6ee3317c30590b15ab5560d90e34b81a63bd`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
