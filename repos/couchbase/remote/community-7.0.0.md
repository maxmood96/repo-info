## `couchbase:community-7.0.0`

```console
$ docker pull couchbase@sha256:24dc913dbba2eaf1690a468e7d0b0ddbf58e6fecaf9a5fbce3105c42b2112ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.0` - linux; amd64

```console
$ docker pull couchbase@sha256:82f8c9aec3bc79261e8b1e8a29ab23d65bee96d90bf6b6eb2a66d8fa01a4dfe3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.2 MB (422209641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2307dcd4725718311d23366366eda963f9751ee2e048a95b5b8a523dd314243b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:17:15 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 31 Aug 2021 03:17:35 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 31 Aug 2021 03:17:36 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Tue, 31 Aug 2021 03:17:36 GMT
ARG CB_VERSION=7.0.0
# Tue, 31 Aug 2021 03:17:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0
# Tue, 31 Aug 2021 03:19:11 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.0-ubuntu20.04_amd64.deb
# Tue, 31 Aug 2021 03:19:11 GMT
ARG CB_SHA256=dd70ca6e45fa40aff5b168aef89509f97eaad5dc2c74c9df7966d28bdc56d917
# Tue, 31 Aug 2021 03:19:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 31 Aug 2021 03:19:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0 CB_SHA256=dd70ca6e45fa40aff5b168aef89509f97eaad5dc2c74c9df7966d28bdc56d917 CB_VERSION=7.0.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 31 Aug 2021 03:19:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0 CB_SHA256=dd70ca6e45fa40aff5b168aef89509f97eaad5dc2c74c9df7966d28bdc56d917 CB_VERSION=7.0.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 31 Aug 2021 03:20:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0 CB_SHA256=dd70ca6e45fa40aff5b168aef89509f97eaad5dc2c74c9df7966d28bdc56d917 CB_VERSION=7.0.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 31 Aug 2021 03:20:00 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 31 Aug 2021 03:20:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0 CB_SHA256=dd70ca6e45fa40aff5b168aef89509f97eaad5dc2c74c9df7966d28bdc56d917 CB_VERSION=7.0.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 31 Aug 2021 03:20:01 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 31 Aug 2021 03:20:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0 CB_SHA256=dd70ca6e45fa40aff5b168aef89509f97eaad5dc2c74c9df7966d28bdc56d917 CB_VERSION=7.0.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 31 Aug 2021 03:20:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0 CB_SHA256=dd70ca6e45fa40aff5b168aef89509f97eaad5dc2c74c9df7966d28bdc56d917 CB_VERSION=7.0.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 31 Aug 2021 03:20:03 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 31 Aug 2021 03:20:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Aug 2021 03:20:04 GMT
CMD ["couchbase-server"]
# Tue, 31 Aug 2021 03:20:04 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 31 Aug 2021 03:20:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909a89f4ffc52b1bc0efc8b382b1da145d18cc3fe8aa349a8c93a0174473f38d`  
		Last Modified: Tue, 31 Aug 2021 03:25:11 GMT  
		Size: 6.3 MB (6265547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669f46faa4219d00fffdc48350b495c094272d77b1505e7438e9786ced31ff1f`  
		Last Modified: Tue, 31 Aug 2021 03:25:07 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a62b620335fce18c26fb91910b64876024ecc41ec80acd823f0ec99c34ee62`  
		Last Modified: Tue, 31 Aug 2021 03:26:36 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394dc3dd2ddac3da10e4566bb242d5e72c3d72af40a5578826f7865f852248bb`  
		Last Modified: Tue, 31 Aug 2021 03:27:21 GMT  
		Size: 387.2 MB (387243766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28361a37e918d48f8ad486cd0a8ce21f22020219380299510452dde6ce80966c`  
		Last Modified: Tue, 31 Aug 2021 03:26:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451dab312469ffb79ad34ffb6a130d67bd35141c9da160c6fa4686b79f83872b`  
		Last Modified: Tue, 31 Aug 2021 03:26:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413108ff812065b39f2dc49057904690d306509e75eeee98f70ed95a89227737`  
		Last Modified: Tue, 31 Aug 2021 03:26:33 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaddae0cd1c5d50f5eceff8c85c480ba8d15d4a7dd3f844017f15970039c0f20`  
		Last Modified: Tue, 31 Aug 2021 03:26:33 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a17b87f1fcd6c1bd8e0535f9be8fdfea565b773adbddeb3ed0a32b052f77a7`  
		Last Modified: Tue, 31 Aug 2021 03:26:33 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb855a0475602ee5716382aa1f419136c2e88a3c726244f10cb6a929ea3ec9`  
		Last Modified: Tue, 31 Aug 2021 03:26:33 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8beb3fd3a97c6ccf02668ec412da96c94181aa88fbad86e7471fb4e801158ea`  
		Last Modified: Tue, 31 Aug 2021 03:26:33 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
