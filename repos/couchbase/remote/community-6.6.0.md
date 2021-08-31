## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:112625dc0a52fa767d10da4f16effd2d5f5b4d708f30c16c98653a679bb2a289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:4a29885ce6566911255f7873f72b72d7e927937f9e8556245ae1936f95f19379
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354223993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76067ef181e26819518d66f7cd289b9a01efe1eb65888c27af69579d62958401`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:21:37 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 31 Aug 2021 03:22:14 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 31 Aug 2021 03:22:15 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Tue, 31 Aug 2021 03:22:15 GMT
ARG CB_VERSION=6.6.0
# Tue, 31 Aug 2021 03:22:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Tue, 31 Aug 2021 03:22:15 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb
# Tue, 31 Aug 2021 03:22:16 GMT
ARG CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559
# Tue, 31 Aug 2021 03:22:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 31 Aug 2021 03:22:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 31 Aug 2021 03:22:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 31 Aug 2021 03:22:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 31 Aug 2021 03:22:58 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 31 Aug 2021 03:22:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 31 Aug 2021 03:22:59 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 31 Aug 2021 03:23:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 31 Aug 2021 03:23:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 31 Aug 2021 03:23:01 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 31 Aug 2021 03:23:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 31 Aug 2021 03:23:01 GMT
CMD ["couchbase-server"]
# Tue, 31 Aug 2021 03:23:01 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 31 Aug 2021 03:23:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3568fede45a221460d4a4be77ba26e77c9a46473d2222007231a9f5330db05`  
		Last Modified: Tue, 31 Aug 2021 03:28:43 GMT  
		Size: 7.4 MB (7374412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eddc4afd6c8ea74be3ea5e5c50a92e5e456155244fd5b8fdbdae4abe2c97a81`  
		Last Modified: Tue, 31 Aug 2021 03:28:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a85f24a8056215e10d418f76f9428580c631214c82bf7d4f237878f81f675b`  
		Last Modified: Tue, 31 Aug 2021 03:28:38 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac496a4ccf145399a0a38180bac726557511e5accef8255097a14ceb3757a88`  
		Last Modified: Tue, 31 Aug 2021 03:29:13 GMT  
		Size: 320.0 MB (320018397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2993d6fb012e37b05cf3d7b4dd419c81a82cb2ac7f8635e2f35f926e232bcfa7`  
		Last Modified: Tue, 31 Aug 2021 03:28:38 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b103b7b10eb12fcb40076fa5162dffe889a3d586d7668c5cbc315f0e85b2bf0`  
		Last Modified: Tue, 31 Aug 2021 03:28:38 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf4a08383691b8f2a5828e046b9a9298c89db8bfdedc3993ce98826d150664f`  
		Last Modified: Tue, 31 Aug 2021 03:28:36 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85577528d682fceacf82afe1541b01f48ddb62a8219597b0f1f02df5d6801f62`  
		Last Modified: Tue, 31 Aug 2021 03:28:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1719b2f11828da91c747313998f3b6fa7d498a475fe253573e2f2f70228c1514`  
		Last Modified: Tue, 31 Aug 2021 03:28:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4b004d16ca85372456965c136f7134b941a69864ff38e38792396388bbb1c9`  
		Last Modified: Tue, 31 Aug 2021 03:28:36 GMT  
		Size: 118.2 KB (118188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb030634e3e27c0fdefa4d91cfa31fe7cdc010d7d48cfd0cde728283bdd0d79`  
		Last Modified: Tue, 31 Aug 2021 03:28:36 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
