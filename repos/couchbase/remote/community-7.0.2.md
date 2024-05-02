## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:94ec213bb8690e8dc1efed21c32911e7116681752a39a25763daba89e8feec74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:fefa8d1b7dd1019f6b2db7719b83fb7fe60a91c73779bab432cdf52117310c70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429074721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5b53b30df9d465757e1a0a515f1fc73c9b6d37c749e043f9ce317d92d304c0`
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
# Thu, 02 May 2024 00:58:10 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:58:11 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 02 May 2024 00:58:11 GMT
ARG CB_VERSION=7.0.2
# Thu, 02 May 2024 00:58:11 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Thu, 02 May 2024 00:58:11 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Thu, 02 May 2024 00:58:11 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Thu, 02 May 2024 00:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:58:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:59:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:59:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:59:06 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:59:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 May 2024 00:59:07 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:59:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:59:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 02 May 2024 00:59:08 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 02 May 2024 00:59:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:59:08 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:59:08 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 02 May 2024 00:59:08 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc08d610d2fa548b2b67f737eb36eb283b7a2036afd9bd8d675db8705ba5514`  
		Last Modified: Thu, 02 May 2024 01:06:58 GMT  
		Size: 6.3 MB (6294092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60ba1b6ccd1ce3f3ff96e2a41cfc090d97f782b61218cc775301c8c4b4d99f`  
		Last Modified: Thu, 02 May 2024 01:06:55 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f10bb3daeb5a6b113a8214c83805f64efabc07aca5743e14fe8837b6988cdc`  
		Last Modified: Thu, 02 May 2024 01:06:55 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1347e5c62c081c8cd54911af7fd643da1463ff4b65e6b13485ecc6f7bdd12a09`  
		Last Modified: Thu, 02 May 2024 01:07:39 GMT  
		Size: 394.1 MB (394062349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cc9db2b286e5a9540143ac7b3eca23ca07bf5eecd386b37e1c76f768e5ef7c`  
		Last Modified: Thu, 02 May 2024 01:06:55 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058b92e31e463d1a4b138ea5f407f2757a78fcacb3d6d26c06b938cd7f1396d2`  
		Last Modified: Thu, 02 May 2024 01:06:55 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8633306ca2854151ccb05471c0b7c2c209241dd568b380ce1f3631cd55397c0`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14958626f7ccbe1614865656aaaf5ecccf87a473969285ef1aea1f2d0a383e2`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910a83ab8115602a23df858681e3f0021dbcbb2f014556b9de04f8d21369508c`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec969ed0b52b873d757f261655524f971a4e7e5c17738a867d85886d44be9ad`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 129.5 KB (129508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec4b5adc5b2aa8268ac9bdc8bea5ea45ceb745e97f93fe7803e735089fe3fd3`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
