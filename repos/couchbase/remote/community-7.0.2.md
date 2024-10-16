## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:814cc6c20fc7077fc2daed765328603e284e2040ffc1de39fb26170edad877f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:cf42529151fed79c1039823c33c5979483d9684249093757ff891cc41000c538
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429091063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c607a27c1bb61745acb4ab708a5a90c464f9f8317dec98f77954fd61b66d99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:22:12 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 16 Oct 2024 02:31:09 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 02:31:09 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 16 Oct 2024 02:31:09 GMT
ARG CB_VERSION=7.0.2
# Wed, 16 Oct 2024 02:31:09 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Wed, 16 Oct 2024 02:31:10 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Wed, 16 Oct 2024 02:31:10 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Wed, 16 Oct 2024 02:31:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 16 Oct 2024 02:31:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 16 Oct 2024 02:32:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 02:32:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 16 Oct 2024 02:32:05 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Wed, 16 Oct 2024 02:32:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 16 Oct 2024 02:32:06 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 16 Oct 2024 02:32:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 16 Oct 2024 02:32:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 16 Oct 2024 02:32:07 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 16 Oct 2024 02:32:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 02:32:07 GMT
CMD ["couchbase-server"]
# Wed, 16 Oct 2024 02:32:07 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 16 Oct 2024 02:32:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe0ceab31746ca301f48f6855d85e735e311fc67cbc0edee35aad1e5243f53`  
		Last Modified: Wed, 16 Oct 2024 02:38:08 GMT  
		Size: 6.3 MB (6310569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d8610745d1d2dc58dfb7eea6f910b4525c6c223653f08792615b1e23cde35c`  
		Last Modified: Wed, 16 Oct 2024 02:38:06 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc709007a1819cb4d35077d55271487e73f394bf6a3ea580476df507821b20d`  
		Last Modified: Wed, 16 Oct 2024 02:38:06 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902b64f88415ac76c5813bf5e5f32a83169c155195459bbd66633572fd106d08`  
		Last Modified: Wed, 16 Oct 2024 02:38:49 GMT  
		Size: 394.1 MB (394062617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2350dfb96fe87440de458288d81d69b8830b5d72ea57a87ca5929c6e4bade25`  
		Last Modified: Wed, 16 Oct 2024 02:38:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f634fa5727a90a43dedb1da8b2e4f9319f6eefe8e64ffdfe1059382ff6acb38d`  
		Last Modified: Wed, 16 Oct 2024 02:38:05 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d96ec2d303ac8c3df713b426db1908b82a0ce6e85a4d8aa8ad969cf9bcbbca`  
		Last Modified: Wed, 16 Oct 2024 02:38:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f93ff30aefb54c33f4dfa29fe1d31f1e526d37e4175b659d9113f6f0061973`  
		Last Modified: Wed, 16 Oct 2024 02:38:04 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a320b28cf407dacf4604b0e1c92e12430501d33e121d886a142df30bdafa2bdf`  
		Last Modified: Wed, 16 Oct 2024 02:38:04 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44752007130eb84d5e951b816029b234cf4d9c1c9dd7a6559be654781b619938`  
		Last Modified: Wed, 16 Oct 2024 02:38:04 GMT  
		Size: 129.5 KB (129509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2a17a10d010221191b389452dc5301611812082f9ba090d56be18b9c785afd`  
		Last Modified: Wed, 16 Oct 2024 02:38:04 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
