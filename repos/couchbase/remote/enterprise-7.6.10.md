## `couchbase:enterprise-7.6.10`

```console
$ docker pull couchbase@sha256:ec27739f541293b2f9e5dd0cd39403fac49c5e3a734fce788dcece7ecc3df7dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.10` - linux; amd64

```console
$ docker pull couchbase@sha256:d87b409a42589e355f86b8c4f86e1405a05fb4d6bbc6902484c5c702982dda61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.0 MB (834019614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92662ede4dad39f6fe74982869fe006c1eefa3a00ef0fcb6645a9e221ec981af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:49:29 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:49:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:49:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:49:29 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:50:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:50:01 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10
# Tue, 07 Apr 2026 01:50:01 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:50:01 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:50:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:50:01 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:50:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=680d6833172db7691aa0f9562aa50e044214f97cd8a785b410e828a840ce38bc            ;;          'amd64')            CB_SHA256=80938b3c86eb4cf412d9eb80b6494d96d32ce90555dc8536e0fb44a884f453ef            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:50:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:50:47 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:50:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:50:47 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:50:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:50:47 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:50:47 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:50:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:50:47 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:50:47 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:50:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97c7a2bdd7d12d4d520a510384501668d5716b8a76f76c51ff7e434ae048fc7`  
		Last Modified: Tue, 07 Apr 2026 01:51:41 GMT  
		Size: 43.8 MB (43816335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d5701847ab73917836a6c9e1fe0261d4bf0f4cc8b7e204bc0267f44f3a972e`  
		Last Modified: Tue, 07 Apr 2026 01:51:39 GMT  
		Size: 878.1 KB (878096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf08e442565fb02018f56752e608ee9b5298a3176e75ab52aef8282d8e2f4661`  
		Last Modified: Tue, 07 Apr 2026 01:51:39 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32849049f0df49766483a9ead2e1803bc541ae080a1ff71a6356f7e8e243d55d`  
		Last Modified: Tue, 07 Apr 2026 01:51:53 GMT  
		Size: 759.6 MB (759584736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30a9748c8a3ab3e2998c816c41298e36edfe86b1e6220309f99742b4215025e`  
		Last Modified: Tue, 07 Apr 2026 01:51:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7499c588542e4477aa2aa98740e6d456ba7961696652c04a6fa8539d1cdc7f78`  
		Last Modified: Tue, 07 Apr 2026 01:51:41 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eca6821fd6a9caa6d3c2c290ddebd0b3ccd064e96fb0da063f8c0bcb36ac917`  
		Last Modified: Tue, 07 Apr 2026 01:51:42 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac22ba98721308a9d8b28d89194c3055f4851e74f67159be4ac6ab1b6bd680d`  
		Last Modified: Tue, 07 Apr 2026 01:51:42 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d936b02d4e05e59219604f5346394535b590bf7865fa3cbf6b99b3d22940b1`  
		Last Modified: Tue, 07 Apr 2026 01:51:43 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536327a1813d037b66d588849690bd9398c0c7622e6a80f7d134b74cdb16f2dd`  
		Last Modified: Tue, 07 Apr 2026 01:51:43 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.10` - unknown; unknown

```console
$ docker pull couchbase@sha256:e14a3a0beecbf8b55c1903b15b9be39fb7e52b7804aee95585aabc7a759586d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b264793ea3fe691c495d0df0bacbd5ab1e1bd62177dd408bd4b23fcda35444`

```dockerfile
```

-	Layers:
	-	`sha256:170c6f0adb7d2343a458935c02051515e5089977a2fa2fad34c7ed02c6dd5f3a`  
		Last Modified: Tue, 07 Apr 2026 01:51:39 GMT  
		Size: 37.5 KB (37544 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.10` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9f40ea4f553f9b76fb86e0cb8d83e6975534d1af9165c8c757d1dde90302e920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.8 MB (796834173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb88e79808d293a70fc4b571828f42d09b860502fc031a4c9ce7664f8f7b443`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:38 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:51:38 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:51:38 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:51:38 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:52:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:52:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10
# Tue, 07 Apr 2026 01:52:07 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:52:07 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:52:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:52:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:52:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=680d6833172db7691aa0f9562aa50e044214f97cd8a785b410e828a840ce38bc            ;;          'amd64')            CB_SHA256=80938b3c86eb4cf412d9eb80b6494d96d32ce90555dc8536e0fb44a884f453ef            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:52:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:52:50 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:52:50 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:52:51 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:52:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:52:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.10 CB_PACKAGE=couchbase-server-enterprise_7.6.10-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:52:51 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:52:51 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:52:51 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:52:51 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082e68a342bb21d5b4c2040be39f7bef6cc78185186ec28230d607b077a59a78`  
		Last Modified: Tue, 07 Apr 2026 01:53:43 GMT  
		Size: 43.6 MB (43633223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffb8c1ea754ce51b3ee8640bf343b60bbf5dd505208e18b044916294f9b64eb`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 765.0 KB (764995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e739857c63cf590a247393c930729a5a9623304f30f26a50be14b537674450b`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3d5ff127722daf4ce7746da94b8f8664cef273a613aac55aeddcc281acf171`  
		Last Modified: Tue, 07 Apr 2026 01:53:55 GMT  
		Size: 723.6 MB (723554896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ac962399ed5c1d18c7bfed5eae37d3e249bd9338dd27ff4dd3b54bf62a0684`  
		Last Modified: Tue, 07 Apr 2026 01:53:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb6f13f2bea5000907af714de0394768ab200f6dd7ddc65536e440aac7513ab`  
		Last Modified: Tue, 07 Apr 2026 01:53:42 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9020e5fbf3086dbd9ef780921e04d706ca3217e6d1c6271ba14ab9cd230e2f5`  
		Last Modified: Tue, 07 Apr 2026 01:53:43 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd98ac1a11925d37335c9315f35e08b87393296a1ec16c9ffebb88160b0cb65`  
		Last Modified: Tue, 07 Apr 2026 01:53:44 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d78728db29743935a8be4245c8fe332152a1b10f3818b037e85751180d7153`  
		Last Modified: Tue, 07 Apr 2026 01:53:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7bba881d635e1d082918cb108b128d9c02478faf0fef347ea02e02d9374efe`  
		Last Modified: Tue, 07 Apr 2026 01:53:45 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.10` - unknown; unknown

```console
$ docker pull couchbase@sha256:2525fdf1a5d743f94e25fa6d8c24ef43394c3406b2773b944fc1a4bd5fbb65e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02a97cceda5948e18b983010b5ee81b0ffde627034c585f6df9baf9180987b2`

```dockerfile
```

-	Layers:
	-	`sha256:45727c44a9d490b2c6e7fee0739083ba0c373733b8ab43b52f4184c1fa590435`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 37.7 KB (37729 bytes)  
		MIME: application/vnd.in-toto+json
