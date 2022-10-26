## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:705f8b4fd8bb78889a4cd5cd73027be4dfa402d8a714cfa75b8b7005e0fe6ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:20bb824c58e04a15c4421018c33868b3866eed1c5b71109da41a856bc56474d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429014401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9245cd1ff86d8eedef80b3678caf936dfbcfc209ad0ac7eeeec905683aaa8da1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 15:57:13 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 25 Oct 2022 16:01:37 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 16:01:38 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Tue, 25 Oct 2022 16:01:38 GMT
ARG CB_VERSION=7.0.2
# Tue, 25 Oct 2022 16:01:38 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Tue, 25 Oct 2022 16:01:38 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Tue, 25 Oct 2022 16:01:38 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Tue, 25 Oct 2022 16:01:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 25 Oct 2022 16:01:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 25 Oct 2022 16:02:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 25 Oct 2022 16:02:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 25 Oct 2022 16:02:36 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Tue, 25 Oct 2022 16:02:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 25 Oct 2022 16:02:37 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 25 Oct 2022 16:02:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 25 Oct 2022 16:02:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 25 Oct 2022 16:02:38 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 25 Oct 2022 16:02:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Oct 2022 16:02:39 GMT
CMD ["couchbase-server"]
# Tue, 25 Oct 2022 16:02:39 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 25 Oct 2022 16:02:39 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260043c1f6d550342dd558fcf44e0452abe6fbc8e030bd4bb42434c32892e571`  
		Last Modified: Wed, 26 Oct 2022 16:52:30 GMT  
		Size: 6.2 MB (6240663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20cde8cc04b348935ea5ffca8a690125997fb95b5cb589e8d4aa179f549da7d`  
		Last Modified: Wed, 26 Oct 2022 16:52:26 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c82ed7e97be556f43c1ca2203cadbe20a74f122e214c3569299cbec4ad7365`  
		Last Modified: Wed, 26 Oct 2022 16:52:26 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d6c4aa97154d9013d4ee5dd733f7aa3aa4a004d1249431bb100ef8b92a376f`  
		Last Modified: Wed, 26 Oct 2022 16:53:18 GMT  
		Size: 394.1 MB (394061910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3320b5fbf7b91d4690a4a731e2fd9733f8d69ca29e8c9027f57cc6c88a659f8`  
		Last Modified: Wed, 26 Oct 2022 16:52:26 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1732b116b68ffa1901d8fa4e25de43b2ca288b0adb11114ae55c8a42b17b0b26`  
		Last Modified: Wed, 26 Oct 2022 16:52:26 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46631f1028230bdc430da975d107aee2ed89867de29a5dd7da6b79e7ebc8539`  
		Last Modified: Wed, 26 Oct 2022 16:52:24 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d793078e149b90206bb1c56d264d02e8f81b600529b7bf92517137c65c1af08`  
		Last Modified: Wed, 26 Oct 2022 16:52:24 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be6609dc7412aa680fff8495e8c7dd4a95cf01a5a14d96a7990e8abe5d06e61`  
		Last Modified: Wed, 26 Oct 2022 16:52:24 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7036c1395a4bf1ed34494aeaf1b752607c301c641159e29938b846ed50e1239c`  
		Last Modified: Wed, 26 Oct 2022 16:52:24 GMT  
		Size: 129.5 KB (129509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c4f4b7e4cb23f455369c6f44dfba10cf2576144b15396dd6ccf21f5bf18904`  
		Last Modified: Wed, 26 Oct 2022 16:52:24 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
