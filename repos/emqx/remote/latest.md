## `emqx:latest`

```console
$ docker pull emqx@sha256:43a189d6ac259fb59088aa80dd4ede560f999449fba0e6be6ac49b0eafde770a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:d48e7d7e94a393457109bbf4b09aaeb2043ca013674b5ef844a43111620cf6c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101660431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2338a355d25ad1180b3e19e255b9cea689c5862c75370524b34131171cb97608`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:24:00 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:24:01 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 07 Jun 2023 22:19:30 GMT
ENV EMQX_VERSION=5.0.25
# Wed, 07 Jun 2023 22:19:31 GMT
ENV AMD64_SHA256=1e5f07430e7904cf4958381864c394916ece4d68e44e467764df9b7599da482a
# Wed, 07 Jun 2023 22:19:31 GMT
ENV ARM64_SHA256=440a9d0c01e0f75f19080663346c9fdbaf6666dd56e084bb8cca886bbc08a90a
# Wed, 07 Jun 2023 22:19:31 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 07 Jun 2023 22:19:37 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 07 Jun 2023 22:19:38 GMT
WORKDIR /opt/emqx
# Wed, 07 Jun 2023 22:19:38 GMT
USER emqx
# Wed, 07 Jun 2023 22:19:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 07 Jun 2023 22:19:38 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 07 Jun 2023 22:19:38 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 07 Jun 2023 22:19:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 07 Jun 2023 22:19:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ce7ad79b255e788cff6cef738579e0bbf7797cb46293052c0dac256ec5cce9`  
		Last Modified: Tue, 23 May 2023 08:24:36 GMT  
		Size: 3.0 MB (2987806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7beaac16821c81034b9f18e03825f60acf03fbd723d44a9650179d3059bc25`  
		Last Modified: Tue, 23 May 2023 08:24:35 GMT  
		Size: 4.1 KB (4119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a314f5352e77c6991d74ad4d9dc9f7cda87c3efd7ba2b2f3e399dedf8e8c2dcd`  
		Last Modified: Wed, 07 Jun 2023 22:19:55 GMT  
		Size: 67.3 MB (67264018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ad9aab3b03844bc4800000e1b2f9f307e5fc135c63f61d1f56e85cd800413`  
		Last Modified: Wed, 07 Jun 2023 22:19:47 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d2280568596878bf05989dc6e47a6a66f7c03f0af29c69413848f6bcbd31a19d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92743008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f62ecb15c5d4c5c1d660366e3163ef3d3277da690371cd15e8152ec106916d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:42:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:42:43 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 07 Jun 2023 21:58:33 GMT
ENV EMQX_VERSION=5.0.25
# Wed, 07 Jun 2023 21:58:33 GMT
ENV AMD64_SHA256=1e5f07430e7904cf4958381864c394916ece4d68e44e467764df9b7599da482a
# Wed, 07 Jun 2023 21:58:33 GMT
ENV ARM64_SHA256=440a9d0c01e0f75f19080663346c9fdbaf6666dd56e084bb8cca886bbc08a90a
# Wed, 07 Jun 2023 21:58:33 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 07 Jun 2023 21:58:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 07 Jun 2023 21:58:39 GMT
WORKDIR /opt/emqx
# Wed, 07 Jun 2023 21:58:39 GMT
USER emqx
# Wed, 07 Jun 2023 21:58:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 07 Jun 2023 21:58:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 07 Jun 2023 21:58:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 07 Jun 2023 21:58:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 07 Jun 2023 21:58:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8345ceedc06f3b0ae12a8eb9f0f0e7dd52b3ae9800880811d86f7c26b0651446`  
		Last Modified: Tue, 23 May 2023 01:43:12 GMT  
		Size: 3.0 MB (3002990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b78e6c4890d65e6f6f17dbd7faa9d396eaad9d65dd2bbeb2e49aee524b18b1e`  
		Last Modified: Tue, 23 May 2023 01:43:11 GMT  
		Size: 4.1 KB (4115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc4af526687cfb27ecf464e364098ed7cf677a79ca6799cdc43b355b38b1ee0`  
		Last Modified: Wed, 07 Jun 2023 21:58:56 GMT  
		Size: 59.7 MB (59682254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47abf02f75b6cbe972b25c8e2ecec6a82796788014fd9aba265fd2bb2855e606`  
		Last Modified: Wed, 07 Jun 2023 21:58:51 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
