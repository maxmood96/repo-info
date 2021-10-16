## `couchbase:enterprise-6.6.3`

```console
$ docker pull couchbase@sha256:98e01e3fb3a8c41138b87062e53242f3f1a86ec61ce96b23559a4f7b72b0d976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.6.3` - linux; amd64

```console
$ docker pull couchbase@sha256:72ba434dd2c55d710eb3c38d4786f23e22493ee30fd01fd4940194a56c0cdd69
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.3 MB (537349495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3497b7413bd3c9f3d0760b17a5631fc473909b83a32ee873ee0fede1a998d0d`
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
# Sat, 16 Oct 2021 01:59:23 GMT
ARG CB_VERSION=6.6.3
# Sat, 16 Oct 2021 01:59:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3
# Sat, 16 Oct 2021 01:59:24 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb
# Sat, 16 Oct 2021 01:59:24 GMT
ARG CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa
# Sat, 16 Oct 2021 01:59:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Oct 2021 01:59:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Oct 2021 02:00:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Oct 2021 02:00:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Oct 2021 02:00:24 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Sat, 16 Oct 2021 02:00:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Oct 2021 02:00:25 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Oct 2021 02:00:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Oct 2021 02:00:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Sat, 16 Oct 2021 02:00:27 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Sat, 16 Oct 2021 02:00:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Oct 2021 02:00:27 GMT
CMD ["couchbase-server"]
# Sat, 16 Oct 2021 02:00:27 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Sat, 16 Oct 2021 02:00:28 GMT
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
	-	`sha256:5fddf7d67ecd8bc17302aed131a091465a84c1e17a7845f6824d36fe6831292f`  
		Last Modified: Sat, 16 Oct 2021 02:03:15 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d1d13b86062bbb9cacdb2719279541c4ffa937d89f8ec2cb34d9fa14bca7a`  
		Last Modified: Sat, 16 Oct 2021 02:04:06 GMT  
		Size: 502.4 MB (502386595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713dbd383edefea8d818defdd0877b30ae44f83ab3970ed2914cbf4552644c46`  
		Last Modified: Sat, 16 Oct 2021 02:03:15 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fee58859be3f6c3a77bb3cafb737f2efd2a2e8b9785918631d2c27ddf367eb7`  
		Last Modified: Sat, 16 Oct 2021 02:03:15 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c145dfdc6f63e62948524e86c28fed88d3a1eabb763f44a18c573b04e619378c`  
		Last Modified: Sat, 16 Oct 2021 02:03:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30132cef8bee532371d0a9c2460b6f82db3ca982ddb169eadbac2c1b82fb7d80`  
		Last Modified: Sat, 16 Oct 2021 02:03:13 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdb29e3f9b0644e865de5f54261af2941ae34b800b3d94ac74492ff3ae10c51`  
		Last Modified: Sat, 16 Oct 2021 02:03:13 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d87776234f303739d13bc8426c91864c0bbdf67d0172a83756f56761347a1a`  
		Last Modified: Sat, 16 Oct 2021 02:03:13 GMT  
		Size: 125.9 KB (125888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fca1ccf1ccfdf0424935532303e3f93b6cb2629d97c82eefdab2920153e57cd`  
		Last Modified: Sat, 16 Oct 2021 02:03:13 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
