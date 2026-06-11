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
$ docker pull emqx@sha256:c944155b31330c235c6547a3c8b791464e243d4c1ffbdc487a7ea07e94b884f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:2281829970b0aa2aa4f6859c9a523901a591211da88e9375ef130baef9922c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108411442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d2755311ecbd5b9f72e37374b0f3e6c8f6f46610eab24ce153b36457f4612f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:25 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 11 Jun 2026 00:16:25 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 11 Jun 2026 00:16:25 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 11 Jun 2026 00:16:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:26 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:26 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:26 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:26 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:26 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f881a9c1167b6fa7d201105a2e7da8c06c62c4d4c14b337ec638900238fc50`  
		Last Modified: Thu, 11 Jun 2026 00:16:42 GMT  
		Size: 78.6 MB (78624964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f87ed11191084273d14cd6fd32022406496212612fa4824459e0b4ceab9d3d0`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:40fc7276e2c07c7e5a53149d82feea061adfc76439abbe0a0df66f1b19df0094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511438c08b712efcf648fd0b978591d7ae186e4de48ec21c22967a6683060b10`

```dockerfile
```

-	Layers:
	-	`sha256:2f5741a64f9a397982543cdc907266c6fced22ee85d7d1edaab5fe0d6efa7538`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 2.4 MB (2403669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818a973edb6a84b429fa02bf3e9bc07a3404fd369996fccf057e9b13bdeb0e4d`  
		Last Modified: Thu, 11 Jun 2026 00:16:39 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9a2adc6770eda7504340e6f199952abab9449cb4cb777a87e122d429291ccb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106682221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4ce39443e10abb7c38f0c3fd1852b94103e9c3e1ba95706495f39fdcf8d833`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:02 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 11 Jun 2026 00:16:02 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 11 Jun 2026 00:16:02 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 11 Jun 2026 00:16:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:02 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:02 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:02 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:02 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:02 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e47907a0d537f528040e06440063f2303b79e699c5a695c0ea899ca5eb583e`  
		Last Modified: Thu, 11 Jun 2026 00:16:17 GMT  
		Size: 76.5 MB (76532627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129feb6d86266ed0aa75674d755fd73fcb10534cc2364a7f043cd04b270afde3`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:dff4c71d67365c8b642a54033f0151511d9c7fd8468ef1938d98136d485aca92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcd4702416f1c32dafdc85df48dc1b285828e2bb3b38e7a0846157f62b162f8`

```dockerfile
```

-	Layers:
	-	`sha256:e38a89c4f685b8a506930c7b461dc8d1f8ec7284df51b52f686d14322b04ffe1`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 2.4 MB (2403950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2529115c7398840e9ffe158eba86c29f265f6186a4b6f43f684471d6dad07f56`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:b500236af08586af8256ccd5f53bf2ac815dfe69356f29ebab5c11c07190a718
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:34440179ffb3a75a197e92b7541f75c544fdbaa87efab6abf64d35eebe7b0800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125396653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b2fb9d294cea19877a4073e101c9660cd481d8dfecb7ca6c2efbe8507f18c0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:16:22 GMT
ENV EMQX_VERSION=5.7.2
# Thu, 11 Jun 2026 00:16:22 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Thu, 11 Jun 2026 00:16:22 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Thu, 11 Jun 2026 00:16:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:22 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:22 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:22 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:22 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ef70d4cbcf56988e2219050e4caf8cb6b7f456e26f64e951cd4864e2e4948a`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 97.2 MB (97157966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04de636092fd9c363ce107e224b0fbe1f54997ef8b8ba2974a2d2384ea4b340`  
		Last Modified: Thu, 11 Jun 2026 00:16:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:45ce5007ad9989f166965aa3dec0e1801f155b323f887ed642c88c727f7e7ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177223894746d08712b3e41c43c12b4004d86b1db94f70b56d31d71475b3c7e0`

```dockerfile
```

-	Layers:
	-	`sha256:9441a159bd6f8630d771a1e95dbc00780451bca248cfe9540269e61f61031bd3`  
		Last Modified: Thu, 11 Jun 2026 00:16:37 GMT  
		Size: 2.8 MB (2751434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ca0550e2a9b43b9d6009aac73140918f1f565dfbdd79196d5c4616055616b8`  
		Last Modified: Thu, 11 Jun 2026 00:16:37 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8497c0fd0e93b3bd9cc7d3b94461fb2a5a8aa70dca835805323f8f5502327b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121843475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d7a9422694f058c254f18864bcba5d6541ef09cef999804fcead6f15754ff7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:16:00 GMT
ENV EMQX_VERSION=5.7.2
# Thu, 11 Jun 2026 00:16:00 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Thu, 11 Jun 2026 00:16:00 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Thu, 11 Jun 2026 00:16:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:00 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:00 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:00 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:00 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:00 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a53542af0aacb03e6416df33451ccb2650a9f495ace961bee3f3a47747b7f5`  
		Last Modified: Thu, 11 Jun 2026 00:16:17 GMT  
		Size: 93.7 MB (93720106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b19b1c6c9bd9288eb0564467dbb24b2666930a75ee6a66a72f15a2427ab3bb`  
		Last Modified: Thu, 11 Jun 2026 00:16:14 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:1533f760ee1a5a3abb16574481daf543ae0676ca0cd7cd103cb311c28d89dd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466f7769da04b9507239c3b77788c38ff3a47afa799ac35a6bb169bebc2570c5`

```dockerfile
```

-	Layers:
	-	`sha256:7270e0f97964c15a3df0dab0382d6a22361cbd4d88f2c733e17133b74262179f`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 2.8 MB (2751690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c09b1ff5fa11e9ce295dd13092042f4a594e8d328d2c3fb860bb79bb86ec6e8`  
		Last Modified: Thu, 11 Jun 2026 00:16:14 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:b500236af08586af8256ccd5f53bf2ac815dfe69356f29ebab5c11c07190a718
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:34440179ffb3a75a197e92b7541f75c544fdbaa87efab6abf64d35eebe7b0800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125396653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b2fb9d294cea19877a4073e101c9660cd481d8dfecb7ca6c2efbe8507f18c0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:16:22 GMT
ENV EMQX_VERSION=5.7.2
# Thu, 11 Jun 2026 00:16:22 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Thu, 11 Jun 2026 00:16:22 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Thu, 11 Jun 2026 00:16:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:22 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:22 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:22 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:22 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ef70d4cbcf56988e2219050e4caf8cb6b7f456e26f64e951cd4864e2e4948a`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 97.2 MB (97157966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04de636092fd9c363ce107e224b0fbe1f54997ef8b8ba2974a2d2384ea4b340`  
		Last Modified: Thu, 11 Jun 2026 00:16:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:45ce5007ad9989f166965aa3dec0e1801f155b323f887ed642c88c727f7e7ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177223894746d08712b3e41c43c12b4004d86b1db94f70b56d31d71475b3c7e0`

```dockerfile
```

-	Layers:
	-	`sha256:9441a159bd6f8630d771a1e95dbc00780451bca248cfe9540269e61f61031bd3`  
		Last Modified: Thu, 11 Jun 2026 00:16:37 GMT  
		Size: 2.8 MB (2751434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ca0550e2a9b43b9d6009aac73140918f1f565dfbdd79196d5c4616055616b8`  
		Last Modified: Thu, 11 Jun 2026 00:16:37 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8497c0fd0e93b3bd9cc7d3b94461fb2a5a8aa70dca835805323f8f5502327b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121843475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d7a9422694f058c254f18864bcba5d6541ef09cef999804fcead6f15754ff7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:16:00 GMT
ENV EMQX_VERSION=5.7.2
# Thu, 11 Jun 2026 00:16:00 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Thu, 11 Jun 2026 00:16:00 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Thu, 11 Jun 2026 00:16:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:00 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:00 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:00 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:00 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:00 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a53542af0aacb03e6416df33451ccb2650a9f495ace961bee3f3a47747b7f5`  
		Last Modified: Thu, 11 Jun 2026 00:16:17 GMT  
		Size: 93.7 MB (93720106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b19b1c6c9bd9288eb0564467dbb24b2666930a75ee6a66a72f15a2427ab3bb`  
		Last Modified: Thu, 11 Jun 2026 00:16:14 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:1533f760ee1a5a3abb16574481daf543ae0676ca0cd7cd103cb311c28d89dd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466f7769da04b9507239c3b77788c38ff3a47afa799ac35a6bb169bebc2570c5`

```dockerfile
```

-	Layers:
	-	`sha256:7270e0f97964c15a3df0dab0382d6a22361cbd4d88f2c733e17133b74262179f`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 2.8 MB (2751690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c09b1ff5fa11e9ce295dd13092042f4a594e8d328d2c3fb860bb79bb86ec6e8`  
		Last Modified: Thu, 11 Jun 2026 00:16:14 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:c944155b31330c235c6547a3c8b791464e243d4c1ffbdc487a7ea07e94b884f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:2281829970b0aa2aa4f6859c9a523901a591211da88e9375ef130baef9922c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108411442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d2755311ecbd5b9f72e37374b0f3e6c8f6f46610eab24ce153b36457f4612f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:25 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 11 Jun 2026 00:16:25 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 11 Jun 2026 00:16:25 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 11 Jun 2026 00:16:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:26 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:26 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:26 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:26 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:26 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f881a9c1167b6fa7d201105a2e7da8c06c62c4d4c14b337ec638900238fc50`  
		Last Modified: Thu, 11 Jun 2026 00:16:42 GMT  
		Size: 78.6 MB (78624964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f87ed11191084273d14cd6fd32022406496212612fa4824459e0b4ceab9d3d0`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:40fc7276e2c07c7e5a53149d82feea061adfc76439abbe0a0df66f1b19df0094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511438c08b712efcf648fd0b978591d7ae186e4de48ec21c22967a6683060b10`

```dockerfile
```

-	Layers:
	-	`sha256:2f5741a64f9a397982543cdc907266c6fced22ee85d7d1edaab5fe0d6efa7538`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 2.4 MB (2403669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818a973edb6a84b429fa02bf3e9bc07a3404fd369996fccf057e9b13bdeb0e4d`  
		Last Modified: Thu, 11 Jun 2026 00:16:39 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9a2adc6770eda7504340e6f199952abab9449cb4cb777a87e122d429291ccb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106682221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4ce39443e10abb7c38f0c3fd1852b94103e9c3e1ba95706495f39fdcf8d833`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:02 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 11 Jun 2026 00:16:02 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 11 Jun 2026 00:16:02 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 11 Jun 2026 00:16:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:02 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:02 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:02 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:02 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:02 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e47907a0d537f528040e06440063f2303b79e699c5a695c0ea899ca5eb583e`  
		Last Modified: Thu, 11 Jun 2026 00:16:17 GMT  
		Size: 76.5 MB (76532627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129feb6d86266ed0aa75674d755fd73fcb10534cc2364a7f043cd04b270afde3`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:dff4c71d67365c8b642a54033f0151511d9c7fd8468ef1938d98136d485aca92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcd4702416f1c32dafdc85df48dc1b285828e2bb3b38e7a0846157f62b162f8`

```dockerfile
```

-	Layers:
	-	`sha256:e38a89c4f685b8a506930c7b461dc8d1f8ec7284df51b52f686d14322b04ffe1`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 2.4 MB (2403950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2529115c7398840e9ffe158eba86c29f265f6186a4b6f43f684471d6dad07f56`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:c944155b31330c235c6547a3c8b791464e243d4c1ffbdc487a7ea07e94b884f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:2281829970b0aa2aa4f6859c9a523901a591211da88e9375ef130baef9922c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108411442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d2755311ecbd5b9f72e37374b0f3e6c8f6f46610eab24ce153b36457f4612f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:25 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 11 Jun 2026 00:16:25 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 11 Jun 2026 00:16:25 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 11 Jun 2026 00:16:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:26 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:26 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:26 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:26 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:26 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f881a9c1167b6fa7d201105a2e7da8c06c62c4d4c14b337ec638900238fc50`  
		Last Modified: Thu, 11 Jun 2026 00:16:42 GMT  
		Size: 78.6 MB (78624964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f87ed11191084273d14cd6fd32022406496212612fa4824459e0b4ceab9d3d0`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:40fc7276e2c07c7e5a53149d82feea061adfc76439abbe0a0df66f1b19df0094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511438c08b712efcf648fd0b978591d7ae186e4de48ec21c22967a6683060b10`

```dockerfile
```

-	Layers:
	-	`sha256:2f5741a64f9a397982543cdc907266c6fced22ee85d7d1edaab5fe0d6efa7538`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 2.4 MB (2403669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818a973edb6a84b429fa02bf3e9bc07a3404fd369996fccf057e9b13bdeb0e4d`  
		Last Modified: Thu, 11 Jun 2026 00:16:39 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9a2adc6770eda7504340e6f199952abab9449cb4cb777a87e122d429291ccb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106682221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4ce39443e10abb7c38f0c3fd1852b94103e9c3e1ba95706495f39fdcf8d833`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:02 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 11 Jun 2026 00:16:02 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 11 Jun 2026 00:16:02 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 11 Jun 2026 00:16:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:02 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:02 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:02 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:02 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:02 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e47907a0d537f528040e06440063f2303b79e699c5a695c0ea899ca5eb583e`  
		Last Modified: Thu, 11 Jun 2026 00:16:17 GMT  
		Size: 76.5 MB (76532627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129feb6d86266ed0aa75674d755fd73fcb10534cc2364a7f043cd04b270afde3`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:dff4c71d67365c8b642a54033f0151511d9c7fd8468ef1938d98136d485aca92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcd4702416f1c32dafdc85df48dc1b285828e2bb3b38e7a0846157f62b162f8`

```dockerfile
```

-	Layers:
	-	`sha256:e38a89c4f685b8a506930c7b461dc8d1f8ec7284df51b52f686d14322b04ffe1`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 2.4 MB (2403950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2529115c7398840e9ffe158eba86c29f265f6186a4b6f43f684471d6dad07f56`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:c944155b31330c235c6547a3c8b791464e243d4c1ffbdc487a7ea07e94b884f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:2281829970b0aa2aa4f6859c9a523901a591211da88e9375ef130baef9922c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108411442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d2755311ecbd5b9f72e37374b0f3e6c8f6f46610eab24ce153b36457f4612f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:25 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 11 Jun 2026 00:16:25 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 11 Jun 2026 00:16:25 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 11 Jun 2026 00:16:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:26 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:26 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:26 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:26 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:26 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f881a9c1167b6fa7d201105a2e7da8c06c62c4d4c14b337ec638900238fc50`  
		Last Modified: Thu, 11 Jun 2026 00:16:42 GMT  
		Size: 78.6 MB (78624964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f87ed11191084273d14cd6fd32022406496212612fa4824459e0b4ceab9d3d0`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:40fc7276e2c07c7e5a53149d82feea061adfc76439abbe0a0df66f1b19df0094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511438c08b712efcf648fd0b978591d7ae186e4de48ec21c22967a6683060b10`

```dockerfile
```

-	Layers:
	-	`sha256:2f5741a64f9a397982543cdc907266c6fced22ee85d7d1edaab5fe0d6efa7538`  
		Last Modified: Thu, 11 Jun 2026 00:16:40 GMT  
		Size: 2.4 MB (2403669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818a973edb6a84b429fa02bf3e9bc07a3404fd369996fccf057e9b13bdeb0e4d`  
		Last Modified: Thu, 11 Jun 2026 00:16:39 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9a2adc6770eda7504340e6f199952abab9449cb4cb777a87e122d429291ccb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106682221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4ce39443e10abb7c38f0c3fd1852b94103e9c3e1ba95706495f39fdcf8d833`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:02 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 11 Jun 2026 00:16:02 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 11 Jun 2026 00:16:02 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 11 Jun 2026 00:16:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jun 2026 00:16:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 00:16:02 GMT
WORKDIR /opt/emqx
# Thu, 11 Jun 2026 00:16:02 GMT
USER emqx
# Thu, 11 Jun 2026 00:16:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jun 2026 00:16:02 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 11 Jun 2026 00:16:02 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 11 Jun 2026 00:16:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:16:02 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e47907a0d537f528040e06440063f2303b79e699c5a695c0ea899ca5eb583e`  
		Last Modified: Thu, 11 Jun 2026 00:16:17 GMT  
		Size: 76.5 MB (76532627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129feb6d86266ed0aa75674d755fd73fcb10534cc2364a7f043cd04b270afde3`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:dff4c71d67365c8b642a54033f0151511d9c7fd8468ef1938d98136d485aca92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcd4702416f1c32dafdc85df48dc1b285828e2bb3b38e7a0846157f62b162f8`

```dockerfile
```

-	Layers:
	-	`sha256:e38a89c4f685b8a506930c7b461dc8d1f8ec7284df51b52f686d14322b04ffe1`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 2.4 MB (2403950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2529115c7398840e9ffe158eba86c29f265f6186a4b6f43f684471d6dad07f56`  
		Last Modified: Thu, 11 Jun 2026 00:16:15 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
