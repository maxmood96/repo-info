## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:53d868ad318e1ab55e56b50d17f9ac4f45e98b3d4da7442484d25b6f54c108aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:3e0be28ee2752151a55f292c712ff1e61806fb7811ae8e6dbb42ce8929e0e97b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429075289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f4ca4c87fa6c2c2e9bb4b3579e37a7a92cf343db14081ee4d597c34387e62f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Fri, 26 Apr 2024 00:17:11 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 26 Apr 2024 00:29:02 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 26 Apr 2024 00:29:03 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 26 Apr 2024 00:29:03 GMT
ARG CB_VERSION=7.0.2
# Fri, 26 Apr 2024 00:29:03 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Fri, 26 Apr 2024 00:29:03 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Fri, 26 Apr 2024 00:29:04 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Fri, 26 Apr 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 26 Apr 2024 00:29:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 26 Apr 2024 00:29:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 26 Apr 2024 00:29:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 26 Apr 2024 00:29:57 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Fri, 26 Apr 2024 00:29:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 26 Apr 2024 00:29:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 26 Apr 2024 00:29:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 26 Apr 2024 00:29:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 26 Apr 2024 00:29:59 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 26 Apr 2024 00:29:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 00:29:59 GMT
CMD ["couchbase-server"]
# Fri, 26 Apr 2024 00:29:59 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 26 Apr 2024 00:29:59 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ae28acb9492a90d218c68936768f7770f892ffa58cd20ec2b5b5325ed0472c`  
		Last Modified: Fri, 26 Apr 2024 00:37:39 GMT  
		Size: 6.3 MB (6294048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0702fe26966eda8d5c8900ce440262001e6365acfc571c64a18f9c787ccb3d9`  
		Last Modified: Fri, 26 Apr 2024 00:37:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55da50504386fb74fa25a433732acc581036d4c7e26a50f64863642317f189ac`  
		Last Modified: Fri, 26 Apr 2024 00:37:36 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6229de9b570218800e5e7667349f287c89eecbbd2b57b01a66de214987e070`  
		Last Modified: Fri, 26 Apr 2024 00:38:19 GMT  
		Size: 394.1 MB (394062645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09273cd936b55c2319af1520f76cb312a6f837586b91032d7a8d2905ddb0620d`  
		Last Modified: Fri, 26 Apr 2024 00:37:36 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da6fdf11e0cd44ba0bf4266c826eab9d8e738aea5a0cd55a60d548d687d675`  
		Last Modified: Fri, 26 Apr 2024 00:37:35 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde871b891a25eb9357775383114107af5535411b10d0a0bd8389c23b7070ea3`  
		Last Modified: Fri, 26 Apr 2024 00:37:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba0c4568bd1c3d78bf828d3932a8b98d1bdbe4a123ead9158d487e6903f940d`  
		Last Modified: Fri, 26 Apr 2024 00:37:34 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c47a7f9c718438fd1da02f6b98b2e127b89653aa81b01eec49d7fcb99a028d`  
		Last Modified: Fri, 26 Apr 2024 00:37:34 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d752bbc718ef6a28c09c9a5fe776f173e8e8c3c355a00c37cc15c82fd2e28173`  
		Last Modified: Fri, 26 Apr 2024 00:37:34 GMT  
		Size: 129.5 KB (129513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c9fd7005fd2ed998d01d8e5f02aa54d7555213aba01434927893d21a204100`  
		Last Modified: Fri, 26 Apr 2024 00:37:34 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
