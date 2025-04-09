## `couchbase:community-7.2.2`

```console
$ docker pull couchbase@sha256:3df2941e779a1d8ec526beb3de0a2b62bf9e0d477860d509c2fa1efb5ab64f40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:0b65b82a32d500babdc7918fd53dc60e8da1fbbfaa03bcbbd815ef01fc70989c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360347023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988ddbeb7a3bf818934c7e0999e02f31b2f7f5aad06bb6ba66d1512c1d1246c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 25 Sep 2023 18:22:30 GMT
ARG RELEASE
# Mon, 25 Sep 2023 18:22:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 25 Sep 2023 18:22:30 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 25 Sep 2023 18:22:30 GMT
CMD ["/bin/bash"]
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 25 Sep 2023 18:22:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Sep 2023 18:22:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 18:22:30 GMT
CMD ["couchbase-server"]
# Mon, 25 Sep 2023 18:22:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 25 Sep 2023 18:22:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f5614342c8617d8d96afb5a4f8f9918da6338dcfe1f5f47380a9a8b12cb2e7`  
		Last Modified: Wed, 09 Apr 2025 01:13:55 GMT  
		Size: 6.3 MB (6295130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0662daf09c3ef65dbbfd7eec2f8efed9f8e14d9e9d88a1bdd218dde2132fbe`  
		Last Modified: Wed, 09 Apr 2025 01:13:55 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed69a42399e487cd2875401ac34f02dfe254c8804f604ed1ea703d46984f8f7`  
		Last Modified: Wed, 09 Apr 2025 01:14:01 GMT  
		Size: 326.5 MB (326537200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb818fd896c98f339d6eb7c1fbee25caca2d1cd9ed5bfe12531d6e49e94ef045`  
		Last Modified: Wed, 09 Apr 2025 01:13:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115411cbabe74bf70ece397012b3ba0d9e7e6cde814298d91ac361930345ce87`  
		Last Modified: Wed, 09 Apr 2025 01:13:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bf65398f8e81805921e2f1efdb4b5cb971866337976f6ff9c293f25276b6ee`  
		Last Modified: Wed, 09 Apr 2025 01:13:56 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33d5dea9b2c06084e821b0a38a981c3f7ff0ae02bd4e643a29a9fed86db2afb`  
		Last Modified: Wed, 09 Apr 2025 01:13:56 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77e6439cac1def5b58937a2c671c3a28ed2eb8bb6f67d0d39de00220664345c`  
		Last Modified: Wed, 09 Apr 2025 01:13:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3eb49d5a28ea9ce800a96cf72a3a7ec6c6ed1b5518bb0cad729626daad9179a`  
		Last Modified: Wed, 09 Apr 2025 01:13:56 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:12bf180723ab5c10f48cdb38c66362651e83aa8fe216fe51d6bba2118edcf368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d3e285f011e35e2ace00f82ea4190074a86ef7b0eb01a2bcb877b573d516cb`

```dockerfile
```

-	Layers:
	-	`sha256:58396e4f8e843e725eeeceaa9cad111a35e5142ead987b8f26c7113f4c95033e`  
		Last Modified: Wed, 09 Apr 2025 01:13:55 GMT  
		Size: 31.5 KB (31500 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:0d472cc730c8a8dafec87cdbaa35ea48f3ba5640f8bc8df67626516d34dddffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336810539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703d26e7a924f1945087b50dc4981fd97a2f342d6b0c5eca93630e3747960d90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 25 Sep 2023 18:22:30 GMT
ARG RELEASE
# Mon, 25 Sep 2023 18:22:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 25 Sep 2023 18:22:30 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 25 Sep 2023 18:22:30 GMT
CMD ["/bin/bash"]
# Mon, 25 Sep 2023 18:22:30 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 25 Sep 2023 18:22:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Mon, 25 Sep 2023 18:22:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Sep 2023 18:22:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 25 Sep 2023 18:22:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 18:22:30 GMT
CMD ["couchbase-server"]
# Mon, 25 Sep 2023 18:22:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 25 Sep 2023 18:22:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbd3b6d8b3dd5d4ede9235b28df451d880e2947c78240a111c0abd42143dbaa`  
		Last Modified: Wed, 09 Apr 2025 06:46:17 GMT  
		Size: 6.1 MB (6124748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec987c84f658d1d75b18f0e91f121bc3cd34237e806a44b3e3db8b17748989a`  
		Last Modified: Wed, 09 Apr 2025 06:53:08 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc7fcd55ff69d8777dd743c37a6e3af775f77835a2954ae77d46da976c5f03`  
		Last Modified: Wed, 09 Apr 2025 06:53:15 GMT  
		Size: 304.7 MB (304703815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ccf18726885e3fe4b4eace9b14d0d5f763ff3ec9a2f7094e68f88af26dd1d`  
		Last Modified: Wed, 09 Apr 2025 06:53:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaf741eff860af5a49e57381bb16ed132c9a607db50f60795890ba4f0976372`  
		Last Modified: Wed, 09 Apr 2025 06:53:08 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125960193c4635ee4073fc848c9b4ecc65b23fcf618d657e5ff1c4c01ab0114d`  
		Last Modified: Wed, 09 Apr 2025 06:53:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf998ac2e2bb9092eb21d7ecfbe01fd370e3555fad489da6c71859fac78e5cf`  
		Last Modified: Wed, 09 Apr 2025 06:53:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb1838dde463a454e4ef5d24859bfb9dc53be07d20354a2b7a6a2b6d6022d87`  
		Last Modified: Wed, 09 Apr 2025 06:53:09 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f2974660c7f4af0c87e45fc3a8fa7f3237dac0c27ae4277d6ef1b6b4ade546`  
		Last Modified: Wed, 09 Apr 2025 06:53:10 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:7d7bc3c4fcb930dc1223c332e096f55693bde59b8be3dbe46a64795e36e54d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc2aed2bd5f991cc33bf009dea9b3b1cfa327eee50bb706703f7491a1c1a64a`

```dockerfile
```

-	Layers:
	-	`sha256:1ee7afb0fe12f63112ebd1fcfb2d0917e238090792189113e99b4d22e13a333e`  
		Last Modified: Wed, 09 Apr 2025 06:53:08 GMT  
		Size: 31.7 KB (31657 bytes)  
		MIME: application/vnd.in-toto+json
