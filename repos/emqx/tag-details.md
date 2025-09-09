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
$ docker pull emqx@sha256:16dd883c345325dac977b9ee34eae6c9b127edfaedf48cca812756710fbe062a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

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

### `emqx:5` - unknown; unknown

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

### `emqx:5` - linux; arm64 variant v8

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

### `emqx:5` - unknown; unknown

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

## `emqx:5.7`

```console
$ docker pull emqx@sha256:486c6c1f4811113af2da36589e77a384a80655c81733fcd1569161ea1bf0f23b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:a6800d6fea0ca76485764bbc557b3413bcd9e098a8791864e83ca9fbe97c268e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8fd65d81b0417883460c0b1787b3932d901e713394ec5c9f3fdbcacd8a181b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f2f2522ec0d89b6e6e4b3559366765d6c02a9021d80834d261a199288d3c10`  
		Last Modified: Mon, 08 Sep 2025 21:57:27 GMT  
		Size: 97.2 MB (97155146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bb5562da1a980753eaa34a5cd007b2f981acaf7e8b2b84d7fcc7960c852007`  
		Last Modified: Mon, 08 Sep 2025 21:52:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:76b6eb0faa5d381df687f0fa02b4ac6d38ec91dd2a48a88b7ed2ba1933dbb881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c64fbf3da71ea068b9eb43adcfe0c0b5742c5b3dbbc6c8129cbd9edcfb2902`

```dockerfile
```

-	Layers:
	-	`sha256:6c6d146872477a7c666c62f77040fa8d549c73cf7e13669c38f37833f1baa5fa`  
		Last Modified: Mon, 08 Sep 2025 23:27:30 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da01f7b8640aaefbf32b60a17aa352692d8e155090227051d56991befed866f`  
		Last Modified: Mon, 08 Sep 2025 23:27:31 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8045fab44a097b4a9c96b8bac4a419e7d057a48dda5237ab86f68dce83f94775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e438acc8793f255c11a4c0d5a8faa948a557898be7ebf761bc0ee5f63ebe26d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f5f876bb42499944501e118fc42204348fc514e9a9b4781ef48df12f7be8e5`  
		Last Modified: Mon, 08 Sep 2025 21:28:34 GMT  
		Size: 93.7 MB (93715165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9df52ca3b9c69d449f434aa6284ebe13740c787f95db4c430ed5ea87afa9fa8`  
		Last Modified: Mon, 08 Sep 2025 21:28:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:1f85135b6662eb28fdbdcd10a1d21dc83ef415eac5bc713f287ee36b09b17648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae461d5157d767d702be80d31bf9c9f5d71b2c88f58c618f26b56e3f2c01a4a9`

```dockerfile
```

-	Layers:
	-	`sha256:427915ae922d012ec181478f28aaa49fedcf8a08d009be44f4748e5bbcb447bf`  
		Last Modified: Mon, 08 Sep 2025 23:27:36 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43075a5210be30d66f18ed35ca8ab17692cf19ae95b3c3b4848ccfd2e5dc0f9`  
		Last Modified: Mon, 08 Sep 2025 23:27:37 GMT  
		Size: 12.0 KB (12030 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:486c6c1f4811113af2da36589e77a384a80655c81733fcd1569161ea1bf0f23b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:a6800d6fea0ca76485764bbc557b3413bcd9e098a8791864e83ca9fbe97c268e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8fd65d81b0417883460c0b1787b3932d901e713394ec5c9f3fdbcacd8a181b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f2f2522ec0d89b6e6e4b3559366765d6c02a9021d80834d261a199288d3c10`  
		Last Modified: Mon, 08 Sep 2025 21:57:27 GMT  
		Size: 97.2 MB (97155146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bb5562da1a980753eaa34a5cd007b2f981acaf7e8b2b84d7fcc7960c852007`  
		Last Modified: Mon, 08 Sep 2025 21:52:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:76b6eb0faa5d381df687f0fa02b4ac6d38ec91dd2a48a88b7ed2ba1933dbb881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c64fbf3da71ea068b9eb43adcfe0c0b5742c5b3dbbc6c8129cbd9edcfb2902`

```dockerfile
```

-	Layers:
	-	`sha256:6c6d146872477a7c666c62f77040fa8d549c73cf7e13669c38f37833f1baa5fa`  
		Last Modified: Mon, 08 Sep 2025 23:27:30 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da01f7b8640aaefbf32b60a17aa352692d8e155090227051d56991befed866f`  
		Last Modified: Mon, 08 Sep 2025 23:27:31 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8045fab44a097b4a9c96b8bac4a419e7d057a48dda5237ab86f68dce83f94775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e438acc8793f255c11a4c0d5a8faa948a557898be7ebf761bc0ee5f63ebe26d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f5f876bb42499944501e118fc42204348fc514e9a9b4781ef48df12f7be8e5`  
		Last Modified: Mon, 08 Sep 2025 21:28:34 GMT  
		Size: 93.7 MB (93715165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9df52ca3b9c69d449f434aa6284ebe13740c787f95db4c430ed5ea87afa9fa8`  
		Last Modified: Mon, 08 Sep 2025 21:28:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:1f85135b6662eb28fdbdcd10a1d21dc83ef415eac5bc713f287ee36b09b17648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae461d5157d767d702be80d31bf9c9f5d71b2c88f58c618f26b56e3f2c01a4a9`

```dockerfile
```

-	Layers:
	-	`sha256:427915ae922d012ec181478f28aaa49fedcf8a08d009be44f4748e5bbcb447bf`  
		Last Modified: Mon, 08 Sep 2025 23:27:36 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43075a5210be30d66f18ed35ca8ab17692cf19ae95b3c3b4848ccfd2e5dc0f9`  
		Last Modified: Mon, 08 Sep 2025 23:27:37 GMT  
		Size: 12.0 KB (12030 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:16dd883c345325dac977b9ee34eae6c9b127edfaedf48cca812756710fbe062a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

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

### `emqx:5.8` - unknown; unknown

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

### `emqx:5.8` - linux; arm64 variant v8

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

### `emqx:5.8` - unknown; unknown

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

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:16dd883c345325dac977b9ee34eae6c9b127edfaedf48cca812756710fbe062a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

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

### `emqx:5.8.8` - unknown; unknown

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

### `emqx:5.8.8` - linux; arm64 variant v8

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

### `emqx:5.8.8` - unknown; unknown

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
