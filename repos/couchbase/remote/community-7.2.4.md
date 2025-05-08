## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:ed4094e7149b5ca69df6e97491ba31e053829e72fa72dac48a2bec18cd25bf54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:e6def45df225a205c7f8359d809ea8f59d5fc34f51e38f900fd0aadbd6103c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364883794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0472193ba51acbedfb4e5e956fe6f2d4432e25be5cfb72339c87712a67c1c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 25 Jan 2024 18:02:30 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:02:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:02:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:02:30 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 25 Jan 2024 18:02:30 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Thu, 25 Jan 2024 18:02:30 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 18:02:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 25 Jan 2024 18:02:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 25 Jan 2024 18:02:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 25 Jan 2024 18:02:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 25 Jan 2024 18:02:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Jan 2024 18:02:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jan 2024 18:02:30 GMT
CMD ["couchbase-server"]
# Thu, 25 Jan 2024 18:02:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 25 Jan 2024 18:02:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8962f861b7d76e47d85d88fb5b838f40f088df85732f65fdb0f584369dd7763f`  
		Last Modified: Wed, 09 Apr 2025 01:14:03 GMT  
		Size: 6.3 MB (6295168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6d8881bf4bce240619faca11b20cd85373fbf169bcb31474243995c87e4354`  
		Last Modified: Wed, 09 Apr 2025 01:14:03 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebae0ba48f83c4b6a16c94d66e47f1de60a09a8010da01f27f6a48f561b8534e`  
		Last Modified: Wed, 09 Apr 2025 01:14:08 GMT  
		Size: 331.1 MB (331073939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076efa23bff7b7d4e1be0ad6dee1181d2d79bd201a872bedd7f60eab9618c88d`  
		Last Modified: Wed, 09 Apr 2025 01:14:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcf40dd1f36f61abdb3410f38da5ea2868a742279f6ea749739138fe73523c4`  
		Last Modified: Wed, 09 Apr 2025 01:14:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a066027c7fb9e47576391628b66b31761d5de1487d692ac27ed3cf9e110b5a06`  
		Last Modified: Wed, 09 Apr 2025 01:14:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3990eb514cddb596bf2f5ff1f1faa387542a3cd4495005b721c965ab429c234f`  
		Last Modified: Wed, 09 Apr 2025 01:14:04 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcda11cb2036e964de6c5a643da764f6e5994695397c5286c3e313ef26d6a13`  
		Last Modified: Wed, 09 Apr 2025 01:14:05 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f950b4e7076606a667a89c450a705a4bdbfc421bcbe258558dbbcfcfeb2a1ee`  
		Last Modified: Wed, 09 Apr 2025 01:14:05 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:d11d7c2e28fd8b371cb0fea468d2b8cd1349089dd652e9870b82e930104fa85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69913134eb34fa034b24caea89e66737cd0bf2dc91d1f91e26e7eef9d1b3d68`

```dockerfile
```

-	Layers:
	-	`sha256:a2799bf5f1346e7adaacb88a324f227a84d3d94eca29254662e75935c1ddc2b2`  
		Last Modified: Wed, 09 Apr 2025 01:14:03 GMT  
		Size: 31.5 KB (31499 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:c796cdc5ad58e5fe95207422ef52fcd5e306c7a15cebf279565a98e9db295f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344969441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e9e6d66d4084cf7a79f9408b21bdd803b16b68ce0509b795bb0ad708ac0ccc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 25 Jan 2024 18:02:30 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:02:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:02:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:02:30 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 25 Jan 2024 18:02:30 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Thu, 25 Jan 2024 18:02:30 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 18:02:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 25 Jan 2024 18:02:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 25 Jan 2024 18:02:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 25 Jan 2024 18:02:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 25 Jan 2024 18:02:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Jan 2024 18:02:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 25 Jan 2024 18:02:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Jan 2024 18:02:30 GMT
CMD ["couchbase-server"]
# Thu, 25 Jan 2024 18:02:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 25 Jan 2024 18:02:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbd3b6d8b3dd5d4ede9235b28df451d880e2947c78240a111c0abd42143dbaa`  
		Last Modified: Thu, 08 May 2025 17:33:02 GMT  
		Size: 6.1 MB (6124748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3065722c79ea7867be5714366ed4702ab3a598ba827abbe400aa650bef852d06`  
		Last Modified: Wed, 09 Apr 2025 06:47:41 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79f9cee01b74f557624da81534ab817e9ee1bb12eaf8c810cf37a75f459122f`  
		Last Modified: Wed, 09 Apr 2025 06:47:51 GMT  
		Size: 312.9 MB (312862718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a45c2cef06774714bab6de2fba3bcba3fe67ff127eb1ed9eadb0224d8a266`  
		Last Modified: Wed, 09 Apr 2025 06:47:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4357714e6be91bedeebb922585898f584629c05651dba85dc98e0474b0d8c10`  
		Last Modified: Wed, 09 Apr 2025 06:47:41 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb2c9981cc729dc2991ac8366a5c70f40e1e672af15b4b2c55ac76095954067`  
		Last Modified: Wed, 09 Apr 2025 06:47:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895b3673ea6135e25bd48eac769276734f9b4478b10d69ebf50f2bf886a5788a`  
		Last Modified: Wed, 09 Apr 2025 06:47:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e7931e41ec20b56f67c71cb320891138c4b2c64410742ec042d31081fec7b1`  
		Last Modified: Wed, 09 Apr 2025 06:47:42 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d8eb5584d9a177d5f3716cbeb0799fc0803015154b83a0344a8d2336e18538`  
		Last Modified: Wed, 09 Apr 2025 06:47:44 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:2cb6843e8f78d1375ab47570737529bcd7c501ab3455028366a17f0a707f2ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648f30df103b143e10256257476b887ab069d9b22de8bd817b64530da9cf4e3a`

```dockerfile
```

-	Layers:
	-	`sha256:8ff461b6afa7cc7c3f962c432441448e3c17388f51e5224e602bfe8d29f762e4`  
		Last Modified: Wed, 09 Apr 2025 06:47:41 GMT  
		Size: 31.7 KB (31657 bytes)  
		MIME: application/vnd.in-toto+json
