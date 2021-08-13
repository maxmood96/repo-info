## `couchbase:enterprise-6.6.3`

```console
$ docker pull couchbase@sha256:bc3416f7704622501b4472c5021df57ebb978955a0d5d546083724d7ca3c41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.6.3` - linux; amd64

```console
$ docker pull couchbase@sha256:fccb7527080e247c7353e1c488dbfca6bb7a9f47156712f5958d20dab402e99d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.4 MB (537356336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0175aadfa21dbee0affaa456fd5bcd1e5f9eaace16458995abe3207c252fcbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:17:12 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 26 Jul 2021 22:20:33 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 26 Jul 2021 22:20:33 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 12 Aug 2021 23:19:43 GMT
ARG CB_VERSION=6.6.3
# Thu, 12 Aug 2021 23:19:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3
# Thu, 12 Aug 2021 23:19:44 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb
# Thu, 12 Aug 2021 23:19:44 GMT
ARG CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa
# Thu, 12 Aug 2021 23:19:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Aug 2021 23:19:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 12 Aug 2021 23:20:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Aug 2021 23:20:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 12 Aug 2021 23:20:51 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 12 Aug 2021 23:20:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 12 Aug 2021 23:20:52 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 12 Aug 2021 23:20:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 12 Aug 2021 23:20:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.3 CB_SHA256=8d62db9365171aba0ee646c0189b81dec8ef9718fac7b44bd72e15da4e2b38fa CB_VERSION=6.6.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 12 Aug 2021 23:20:54 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 12 Aug 2021 23:20:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Aug 2021 23:20:54 GMT
CMD ["couchbase-server"]
# Thu, 12 Aug 2021 23:20:55 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 12 Aug 2021 23:20:55 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d887c602d6e2b416c36a7344e07f41278a46971fa08be0eeb2fc78a75d7013b`  
		Last Modified: Mon, 26 Jul 2021 22:39:49 GMT  
		Size: 6.3 MB (6272568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b219d16ecda3370190c17757e31f650c0b2db8a483364cebc0add69c976f1fa`  
		Last Modified: Mon, 26 Jul 2021 22:39:45 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d45cc046e3f9f2bb2c8fd4b91cc9d3ed68b627a240bb0e621ae9f58b0959b7`  
		Last Modified: Thu, 12 Aug 2021 23:21:33 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac86a4d3b34fccecb16f3f75e2a94e1afdfdf20aa49fc9a058bfbcddf75a1c9`  
		Last Modified: Thu, 12 Aug 2021 23:22:24 GMT  
		Size: 502.4 MB (502385552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef9cd3ed9cda9d89dd454b3186650996c8a52a314a82860d0d99a52edfd0076`  
		Last Modified: Thu, 12 Aug 2021 23:21:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1c2e5e740ac45f1107805174926bf940431443fb9575f593314520599e6f4c`  
		Last Modified: Thu, 12 Aug 2021 23:21:33 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4e70b2044b9f9feb0f57c3402e02fdbd001f888242b0ea6c012eb7ef5959cd`  
		Last Modified: Thu, 12 Aug 2021 23:21:31 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d653e0801ec115d089700f04f189f558954f70e7b4b4829abb610134215c282`  
		Last Modified: Thu, 12 Aug 2021 23:21:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21de956e803bd767454a5f46d1978b2a2c2de88409fc19032278fce7b95128b2`  
		Last Modified: Thu, 12 Aug 2021 23:21:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3445a787279de970b1f8a3d890c9e6edfc88d394af7b3774e7f4ee5ba7eea`  
		Last Modified: Thu, 12 Aug 2021 23:21:31 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a48e2a2ca8c59dc47a945e01983795c07e40bbb9fd9b9de290cfd5f40f3bb8f`  
		Last Modified: Thu, 12 Aug 2021 23:21:31 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
