## `couchbase:enterprise-7.6.1`

```console
$ docker pull couchbase@sha256:b13d4729f6f87f0e21be3689aedce17e2659f4aa86b6a3a7c10e8b3db3529c93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:2ba1d7245ae22ad8d9f34cca3da61452f9e4976d1456ca06cfcbfa475cfba71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.6 MB (724627201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccaed77070792b9e9ea45a32573805c9670e1b19252d7344affbb5c19e0b353`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 03 Apr 2024 01:29:26 GMT
ARG RELEASE
# Wed, 03 Apr 2024 01:29:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 03 Apr 2024 01:29:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 03 Apr 2024 01:29:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 03 Apr 2024 01:29:26 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Wed, 03 Apr 2024 01:29:26 GMT
CMD ["/bin/bash"]
# Wed, 03 Apr 2024 01:29:26 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 03 Apr 2024 01:29:26 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 03 Apr 2024 01:29:26 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 03 Apr 2024 01:29:26 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Wed, 03 Apr 2024 01:29:26 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 03 Apr 2024 01:29:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Apr 2024 01:29:26 GMT
CMD ["couchbase-server"]
# Wed, 03 Apr 2024 01:29:26 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 03 Apr 2024 01:29:26 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a33d9204ca599758c70ffb0b3f4651fbdca2e3c9dde66158c90ae097fa16b3`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 6.2 MB (6200212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e8c650df720ad1b76e42ef27640acfd7231cda60d60203b5c3b1729f480ec`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 864.3 KB (864262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8816ea82a59b14b668f6a14c0f56c4afb3fa55a9471f4164bf78d867fa052c`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cbdf76fc7887c0f36e0bf14935cfe49315cab68e7933fa02930fcb709903ef`  
		Last Modified: Thu, 08 May 2025 17:15:38 GMT  
		Size: 690.0 MB (690047647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b222906c44f8c3431d0686d3c47beee4e917e32fed2a21e664806ec533e410`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830b5bff93c9bf94e5523ab9a3c0f6981ae8ec8a739d879ef993e5d319b84edd`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 661.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0263b1e66f5d1cab5ac0b472adaec34e9c54ca3258aa73a440c5ff65069a6d1a`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 694.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b30392fba3af40113889506f3e1ed4a9e2ba587191b683073f6ae30fa72c29c`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189051d5b52eafe05d4e3692519924d41a8419095f296051121e2fc0900ee801`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8448f5d3c0e940c9c88862ce24afd835587c6aff7727f97033de51d96a7f21`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:47d776dec20c96fd9bb15b3afd708f6ecfd151cb7160f6cdf9fc9af3330beaba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3eb9045548e365b6ee3ecfe02abb391dd457986d6bbcbbcc976124c1219d40`

```dockerfile
```

-	Layers:
	-	`sha256:472bc7004d54baa7089832ed8407329d9e26a82174a1a52303a75ce17c9308bc`  
		Last Modified: Wed, 09 Apr 2025 01:14:14 GMT  
		Size: 35.8 KB (35755 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:02d83036572f21ebf73851abffebefda7b747849117ccd7f1bb576e3370de078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.6 MB (697623801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91403681916783f85024a8c0c377eadd305aec6090ea6cb1e62e554d3e1addc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 03 Apr 2024 01:29:26 GMT
ARG RELEASE
# Wed, 03 Apr 2024 01:29:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 03 Apr 2024 01:29:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 03 Apr 2024 01:29:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 03 Apr 2024 01:29:26 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Wed, 03 Apr 2024 01:29:26 GMT
CMD ["/bin/bash"]
# Wed, 03 Apr 2024 01:29:26 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 03 Apr 2024 01:29:26 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 03 Apr 2024 01:29:26 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 03 Apr 2024 01:29:26 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Wed, 03 Apr 2024 01:29:26 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 03 Apr 2024 01:29:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 03 Apr 2024 01:29:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Apr 2024 01:29:26 GMT
CMD ["couchbase-server"]
# Wed, 03 Apr 2024 01:29:26 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 03 Apr 2024 01:29:26 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ccdccb08ab290f1bf5f33c9b3a1de3e29ab99b5710fa7325de743454880281`  
		Last Modified: Thu, 08 May 2025 18:01:31 GMT  
		Size: 6.0 MB (6036543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44c4d997a0d024e276867f67d250c5b7f3b7980a7de4c0fe0ea2b4169c01c46`  
		Last Modified: Thu, 08 May 2025 18:01:27 GMT  
		Size: 711.8 KB (711813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c46a95d479ccd8b998b2ffa9cdd1ea8e387e68719940988202d618205ca1702`  
		Last Modified: Wed, 09 Apr 2025 06:32:46 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bab168e1d722819a3124a6ec774c56013c496e94781b2883d451ff3e37b5b8`  
		Last Modified: Wed, 09 Apr 2025 06:33:02 GMT  
		Size: 664.9 MB (664893093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59d183832a7e162294cf8b41f5097c7c065380a5a3866e715f4decef2b6e5d0`  
		Last Modified: Wed, 09 Apr 2025 06:32:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2955e4450914df0437f7c49c8a9237ef9d7a7b469c536e535f09ef81d717d9d`  
		Last Modified: Wed, 09 Apr 2025 06:32:46 GMT  
		Size: 659.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cc44b2a3220b771badda05c6fb67502a604f15ad4ae6004a1cc56f01a7ab79`  
		Last Modified: Wed, 09 Apr 2025 06:32:47 GMT  
		Size: 692.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e251c97b1ed1942b670728ec1a9cf45b241c60e7840296d4af10c39312e3f24`  
		Last Modified: Wed, 09 Apr 2025 06:32:47 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aa19109ecbb6395ca6438aa2fc5c7b26317c474847250b5794bbd38fb57b8c`  
		Last Modified: Wed, 09 Apr 2025 06:32:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f38fd1fa3dbdf54b2dad5777be70bde44b4465cc7a45d7c223691855f216cb`  
		Last Modified: Wed, 09 Apr 2025 06:32:49 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:1aa507f40076bbc20ae7ec6ff188ca1e024359de628489738525430c364fbd2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 KB (35940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacf479d52a6877befc93ec0b6d31db497dd595b8062e0592b7a439d452bf302`

```dockerfile
```

-	Layers:
	-	`sha256:117a4a021075196073748a6a298b2c9b09ac96936478c2caf954ba9e46db1fa1`  
		Last Modified: Wed, 09 Apr 2025 06:32:46 GMT  
		Size: 35.9 KB (35940 bytes)  
		MIME: application/vnd.in-toto+json
