## `couchbase:enterprise-7.0.2`

```console
$ docker pull couchbase@sha256:2fc709732f2f4bdc6c1a86245b361ee3c7401c3bc00adabfb148abf76979d27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:2fe48c849de10d69ba7524a73f9e70a9e1cb7dfa68f425565082766944d8791c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.3 MB (653331709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216ca9eb95297b98b8d26bbf03a58451c63ad09eaad8436e851a5f70e6e87c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 01:56:48 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Oct 2021 01:57:08 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Oct 2021 01:57:09 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Sat, 16 Oct 2021 01:57:09 GMT
ARG CB_VERSION=7.0.2
# Sat, 16 Oct 2021 01:57:09 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Sat, 16 Oct 2021 01:57:09 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.2-ubuntu20.04_amd64.deb
# Sat, 16 Oct 2021 01:57:10 GMT
ARG CB_SHA256=208fa1e4bf89e34f0f83abbd75cd720a18dd2de490b0154b42baaed690c36d15
# Sat, 16 Oct 2021 01:57:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Oct 2021 01:57:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=208fa1e4bf89e34f0f83abbd75cd720a18dd2de490b0154b42baaed690c36d15 CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Oct 2021 01:58:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=208fa1e4bf89e34f0f83abbd75cd720a18dd2de490b0154b42baaed690c36d15 CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Oct 2021 01:58:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=208fa1e4bf89e34f0f83abbd75cd720a18dd2de490b0154b42baaed690c36d15 CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Oct 2021 01:58:19 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Sat, 16 Oct 2021 01:58:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=208fa1e4bf89e34f0f83abbd75cd720a18dd2de490b0154b42baaed690c36d15 CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Oct 2021 01:58:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Oct 2021 01:58:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=208fa1e4bf89e34f0f83abbd75cd720a18dd2de490b0154b42baaed690c36d15 CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Oct 2021 01:58:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=208fa1e4bf89e34f0f83abbd75cd720a18dd2de490b0154b42baaed690c36d15 CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Sat, 16 Oct 2021 01:58:21 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Sat, 16 Oct 2021 01:58:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Oct 2021 01:58:22 GMT
CMD ["couchbase-server"]
# Sat, 16 Oct 2021 01:58:22 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Sat, 16 Oct 2021 01:58:22 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70e0b832017c5b057450b3c05d02cd15d9687606589e0446fa6329ae65e7f32`  
		Last Modified: Sat, 16 Oct 2021 02:00:56 GMT  
		Size: 6.3 MB (6265546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6682df4a3ff50d93156aa026b6e11d7d533b0cbdf3ca9603a87c4d00d3b6041b`  
		Last Modified: Sat, 16 Oct 2021 02:00:53 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2a3c062e7977ae347b40db2066007c9a2ebb731329abe4d9f63fcafe822aaa`  
		Last Modified: Sat, 16 Oct 2021 02:00:53 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d227b8ccd9660fd86f09de4a697986c21dfacb8dfba61482d31bad10fc5c3e`  
		Last Modified: Sat, 16 Oct 2021 02:01:57 GMT  
		Size: 618.4 MB (618365071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa3dcb30482ffb8cf9d1d092e7fe631bbaf5381a88ac7fe4cda73dcce93ee5d`  
		Last Modified: Sat, 16 Oct 2021 02:00:53 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27d4a21495e26723b85e17fc581ca7168601ca38ed832d96b7459ff00d9f6c2`  
		Last Modified: Sat, 16 Oct 2021 02:00:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76207773f82f8e10c4592f1398bd9ee82cfe324cda83621df03e2ac386524d1f`  
		Last Modified: Sat, 16 Oct 2021 02:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c0c761dd43c0ef50bf97ba335dd43aa7d487b5fe12e833575b01a5bb12034c`  
		Last Modified: Sat, 16 Oct 2021 02:00:50 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a909fc7a0618b163612013754523441ae7a66ba7e9b0073a9f2a4e6adb41d1`  
		Last Modified: Sat, 16 Oct 2021 02:00:51 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9db8c6b29ee69707a9ead70548077f40f295ca50233b18f488d26173926b1d4`  
		Last Modified: Sat, 16 Oct 2021 02:00:50 GMT  
		Size: 129.5 KB (129508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cefb3bbcb1b9b7871cef05161e468c665f655ec30e4e304d459ccf70057d0de`  
		Last Modified: Sat, 16 Oct 2021 02:00:50 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
