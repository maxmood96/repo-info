## `emqx:latest`

```console
$ docker pull emqx@sha256:e61fac59b31a5f27f6a8701a179384bff775a74246ec77b52b26ea54ff804f47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:bcf835a6854ff358b666ef02392bf6bf07ab2c96a4114ec07dc0ab1a8c7feb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108401152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776f8193252a6e48334cbbb55d6f629110548b96c931cae13b0525ab8b893376`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:20 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 07 Apr 2026 01:17:20 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 07 Apr 2026 01:17:20 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 07 Apr 2026 01:17:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:17:20 GMT
WORKDIR /opt/emqx
# Tue, 07 Apr 2026 01:17:20 GMT
USER emqx
# Tue, 07 Apr 2026 01:17:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Apr 2026 01:17:20 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Apr 2026 01:17:20 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Apr 2026 01:17:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:17:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665d66b4e0950915a818fea2f650179952b32339b806774fefa1a1a741e9e6d4`  
		Last Modified: Tue, 07 Apr 2026 01:17:36 GMT  
		Size: 78.6 MB (78624450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e99607e6df79f2c06b355584ad2f6b2e60d8500db6f2c4ed41719749b7632fd`  
		Last Modified: Tue, 07 Apr 2026 01:17:33 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:8f8cc49eff4cd54cafd93cb8f5f6dc3ce085bb99402b3f34a37b34b4922ba4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4e03000c6a381a20c32159d06c8e3909d2118440cf6ed05373af7e9ad295f6`

```dockerfile
```

-	Layers:
	-	`sha256:844895cb2d481b4bc408c87d60819d39b7f6fb3ae8b465b7e88c574748d83561`  
		Last Modified: Tue, 07 Apr 2026 01:17:34 GMT  
		Size: 2.4 MB (2403501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7fde17a987822d35a3e2627ed64bb6ba1399085ffd189d4aa9b226122f970b`  
		Last Modified: Tue, 07 Apr 2026 01:17:33 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:14149700fc323e4470fcf19243f9e0e77990a94ab2ecb1c61aaa845d8d2e53a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106671113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0797b70d00187c5037876486956781972a8c1852430016ef7c5f862020af7f58`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:14 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 07 Apr 2026 01:16:14 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 07 Apr 2026 01:16:14 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 07 Apr 2026 01:16:14 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Apr 2026 01:16:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:16:14 GMT
WORKDIR /opt/emqx
# Tue, 07 Apr 2026 01:16:14 GMT
USER emqx
# Tue, 07 Apr 2026 01:16:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Apr 2026 01:16:14 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Apr 2026 01:16:14 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Apr 2026 01:16:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:16:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfc96eef1daded895e5e0404338dcdc58f7e58e2bee5a0af2334266cc344929`  
		Last Modified: Tue, 07 Apr 2026 01:16:29 GMT  
		Size: 76.5 MB (76531498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5daf44279b7a403b29a37f7a1546df7ca8f6e815303e9fca98b31e66bc6509`  
		Last Modified: Tue, 07 Apr 2026 01:16:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:cd346736faa971f35b68435c847c54a73ecc3833f8da5c755ed752ad67cf7612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d66130ecb0f5989afcd66868068aacd1a4440b6af2e73a8a42e35e7fb61f14`

```dockerfile
```

-	Layers:
	-	`sha256:b0848a222fc252e8db8de531e4e910ac64506847430e32669b92730b367e5a89`  
		Last Modified: Tue, 07 Apr 2026 01:16:28 GMT  
		Size: 2.4 MB (2403790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f4ab95d77db79d2ea10268ca3562a89e13b51f9325650a0cfa218f5ff9a9fb`  
		Last Modified: Tue, 07 Apr 2026 01:16:27 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json
