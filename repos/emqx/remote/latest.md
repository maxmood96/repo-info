## `emqx:latest`

```console
$ docker pull emqx@sha256:a516f4bb55587f0e39afef03a084ef46e28754f122f4671b501a66b7697b0a2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:0ce1cfcf6a109e8ced850a16d6af8fcdac833cd7805c46f7e7cae38113376315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125472373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d25edbc8f220dcc94592b7ef6bd9fe7353bc7bdfde2a2cdb7f7962199fa47fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sun, 01 Sep 2024 07:35:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4cab07d9f026d2d5c94fb73c27e404342a2b95948b0775cd70961d000b232b`  
		Last Modified: Thu, 17 Oct 2024 01:17:10 GMT  
		Size: 96.3 MB (96345020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23bab9ec5c621c7307ff82caccffd3ecccf9b8323da0ace845f0a5c1f08ee74`  
		Last Modified: Thu, 17 Oct 2024 01:17:07 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:e22f02fdac42973c24bc9b381584c274a778d9193d63fbd9b9acb7d3d62acacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ec9f2966e5e0e9ce46da71d3c6b03d569bf1d6ec820f9266c2e985b76b06a7`

```dockerfile
```

-	Layers:
	-	`sha256:16886c0b3135b190cb2414d029c55c36bb3bfcf7e4bdf0dbb2d90d1b967ebb0a`  
		Last Modified: Thu, 17 Oct 2024 01:17:08 GMT  
		Size: 2.6 MB (2598848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69995216b224fb6c62d943f7cfc0bccdf68db653370433565163dddfc141e69d`  
		Last Modified: Thu, 17 Oct 2024 01:17:07 GMT  
		Size: 12.3 KB (12343 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b165e5d88fcdebb8742a5aadc83816811968f56832da748d655ac9d886196906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122067423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2f63e43d4b2e7f08e754b1c8783f23c5faf8dd288b5a1d6d96e1f9dd6cc133`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sun, 01 Sep 2024 07:35:29 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dfb3cc8fefc738acb0c1f351d64e56c1eef605e9284498213db726856aeb33`  
		Last Modified: Fri, 27 Sep 2024 11:22:39 GMT  
		Size: 92.9 MB (92909992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7a532b0135aee635943dd14f80428243e14b700f43e50569b065a136875f96`  
		Last Modified: Fri, 27 Sep 2024 11:22:36 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:081fd6b1f10127ae20a8528c6041709e01afce0f715c20e63fedbf38b976fad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c752042b5cda683ceddeac2d2fdd4b5dc87de4bf417c19fbd8fc65183b998a`

```dockerfile
```

-	Layers:
	-	`sha256:cae49897e6fc74e139f4f5341d625ee04dcada3f4cbc3aa2d56a1f04f392046c`  
		Last Modified: Fri, 27 Sep 2024 11:22:36 GMT  
		Size: 2.6 MB (2599127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20cf5a72a7e4ffc9bc0645b95fd304f16941fac8b9771282e2f2117d2555ef2f`  
		Last Modified: Fri, 27 Sep 2024 11:22:36 GMT  
		Size: 12.6 KB (12608 bytes)  
		MIME: application/vnd.in-toto+json
