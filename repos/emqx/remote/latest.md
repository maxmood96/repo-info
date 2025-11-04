## `emqx:latest`

```console
$ docker pull emqx@sha256:78fe69db535fdc5dfee683bd6137b20c64760bacf1a99becf4b1de3e48dbace7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:de575cc9c3f2297495e7c20a6df5f8ad56f38671e67119e533f81a2d26b0bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108401110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d091c7c9e4b039f92a2f4ffaccc2d52f7e51db5807e9da98ce07fb9fd8819c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 07:56:49 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 04 Nov 2025 07:56:49 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 04 Nov 2025 07:56:49 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 04 Nov 2025 07:56:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 07:56:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 07:56:49 GMT
USER emqx
# Tue, 04 Nov 2025 07:56:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 07:56:49 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 07:56:49 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1cf32effd94989dd74a148d877a700d4243f11e8ad8569f6eca908e7487af8`  
		Last Modified: Tue, 04 Nov 2025 07:57:19 GMT  
		Size: 78.6 MB (78621941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c14e66fdf14adc2b18bbdbbd97fce5f48a058da7391ad30b29661736a0eb0`  
		Last Modified: Tue, 04 Nov 2025 07:57:09 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:6a1194f7197fd809825ed747ca84f1c67a1d6720c616e5c4a0d37571d957d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7179793449735effc426b818d5b79351953eef79b9f358fcf9c8ad2ca21c48f9`

```dockerfile
```

-	Layers:
	-	`sha256:d72c18cf09dbec93333b00842a4b4c574e709129d3f8a193c8deb1d3e2696236`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 2.4 MB (2403335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4312173f4d9534c705996a043146519da9ac5973889faa4ca2a9de23bdffe01`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6f192eb65b219b92ccb54ebb86bb287246ba5dbc65e77ead97d6205036ebf186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b364b82e944ba5ef5cc8d10559cf239f5f02af5fbf0de573394da737351ee73c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13ddf0ee5532d35175437c90898d40055da1300a6555a0db4742545f7563933`  
		Last Modified: Tue, 21 Oct 2025 01:16:58 GMT  
		Size: 76.5 MB (76530272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff8b66d54b881659f5c9f77dec25ae05e4218d016f32f57bef15de19709b51d`  
		Last Modified: Tue, 21 Oct 2025 01:16:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:39002a88ec037650c0a6a1ed52a5ce7bb446e19dabde8e07589682753b3d54b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3be2f3d329a71640a643571fa66e232303cc2cd5dddca941350f155b94b9c`

```dockerfile
```

-	Layers:
	-	`sha256:8b42980123438161a3909064137eb866a1c420bfca5778582c8495a944e47168`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 2.4 MB (2403624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a5bb2dae5298fa0cff01cb24a233fe38dec22b38a04104d654ead5eb2d17e8`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
