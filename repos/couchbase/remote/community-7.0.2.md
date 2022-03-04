## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:d8647cc33ef20d722aa4846b20a0b9b4522938c21f983853bcb38cb7eb9cd84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:5a67921528a14ad2bf359440c7af1a3aabff9e7242f4cc637b0a0df39cc0c0b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429022348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504331a6b437867eb362445bc1d35f4c341aa5bf5f9e2c4840ca9060411b5403`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:09:12 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Mar 2022 21:11:15 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:11:16 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_VERSION=7.0.2
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Thu, 03 Mar 2022 21:11:16 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Thu, 03 Mar 2022 21:11:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Mar 2022 21:11:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Mar 2022 21:12:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Mar 2022 21:12:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Mar 2022 21:12:14 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Thu, 03 Mar 2022 21:12:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Mar 2022 21:12:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Mar 2022 21:12:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Mar 2022 21:12:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 03 Mar 2022 21:12:15 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 03 Mar 2022 21:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 21:12:16 GMT
CMD ["couchbase-server"]
# Thu, 03 Mar 2022 21:12:16 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 03 Mar 2022 21:12:16 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9228e5742f1a596a58835b57217984fb6cde7473b0f6e80fc6c369d17b79901`  
		Last Modified: Thu, 03 Mar 2022 21:21:29 GMT  
		Size: 6.3 MB (6261146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fe12d71ac6230ed642d7c1d5e132e4dfc5556bd9a170a44f4e76ea3f765cee`  
		Last Modified: Thu, 03 Mar 2022 21:21:26 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bfe17046bd421b9011d0b5ec9ab0df901abbff702ca715d11626705f8058ad`  
		Last Modified: Thu, 03 Mar 2022 21:21:25 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1800c5ceadc33d1540a2f2eb4f85f8a8cca43b03e3b32b7ce3ccf611e322de2`  
		Last Modified: Thu, 03 Mar 2022 21:22:15 GMT  
		Size: 394.1 MB (394061464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afc4a7360a5e5bf71d09f84e3c1e5133067f509a0c9c7061a0a319a5d88aae3`  
		Last Modified: Thu, 03 Mar 2022 21:21:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe943b6095d5a944e66aaf5778f6cad160c6007ce8a80a26be4fcb79c6c63d1`  
		Last Modified: Thu, 03 Mar 2022 21:21:25 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f2b70cef4100b5fa0080abc1c3483a689a9294178d08a57e48ef8222f7c1b4`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5c50463e751abf4722b32670ea320dc918d9135b7c129191a1cb8d3a907238`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1206ec5d85a9a15f8e9f3a3ccafa13b5afe2bc5ac4c289269af75df013bed8bd`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a125e514453eab7e9f445e4b7f3cd295d8c1714b91d8383ae5608fe851e618b1`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 129.5 KB (129504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c9b415de2f0faf0fa560913db895750b0c37b7e69815ba217c735746a03807`  
		Last Modified: Thu, 03 Mar 2022 21:21:23 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
