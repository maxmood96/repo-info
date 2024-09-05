## `emqx:latest`

```console
$ docker pull emqx@sha256:ff45a44441aefe8182dff4ac38ef5cef17023e819c93aac152ef42a0108e7ea9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:64fc0137c0b82a10d6306a3e1172b8494f76eaad1227035ff720f8d7d034b5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125472620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789494dd19c3636699f005cba56d887d582564913e12453e79a7b63c3ebd19c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sun, 01 Sep 2024 07:35:29 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Sun, 01 Sep 2024 07:35:29 GMT
CMD ["bash"]
# Sun, 01 Sep 2024 07:35:29 GMT
ENV EMQX_VERSION=5.8.0
# Sun, 01 Sep 2024 07:35:29 GMT
ENV AMD64_SHA256=95a8b8d0e51b2f9d0c7eab768aeb51e7e01ed290cd61a0a97092c2bb38815d58
# Sun, 01 Sep 2024 07:35:29 GMT
ENV ARM64_SHA256=13e8614b3376e06da72079ab1845e7213226c47c2ae3e805fd29c25f8041f81d
# Sun, 01 Sep 2024 07:35:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sun, 01 Sep 2024 07:35:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sun, 01 Sep 2024 07:35:29 GMT
WORKDIR /opt/emqx
# Sun, 01 Sep 2024 07:35:29 GMT
USER emqx
# Sun, 01 Sep 2024 07:35:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sun, 01 Sep 2024 07:35:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sun, 01 Sep 2024 07:35:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sun, 01 Sep 2024 07:35:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sun, 01 Sep 2024 07:35:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483053bb0099f82b6d284f619f08a77edfd10931355b1509393d7cc6c8d3c583`  
		Last Modified: Wed, 04 Sep 2024 23:09:56 GMT  
		Size: 96.3 MB (96345073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b531d1868cd2599f3a9e22ebe59cb8b2a7a8cc0e0d209ff7323e0f5b1d00bb7`  
		Last Modified: Wed, 04 Sep 2024 23:09:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:a7fc3e4aeb2db96db0beec407b077acfd1f3bf8d4bb5b3786b890758e2e87464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1f64003fcb393c3953fa2f4317a20de419cddc4bd4ed3dce0cfa437f4be6c6`

```dockerfile
```

-	Layers:
	-	`sha256:99091625c0cc66004e4d41e98a297e981e277386a0a2d741b4c09eeeb387a904`  
		Last Modified: Wed, 04 Sep 2024 23:09:55 GMT  
		Size: 2.6 MB (2598835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50e297afe7cf5c2a139c709b6a26096df2dd2841cac31104d70ea3d4e1b11d7`  
		Last Modified: Wed, 04 Sep 2024 23:09:55 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0912b26f91b364d0a1fd0439fe4a657028b3890f12fe9548ef0cbd5ee1a43750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122067568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01abb61e9dec1394def93682d29d8224dbe827518d405d59e23495119d9169cd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Sun, 01 Sep 2024 07:35:29 GMT
ENV EMQX_VERSION=5.8.0
# Sun, 01 Sep 2024 07:35:29 GMT
ENV AMD64_SHA256=95a8b8d0e51b2f9d0c7eab768aeb51e7e01ed290cd61a0a97092c2bb38815d58
# Sun, 01 Sep 2024 07:35:29 GMT
ENV ARM64_SHA256=13e8614b3376e06da72079ab1845e7213226c47c2ae3e805fd29c25f8041f81d
# Sun, 01 Sep 2024 07:35:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sun, 01 Sep 2024 07:35:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sun, 01 Sep 2024 07:35:29 GMT
WORKDIR /opt/emqx
# Sun, 01 Sep 2024 07:35:29 GMT
USER emqx
# Sun, 01 Sep 2024 07:35:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sun, 01 Sep 2024 07:35:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sun, 01 Sep 2024 07:35:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sun, 01 Sep 2024 07:35:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sun, 01 Sep 2024 07:35:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08927a54060d9c5a4e9c2143d956e04ea5ec66c568e5909dfb0790d266c7fdf2`  
		Last Modified: Tue, 03 Sep 2024 18:57:23 GMT  
		Size: 92.9 MB (92909974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e94e28f2722a81dd2fc974ed708e57de28b2448fba59b310b412f2aa4c3b35e`  
		Last Modified: Tue, 03 Sep 2024 18:57:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:791ff43d3cf154b2040ef603988e8d8ac4b137ab6c5418cb44fa246fde2f7041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ec63521e4ec6ccf6805d9330324ccf109ed3b5fe0d6663697934d2c78c664e`

```dockerfile
```

-	Layers:
	-	`sha256:bcda3960241500dc5ead1baccc7fb5751ca57871074a6e84f41d26613e541ecf`  
		Last Modified: Tue, 03 Sep 2024 18:57:21 GMT  
		Size: 2.6 MB (2599114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad0a007fd4dfb3585daf61cebfc6d16f026a4602dbd0a70404edbb3c46c7e7c`  
		Last Modified: Tue, 03 Sep 2024 18:57:20 GMT  
		Size: 12.6 KB (12608 bytes)  
		MIME: application/vnd.in-toto+json
