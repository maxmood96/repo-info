<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.8`](#emqx588)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:e61fac59b31a5f27f6a8701a179384bff775a74246ec77b52b26ea54ff804f47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

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

### `emqx:5` - unknown; unknown

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

### `emqx:5` - linux; arm64 variant v8

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

### `emqx:5` - unknown; unknown

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

## `emqx:5.7`

```console
$ docker pull emqx@sha256:db9229a537fef40054aee6979bbc1122fb5068d53ccdac900f5c567e4accf528
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:ea230cd7671b28d9ea76f87e41497c2c28e4969b1b20626b81fd5676e26bde3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125392785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f73ec476781fa27ef0e9c0c86d6b7ae543bdc941594600bc413c1dd6bd6f30b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:10 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 07 Apr 2026 01:17:10 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 07 Apr 2026 01:17:10 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 07 Apr 2026 01:17:10 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:17:10 GMT
WORKDIR /opt/emqx
# Tue, 07 Apr 2026 01:17:10 GMT
USER emqx
# Tue, 07 Apr 2026 01:17:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Apr 2026 01:17:10 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Apr 2026 01:17:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Apr 2026 01:17:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:17:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d692929168b04452ca13ce8378b9c965bc38335bba90bf66a9ca574bbe23c10`  
		Last Modified: Tue, 07 Apr 2026 01:17:27 GMT  
		Size: 97.2 MB (97155389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4af1e3d75803dfd7a9ad58a00e23fbaad16d523c99b31058685891006da05f`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:950dd707a807507d9bcd498ba419ee44b7737851adb38f69c32be4de7a9e5dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b826abe84b74cbd98e8f8be6a45b08c66b5ec4827e4d15016656e7d8311841`

```dockerfile
```

-	Layers:
	-	`sha256:5525df91982c1447a18257ae702c636450e495dad8c977e52793f63a22f06e31`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60768565636cd2f466c0070db109526f0564997ca79f9ebb0d97800b9975b2f3`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c0651ac274a46b05f4040ee64fa4e0ab2da33c6628cd86772a32637bbbca08db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121833064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adf8404782e46fcb6edf9d42c2ee96503d9c2ec9c148fa1e4fb4a9cdb665762`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:16:28 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 07 Apr 2026 01:16:28 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 07 Apr 2026 01:16:28 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 07 Apr 2026 01:16:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Apr 2026 01:16:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:16:28 GMT
WORKDIR /opt/emqx
# Tue, 07 Apr 2026 01:16:28 GMT
USER emqx
# Tue, 07 Apr 2026 01:16:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Apr 2026 01:16:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Apr 2026 01:16:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Apr 2026 01:16:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:16:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd00317edc9d95188812f5d0749d414351c483ed3123e539d78f2fefedc6f`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
		Size: 93.7 MB (93715835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50b4a9124eee51e7085d2ddefe3f347a88b953d73d40d22dc02e182481f2470`  
		Last Modified: Tue, 07 Apr 2026 01:16:43 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:9e5622a7c6fa1706718bddb8a7069cf85f7a0af7850199689c476f80e570a1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503a5e2e0fc7bb5af2d4f2bce07372a0a29807de67aa2053eb6211e9720e7d20`

```dockerfile
```

-	Layers:
	-	`sha256:4848ac261c21a8e096e176eb888447afbc1a596fea9d25c430ca3de88e3ee641`  
		Last Modified: Tue, 07 Apr 2026 01:16:43 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62752bb49c2827dc4a3b26ec45c1d113ae00e8d810fbf48e0be1647bb9a0a319`  
		Last Modified: Tue, 07 Apr 2026 01:16:43 GMT  
		Size: 12.0 KB (11985 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:db9229a537fef40054aee6979bbc1122fb5068d53ccdac900f5c567e4accf528
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:ea230cd7671b28d9ea76f87e41497c2c28e4969b1b20626b81fd5676e26bde3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125392785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f73ec476781fa27ef0e9c0c86d6b7ae543bdc941594600bc413c1dd6bd6f30b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:10 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 07 Apr 2026 01:17:10 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 07 Apr 2026 01:17:10 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 07 Apr 2026 01:17:10 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:17:10 GMT
WORKDIR /opt/emqx
# Tue, 07 Apr 2026 01:17:10 GMT
USER emqx
# Tue, 07 Apr 2026 01:17:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Apr 2026 01:17:10 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Apr 2026 01:17:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Apr 2026 01:17:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:17:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d692929168b04452ca13ce8378b9c965bc38335bba90bf66a9ca574bbe23c10`  
		Last Modified: Tue, 07 Apr 2026 01:17:27 GMT  
		Size: 97.2 MB (97155389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4af1e3d75803dfd7a9ad58a00e23fbaad16d523c99b31058685891006da05f`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:950dd707a807507d9bcd498ba419ee44b7737851adb38f69c32be4de7a9e5dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b826abe84b74cbd98e8f8be6a45b08c66b5ec4827e4d15016656e7d8311841`

```dockerfile
```

-	Layers:
	-	`sha256:5525df91982c1447a18257ae702c636450e495dad8c977e52793f63a22f06e31`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60768565636cd2f466c0070db109526f0564997ca79f9ebb0d97800b9975b2f3`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c0651ac274a46b05f4040ee64fa4e0ab2da33c6628cd86772a32637bbbca08db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121833064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adf8404782e46fcb6edf9d42c2ee96503d9c2ec9c148fa1e4fb4a9cdb665762`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:16:28 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 07 Apr 2026 01:16:28 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 07 Apr 2026 01:16:28 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 07 Apr 2026 01:16:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Apr 2026 01:16:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:16:28 GMT
WORKDIR /opt/emqx
# Tue, 07 Apr 2026 01:16:28 GMT
USER emqx
# Tue, 07 Apr 2026 01:16:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Apr 2026 01:16:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Apr 2026 01:16:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Apr 2026 01:16:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:16:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79cd00317edc9d95188812f5d0749d414351c483ed3123e539d78f2fefedc6f`  
		Last Modified: Tue, 07 Apr 2026 01:16:46 GMT  
		Size: 93.7 MB (93715835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50b4a9124eee51e7085d2ddefe3f347a88b953d73d40d22dc02e182481f2470`  
		Last Modified: Tue, 07 Apr 2026 01:16:43 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:9e5622a7c6fa1706718bddb8a7069cf85f7a0af7850199689c476f80e570a1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503a5e2e0fc7bb5af2d4f2bce07372a0a29807de67aa2053eb6211e9720e7d20`

```dockerfile
```

-	Layers:
	-	`sha256:4848ac261c21a8e096e176eb888447afbc1a596fea9d25c430ca3de88e3ee641`  
		Last Modified: Tue, 07 Apr 2026 01:16:43 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62752bb49c2827dc4a3b26ec45c1d113ae00e8d810fbf48e0be1647bb9a0a319`  
		Last Modified: Tue, 07 Apr 2026 01:16:43 GMT  
		Size: 12.0 KB (11985 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:e61fac59b31a5f27f6a8701a179384bff775a74246ec77b52b26ea54ff804f47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

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

### `emqx:5.8` - unknown; unknown

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

### `emqx:5.8` - linux; arm64 variant v8

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

### `emqx:5.8` - unknown; unknown

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

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:e61fac59b31a5f27f6a8701a179384bff775a74246ec77b52b26ea54ff804f47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

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

### `emqx:5.8.8` - unknown; unknown

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

### `emqx:5.8.8` - linux; arm64 variant v8

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

### `emqx:5.8.8` - unknown; unknown

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
