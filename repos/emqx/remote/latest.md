## `emqx:latest`

```console
$ docker pull emqx@sha256:16dd883c345325dac977b9ee34eae6c9b127edfaedf48cca812756710fbe062a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:dc81bf86e75cea8614700e6e0b885516f5c63c99bfd87f3c7925d962f0703382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108395797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22500b536844edd764c39f51b3ceb17462f95aa69e4c4f62265a9677c98676b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1a1ff9b113cabdc895a89836fcf9bccee142ddb77b84d48688f44b16daf924`  
		Last Modified: Mon, 08 Sep 2025 23:27:45 GMT  
		Size: 78.6 MB (78621238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3f1c74959a48166c48ac265429a5a9098d9edde75c52044811a02be155f30`  
		Last Modified: Mon, 08 Sep 2025 21:38:43 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:a530e888a7f2e4c5b3c0914962faa512ec39041b072800620e87bc1fcb04dc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dda067b9112b8d089c0694395dd4ce9b97af2b744f2263fcc6f5375e291963`

```dockerfile
```

-	Layers:
	-	`sha256:b5322df4eb05b73e1a80d03b541e089e59f2ad411e18a4b78369588e9b659695`  
		Last Modified: Mon, 08 Sep 2025 23:27:21 GMT  
		Size: 2.4 MB (2403281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76e110315f54027111d4f2c3839fb90d62b8b45dc212744d6febace135cd3d41`  
		Last Modified: Mon, 08 Sep 2025 23:27:22 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:05ad5d82aec5910b613f08ff5cbb2a6c3fc7b81a8983536ee8c9076a53313f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106668004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78be4b96df2153e023139e2cd6197cde6a999449913aa0d3b256a33d1cf99f49`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69e148f729404ccd3971600fce1ab4c36c7c5de84ee7a2934d296c1c3c62214`  
		Last Modified: Mon, 08 Sep 2025 21:55:50 GMT  
		Size: 76.5 MB (76530310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82078162f46a804d882875b289f1f43352bad37b3db7e48c7b8371c0ca5701b`  
		Last Modified: Mon, 08 Sep 2025 21:55:39 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:1ba7a369da7cda93ecd96f43862ba22d3b875d2eb9b7f8776f85be885044f123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d71ff9e3fac080261186198492e5752a8db8bb57577cb0d97ef7657e115377`

```dockerfile
```

-	Layers:
	-	`sha256:aa7fe468d92c01e847611280f6173678986c2468db68fccda3dff81f3b9792db`  
		Last Modified: Mon, 08 Sep 2025 23:27:27 GMT  
		Size: 2.4 MB (2403570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d7e109d3bbb0846ee448e56c01391a93582f0a3f2885e769e8b940ef21e158`  
		Last Modified: Mon, 08 Sep 2025 23:27:29 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
