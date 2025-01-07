## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:19698d38ea39a37df127b8aedc8a0a636e6b70d05dac2ff8ae8bd7eb23367bfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:a7f57dfc5af064429d924a9923c182bc8c6daa741a35a30802e10287e8ce0b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.8 MB (427793634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d0199cea5f0542b1193febe89a7d0c75b8043dcaf5420b6f999ced324627a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_VERSION=7.0.2
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: CB_VERSION=7.0.2 CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11211/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa34ea4c5838f19cbd98dae13bb1ebf7424ae31d4fa4590d50d99044d50eb0c`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 6.3 MB (6309006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4be9e11bfb8db841d9da9272d474f86cb7873ab22aecab7fd69ee3d215ea89`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c5a92dde3ee759527e7abefba8c3c9f1a47617e86c2e6130f7faf8daa4f154`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a774f6cc61f43318b53b9150c419589ee1c26097cf86a669c99d6866658bbe`  
		Last Modified: Tue, 12 Nov 2024 00:57:29 GMT  
		Size: 393.8 MB (393839665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5338fd01715c169985f29512ae5aebf54a7c5646c559613d8be8d23a23d3370`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7704e91a72f65a6a7811eb71b9fd0e8285024c4e2996765e2ec0e53410134e`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db5118e35dcc31edb5b6005cd82524262d31733011db37b8ff8f1012475e5cf`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24303daae360530b91f217860cad9c71d4659594cdb57ec284e6655f83f26027`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8b8c0fed36ec953e86d42dfdd4ab28be5810066256b2d7d1215a4dda91d07c`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3111960e4b3acbcd9dd9c2cbd2cd905af8ccdf7850d1a6561c778c4cd46585`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 129.5 KB (129508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5937e8f6cb192665e2d8e41ccfdc2e382c4d2f3b85820bed0dd7d32b547e58`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.0.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:59a9821fe624b203e75f9940728016efbe6735a0725ba74f8cffa686eb05a92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d856f7f5bc88b5ed4ae470f8d3f1ed0afb40ef7a362630c3e3207dee920bfa28`

```dockerfile
```

-	Layers:
	-	`sha256:3c5c87f748204cec1ed6a552e05685bab995305b0be8422bc5b2f74f4942f90b`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 31.2 KB (31249 bytes)  
		MIME: application/vnd.in-toto+json
