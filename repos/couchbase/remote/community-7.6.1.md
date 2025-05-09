## `couchbase:community-7.6.1`

```console
$ docker pull couchbase@sha256:031dac85db8ad3c35413661ecded09dfd1acb13e9e12b0d4d9b8d8fd08194ec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:0612712ed223cccb421f5d0a92be981c4d82d141298967386fe578e9e8b91746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384403309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6ab32dbee2e9521f9d77df178a79cd524f46c2fdfc3fa2aecad827041afb0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 03 Apr 2024 01:33:25 GMT
ARG RELEASE
# Wed, 03 Apr 2024 01:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 03 Apr 2024 01:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 03 Apr 2024 01:33:25 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 03 Apr 2024 01:33:25 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Wed, 03 Apr 2024 01:33:25 GMT
CMD ["/bin/bash"]
# Wed, 03 Apr 2024 01:33:25 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 03 Apr 2024 01:33:25 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 03 Apr 2024 01:33:25 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 03 Apr 2024 01:33:25 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Wed, 03 Apr 2024 01:33:25 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 03 Apr 2024 01:33:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Apr 2024 01:33:25 GMT
CMD ["couchbase-server"]
# Wed, 03 Apr 2024 01:33:25 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 03 Apr 2024 01:33:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4f37d65067a78acfc2f2605720418ad9bb4a976cc803e8b141459ee982dd19`  
		Last Modified: Wed, 09 Apr 2025 01:13:44 GMT  
		Size: 6.2 MB (6200227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4706ad7334f019848aee6cecce4e48ddfd08782427c3056f2ef7f6346ba6b7d`  
		Last Modified: Wed, 09 Apr 2025 01:13:44 GMT  
		Size: 864.3 KB (864270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f9fb24c5a336c33d985762755cd3a82cc9afc49ca5b89246e67389b149155b`  
		Last Modified: Wed, 09 Apr 2025 01:13:44 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b8a56448e2856ec518e98f29c6b84701306e5af00a6cf24f70d174c34d8c37`  
		Last Modified: Wed, 09 Apr 2025 01:13:50 GMT  
		Size: 349.8 MB (349823732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddcc2bc53006d410fe8923873f4c52ff54dbef27bdf99c9340942c7dacda14a`  
		Last Modified: Wed, 09 Apr 2025 01:13:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3522700088e66e3188154af6074bd0b0609d361b4653a1e7501e2a27a8c32b`  
		Last Modified: Wed, 09 Apr 2025 01:13:45 GMT  
		Size: 661.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119b261a7ef5ca34b40397d51870bd23c9e5ad2e974ad9b94f5035a6fd73f482`  
		Last Modified: Wed, 09 Apr 2025 01:13:45 GMT  
		Size: 694.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61078b5d7a3e0e301de81bc96b764caa531bc49f375293bcaf64cf8ebd576a11`  
		Last Modified: Wed, 09 Apr 2025 01:13:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b465286cf38d259d23dc2fd6e85724330b7ecc57a2e58b89f8035e5df2d704`  
		Last Modified: Wed, 09 Apr 2025 01:13:45 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b2f3dd85cac364d1af5b2db5aed95dd4111d82372316ecfd14f18b33dc38b7`  
		Last Modified: Wed, 09 Apr 2025 01:13:46 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:6cdab660848365fcf099646d0de947e9b3817081cc6f110eae9bb537324bc43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 KB (35442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbd31e8ca297992a8196f68cdf3b5b601708c630273c35e081dd1ddcf52d6a7`

```dockerfile
```

-	Layers:
	-	`sha256:253b7ba3776584a30d174afb9ba3248d7853c00e1d3a00ded99cbefb794d2fbe`  
		Last Modified: Wed, 09 Apr 2025 01:13:44 GMT  
		Size: 35.4 KB (35442 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:a493dca7a66c8807d3de84fa403675b5101905df279498322e4749800ed4150d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366104323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4987b2b1f11660c552b3ff28ca34c51969bf245a85ef9566a5358969b3477a6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 03 Apr 2024 01:33:25 GMT
ARG RELEASE
# Wed, 03 Apr 2024 01:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 03 Apr 2024 01:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 03 Apr 2024 01:33:25 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 03 Apr 2024 01:33:25 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Wed, 03 Apr 2024 01:33:25 GMT
CMD ["/bin/bash"]
# Wed, 03 Apr 2024 01:33:25 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 03 Apr 2024 01:33:25 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 03 Apr 2024 01:33:25 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 03 Apr 2024 01:33:25 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Wed, 03 Apr 2024 01:33:25 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 03 Apr 2024 01:33:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 03 Apr 2024 01:33:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Apr 2024 01:33:25 GMT
CMD ["couchbase-server"]
# Wed, 03 Apr 2024 01:33:25 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 03 Apr 2024 01:33:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ccdccb08ab290f1bf5f33c9b3a1de3e29ab99b5710fa7325de743454880281`  
		Last Modified: Wed, 09 Apr 2025 06:30:35 GMT  
		Size: 6.0 MB (6036543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44c4d997a0d024e276867f67d250c5b7f3b7980a7de4c0fe0ea2b4169c01c46`  
		Last Modified: Wed, 09 Apr 2025 06:30:35 GMT  
		Size: 711.8 KB (711813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc16995dff8e6a6eb00fc0a30725f8f2b67b1c94a6841cf58ad4f5d77f0a9d`  
		Last Modified: Wed, 09 Apr 2025 06:34:22 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdbfb021525559fd5edfd3f33504e7805c292b4f9a00372260b1117190ac81`  
		Last Modified: Wed, 09 Apr 2025 06:34:30 GMT  
		Size: 333.4 MB (333373611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a253e1763b7f4755d632cc8e9c1e856c3aa0e35b1325e4aaee40740c4bb48d1`  
		Last Modified: Wed, 09 Apr 2025 06:34:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414d1039f7441260a87278079a862487e5e5547c8ff657a004a8649447fc5b8d`  
		Last Modified: Wed, 09 Apr 2025 06:34:22 GMT  
		Size: 660.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92d726e81e5bad87687688f6598d4a1ef9189955ef85ebc9815c000e4bc5511`  
		Last Modified: Wed, 09 Apr 2025 06:34:23 GMT  
		Size: 693.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5848707860539fe35734d93dac7704e2c1b7ebb27f8e648bd5d20c74ec726a`  
		Last Modified: Wed, 09 Apr 2025 06:34:24 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf8cb8de8adb3ef7ebd008d890a7a7366212bea3312a929029aef2456f0bdca`  
		Last Modified: Wed, 09 Apr 2025 06:34:24 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9efe5df59688b94281810b1c993e9ef82e653f9df62cef8b053f859eb110080`  
		Last Modified: Wed, 09 Apr 2025 06:34:24 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:347297e3efee3333955855011c6833ab0512b3e983d666bfddb3191c6157214a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2051cd3a758103a1b1c4ffe6b8b580b8220853984ced91fa6c15c51764296958`

```dockerfile
```

-	Layers:
	-	`sha256:51d758761d8fbf7398abbde7ad5b8f3715ea931ecfb0d262485464a821c1c341`  
		Last Modified: Wed, 09 Apr 2025 06:34:22 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json
