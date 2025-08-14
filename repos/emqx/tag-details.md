<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.7`](#emqx587)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:caa0f45146f33639c5c6f8710b8a9827f05a03d0b64a575e25e70f069dc803b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:a369506b3b5375cac4bba0107dd15334366569d218ebba773b2f9f67eef4b180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105580770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a001fc438393528e457bc550accd33e99916a24c698f7a0309261343d57449`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 03 Jul 2025 07:12:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 03 Jul 2025 07:12:29 GMT
ENV EMQX_VERSION=5.8.7
# Thu, 03 Jul 2025 07:12:29 GMT
ENV AMD64_SHA256=a4ac9db115ab06e3d8dfdeefa71dbfb96ac039279e55df98575e14ba34ed2b1d
# Thu, 03 Jul 2025 07:12:29 GMT
ENV ARM64_SHA256=6efd454c0a0ef0d01ad22f804c91e4502287834de0f5cd3c70381daed43d398f
# Thu, 03 Jul 2025 07:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 03 Jul 2025 07:12:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
WORKDIR /opt/emqx
# Thu, 03 Jul 2025 07:12:29 GMT
USER emqx
# Thu, 03 Jul 2025 07:12:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 03 Jul 2025 07:12:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 03 Jul 2025 07:12:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 03 Jul 2025 07:12:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6234a3529fb6b81fd0596a3f25c72865dd2b42d1ebacf7bbfe55339f829ce4e6`  
		Last Modified: Tue, 12 Aug 2025 23:27:34 GMT  
		Size: 77.3 MB (77349451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74f0ffefb82cb27fca6387b280c5befc0446298d8b7f5cc93a6a6e804aa4ba`  
		Last Modified: Tue, 12 Aug 2025 21:22:46 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:c7fa268c509023a7405749b5fce6d4d775f4ca671a6028d6d6f655ca471635b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f8dc640a37d560a806e9438ea954e2693668b06cc5099f64f6d3bd78ccf5f2`

```dockerfile
```

-	Layers:
	-	`sha256:635b722526cd962e11fedf4c91633abfaecfd9c97e7c3a1d3f07f68b65e67007`  
		Last Modified: Tue, 12 Aug 2025 23:27:18 GMT  
		Size: 2.7 MB (2741191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12af576a93f53948073290b1545e46c8334d85d0982a9ebe20e4fb9170e10235`  
		Last Modified: Tue, 12 Aug 2025 23:27:19 GMT  
		Size: 12.5 KB (12528 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6b8f40b0ad4c6732169d425ec2c76a6d95fe539e25f57851073dacf5a2b7c013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102702155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca01bcb9a39310052fc89d8eb96a445599a49a446883f57c5285fdad7cb97840`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 03 Jul 2025 07:12:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 03 Jul 2025 07:12:29 GMT
ENV EMQX_VERSION=5.8.7
# Thu, 03 Jul 2025 07:12:29 GMT
ENV AMD64_SHA256=a4ac9db115ab06e3d8dfdeefa71dbfb96ac039279e55df98575e14ba34ed2b1d
# Thu, 03 Jul 2025 07:12:29 GMT
ENV ARM64_SHA256=6efd454c0a0ef0d01ad22f804c91e4502287834de0f5cd3c70381daed43d398f
# Thu, 03 Jul 2025 07:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 03 Jul 2025 07:12:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
WORKDIR /opt/emqx
# Thu, 03 Jul 2025 07:12:29 GMT
USER emqx
# Thu, 03 Jul 2025 07:12:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 03 Jul 2025 07:12:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 03 Jul 2025 07:12:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 03 Jul 2025 07:12:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0250921f7ab11be50266cb10738f072e37c42956edd9e3e9e34995893e4a9`  
		Last Modified: Wed, 13 Aug 2025 01:53:46 GMT  
		Size: 74.6 MB (74619092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2502a6b5926e0e9baed02a4f2c77acc1b086e4e5d13b521368b94485b22b14`  
		Last Modified: Wed, 13 Aug 2025 01:53:38 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:3406a1ecd76594eb194d546286f985c03fd504fafe77953b1be4dc1a1e6f808f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2754104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b091ada8ef738d5274e52a6c8783812ae611c5a156dc07537bb6b66b5cc066a`

```dockerfile
```

-	Layers:
	-	`sha256:a5d94c538902b9ba5f36e1ab178ec8d23f5194e1b49e1df4f7135fec0f0345a4`  
		Last Modified: Wed, 13 Aug 2025 02:27:21 GMT  
		Size: 2.7 MB (2741471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d4e1e4651e483833655d43d66d611d4e420a1983d081a3657d4e84fb27e049`  
		Last Modified: Wed, 13 Aug 2025 02:27:22 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:e84f34ca19cba9bde6c94ed13312b67cceb92222d156c631429dd5a35db47f54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:bbf3809047d4810c726696f78d12baf0227c79e16507e95649f06341f2077668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125386325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0413e5e12108945ad78a3fbc52f6bcf7ee00a32d51de0c5c47aed83b7c027a6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c54a8abe57913f7f0cb31f506ff87dcf7bc3d714e32b84552e467d43de7f21c`  
		Last Modified: Tue, 12 Aug 2025 21:11:16 GMT  
		Size: 97.2 MB (97155008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae14ca16209adb5ded2c02a6e36d92942eebeaa21aaf6190d339848850a539`  
		Last Modified: Tue, 12 Aug 2025 21:10:57 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:71cda6b20b5c6ef02d78ffe699d8a78a4179b2cadb6cd5a3609c6354a977dbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2761224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4a6928c55b8365a23c50fbda7f34d08eecafc28875fc6e7594ea950260d8ef`

```dockerfile
```

-	Layers:
	-	`sha256:f9b56dc2ae0a6525337a95dad5b17e5655c4c6551c6c7658b6ade053702ed8d0`  
		Last Modified: Tue, 12 Aug 2025 23:27:21 GMT  
		Size: 2.7 MB (2749273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84c9d9b8ab555b6cb4f3d403b0a59b086a5cfd2276b83965fa58b3e13fc2773`  
		Last Modified: Tue, 12 Aug 2025 23:27:22 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5019f315a33aa0dca8c6287212b63448537c99e439d2bf9bd2319dee32d9ab84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121795395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1a948eee2ebb9132cb4464d087114a4c3650bda2046032bb1af0a2aed630d0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c838d6d31fd3fb6f2eeb9590bbfde7d14a8a9b8ad70672db7850c48a4dd2f2`  
		Last Modified: Wed, 13 Aug 2025 01:53:26 GMT  
		Size: 93.7 MB (93712331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0105be49a70c933b98dadb79fe96d877f4555b2645ada0b11ffd00953fbb46c`  
		Last Modified: Wed, 13 Aug 2025 01:53:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:0c0a017df0a6bf07cf50821750e48f117bc4428f693e0420c39563074435b8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2761559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f479a6db4d7de493c04d6debfc54fd2cbd387257166e0215fc3f701597e86c`

```dockerfile
```

-	Layers:
	-	`sha256:030440ba03243009b4a79c8cadda963a7ed378c9cbfa579402059b07338a4f2a`  
		Last Modified: Wed, 13 Aug 2025 02:27:27 GMT  
		Size: 2.7 MB (2749529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21c06c36de70bf42a6df1e487db48c2ec2fa7293eb14eb835895e322ae519606`  
		Last Modified: Wed, 13 Aug 2025 02:27:28 GMT  
		Size: 12.0 KB (12030 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:e84f34ca19cba9bde6c94ed13312b67cceb92222d156c631429dd5a35db47f54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:bbf3809047d4810c726696f78d12baf0227c79e16507e95649f06341f2077668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125386325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0413e5e12108945ad78a3fbc52f6bcf7ee00a32d51de0c5c47aed83b7c027a6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c54a8abe57913f7f0cb31f506ff87dcf7bc3d714e32b84552e467d43de7f21c`  
		Last Modified: Tue, 12 Aug 2025 21:11:16 GMT  
		Size: 97.2 MB (97155008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae14ca16209adb5ded2c02a6e36d92942eebeaa21aaf6190d339848850a539`  
		Last Modified: Tue, 12 Aug 2025 21:10:57 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:71cda6b20b5c6ef02d78ffe699d8a78a4179b2cadb6cd5a3609c6354a977dbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2761224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4a6928c55b8365a23c50fbda7f34d08eecafc28875fc6e7594ea950260d8ef`

```dockerfile
```

-	Layers:
	-	`sha256:f9b56dc2ae0a6525337a95dad5b17e5655c4c6551c6c7658b6ade053702ed8d0`  
		Last Modified: Tue, 12 Aug 2025 23:27:21 GMT  
		Size: 2.7 MB (2749273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84c9d9b8ab555b6cb4f3d403b0a59b086a5cfd2276b83965fa58b3e13fc2773`  
		Last Modified: Tue, 12 Aug 2025 23:27:22 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5019f315a33aa0dca8c6287212b63448537c99e439d2bf9bd2319dee32d9ab84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121795395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1a948eee2ebb9132cb4464d087114a4c3650bda2046032bb1af0a2aed630d0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c838d6d31fd3fb6f2eeb9590bbfde7d14a8a9b8ad70672db7850c48a4dd2f2`  
		Last Modified: Wed, 13 Aug 2025 01:53:26 GMT  
		Size: 93.7 MB (93712331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0105be49a70c933b98dadb79fe96d877f4555b2645ada0b11ffd00953fbb46c`  
		Last Modified: Wed, 13 Aug 2025 01:53:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:0c0a017df0a6bf07cf50821750e48f117bc4428f693e0420c39563074435b8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2761559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f479a6db4d7de493c04d6debfc54fd2cbd387257166e0215fc3f701597e86c`

```dockerfile
```

-	Layers:
	-	`sha256:030440ba03243009b4a79c8cadda963a7ed378c9cbfa579402059b07338a4f2a`  
		Last Modified: Wed, 13 Aug 2025 02:27:27 GMT  
		Size: 2.7 MB (2749529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21c06c36de70bf42a6df1e487db48c2ec2fa7293eb14eb835895e322ae519606`  
		Last Modified: Wed, 13 Aug 2025 02:27:28 GMT  
		Size: 12.0 KB (12030 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:caa0f45146f33639c5c6f8710b8a9827f05a03d0b64a575e25e70f069dc803b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:a369506b3b5375cac4bba0107dd15334366569d218ebba773b2f9f67eef4b180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105580770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a001fc438393528e457bc550accd33e99916a24c698f7a0309261343d57449`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 03 Jul 2025 07:12:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 03 Jul 2025 07:12:29 GMT
ENV EMQX_VERSION=5.8.7
# Thu, 03 Jul 2025 07:12:29 GMT
ENV AMD64_SHA256=a4ac9db115ab06e3d8dfdeefa71dbfb96ac039279e55df98575e14ba34ed2b1d
# Thu, 03 Jul 2025 07:12:29 GMT
ENV ARM64_SHA256=6efd454c0a0ef0d01ad22f804c91e4502287834de0f5cd3c70381daed43d398f
# Thu, 03 Jul 2025 07:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 03 Jul 2025 07:12:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
WORKDIR /opt/emqx
# Thu, 03 Jul 2025 07:12:29 GMT
USER emqx
# Thu, 03 Jul 2025 07:12:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 03 Jul 2025 07:12:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 03 Jul 2025 07:12:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 03 Jul 2025 07:12:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6234a3529fb6b81fd0596a3f25c72865dd2b42d1ebacf7bbfe55339f829ce4e6`  
		Last Modified: Tue, 12 Aug 2025 23:27:34 GMT  
		Size: 77.3 MB (77349451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74f0ffefb82cb27fca6387b280c5befc0446298d8b7f5cc93a6a6e804aa4ba`  
		Last Modified: Tue, 12 Aug 2025 21:22:46 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:c7fa268c509023a7405749b5fce6d4d775f4ca671a6028d6d6f655ca471635b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f8dc640a37d560a806e9438ea954e2693668b06cc5099f64f6d3bd78ccf5f2`

```dockerfile
```

-	Layers:
	-	`sha256:635b722526cd962e11fedf4c91633abfaecfd9c97e7c3a1d3f07f68b65e67007`  
		Last Modified: Tue, 12 Aug 2025 23:27:18 GMT  
		Size: 2.7 MB (2741191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12af576a93f53948073290b1545e46c8334d85d0982a9ebe20e4fb9170e10235`  
		Last Modified: Tue, 12 Aug 2025 23:27:19 GMT  
		Size: 12.5 KB (12528 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6b8f40b0ad4c6732169d425ec2c76a6d95fe539e25f57851073dacf5a2b7c013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102702155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca01bcb9a39310052fc89d8eb96a445599a49a446883f57c5285fdad7cb97840`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 03 Jul 2025 07:12:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 03 Jul 2025 07:12:29 GMT
ENV EMQX_VERSION=5.8.7
# Thu, 03 Jul 2025 07:12:29 GMT
ENV AMD64_SHA256=a4ac9db115ab06e3d8dfdeefa71dbfb96ac039279e55df98575e14ba34ed2b1d
# Thu, 03 Jul 2025 07:12:29 GMT
ENV ARM64_SHA256=6efd454c0a0ef0d01ad22f804c91e4502287834de0f5cd3c70381daed43d398f
# Thu, 03 Jul 2025 07:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 03 Jul 2025 07:12:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
WORKDIR /opt/emqx
# Thu, 03 Jul 2025 07:12:29 GMT
USER emqx
# Thu, 03 Jul 2025 07:12:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 03 Jul 2025 07:12:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 03 Jul 2025 07:12:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 03 Jul 2025 07:12:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0250921f7ab11be50266cb10738f072e37c42956edd9e3e9e34995893e4a9`  
		Last Modified: Wed, 13 Aug 2025 01:53:46 GMT  
		Size: 74.6 MB (74619092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2502a6b5926e0e9baed02a4f2c77acc1b086e4e5d13b521368b94485b22b14`  
		Last Modified: Wed, 13 Aug 2025 01:53:38 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:3406a1ecd76594eb194d546286f985c03fd504fafe77953b1be4dc1a1e6f808f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2754104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b091ada8ef738d5274e52a6c8783812ae611c5a156dc07537bb6b66b5cc066a`

```dockerfile
```

-	Layers:
	-	`sha256:a5d94c538902b9ba5f36e1ab178ec8d23f5194e1b49e1df4f7135fec0f0345a4`  
		Last Modified: Wed, 13 Aug 2025 02:27:21 GMT  
		Size: 2.7 MB (2741471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d4e1e4651e483833655d43d66d611d4e420a1983d081a3657d4e84fb27e049`  
		Last Modified: Wed, 13 Aug 2025 02:27:22 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.7`

```console
$ docker pull emqx@sha256:caa0f45146f33639c5c6f8710b8a9827f05a03d0b64a575e25e70f069dc803b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.7` - linux; amd64

```console
$ docker pull emqx@sha256:a369506b3b5375cac4bba0107dd15334366569d218ebba773b2f9f67eef4b180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105580770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a001fc438393528e457bc550accd33e99916a24c698f7a0309261343d57449`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 03 Jul 2025 07:12:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 03 Jul 2025 07:12:29 GMT
ENV EMQX_VERSION=5.8.7
# Thu, 03 Jul 2025 07:12:29 GMT
ENV AMD64_SHA256=a4ac9db115ab06e3d8dfdeefa71dbfb96ac039279e55df98575e14ba34ed2b1d
# Thu, 03 Jul 2025 07:12:29 GMT
ENV ARM64_SHA256=6efd454c0a0ef0d01ad22f804c91e4502287834de0f5cd3c70381daed43d398f
# Thu, 03 Jul 2025 07:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 03 Jul 2025 07:12:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
WORKDIR /opt/emqx
# Thu, 03 Jul 2025 07:12:29 GMT
USER emqx
# Thu, 03 Jul 2025 07:12:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 03 Jul 2025 07:12:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 03 Jul 2025 07:12:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 03 Jul 2025 07:12:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6234a3529fb6b81fd0596a3f25c72865dd2b42d1ebacf7bbfe55339f829ce4e6`  
		Last Modified: Tue, 12 Aug 2025 23:27:34 GMT  
		Size: 77.3 MB (77349451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74f0ffefb82cb27fca6387b280c5befc0446298d8b7f5cc93a6a6e804aa4ba`  
		Last Modified: Tue, 12 Aug 2025 21:22:46 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.7` - unknown; unknown

```console
$ docker pull emqx@sha256:c7fa268c509023a7405749b5fce6d4d775f4ca671a6028d6d6f655ca471635b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f8dc640a37d560a806e9438ea954e2693668b06cc5099f64f6d3bd78ccf5f2`

```dockerfile
```

-	Layers:
	-	`sha256:635b722526cd962e11fedf4c91633abfaecfd9c97e7c3a1d3f07f68b65e67007`  
		Last Modified: Tue, 12 Aug 2025 23:27:18 GMT  
		Size: 2.7 MB (2741191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12af576a93f53948073290b1545e46c8334d85d0982a9ebe20e4fb9170e10235`  
		Last Modified: Tue, 12 Aug 2025 23:27:19 GMT  
		Size: 12.5 KB (12528 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6b8f40b0ad4c6732169d425ec2c76a6d95fe539e25f57851073dacf5a2b7c013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102702155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca01bcb9a39310052fc89d8eb96a445599a49a446883f57c5285fdad7cb97840`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 03 Jul 2025 07:12:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 03 Jul 2025 07:12:29 GMT
ENV EMQX_VERSION=5.8.7
# Thu, 03 Jul 2025 07:12:29 GMT
ENV AMD64_SHA256=a4ac9db115ab06e3d8dfdeefa71dbfb96ac039279e55df98575e14ba34ed2b1d
# Thu, 03 Jul 2025 07:12:29 GMT
ENV ARM64_SHA256=6efd454c0a0ef0d01ad22f804c91e4502287834de0f5cd3c70381daed43d398f
# Thu, 03 Jul 2025 07:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 03 Jul 2025 07:12:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
WORKDIR /opt/emqx
# Thu, 03 Jul 2025 07:12:29 GMT
USER emqx
# Thu, 03 Jul 2025 07:12:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 03 Jul 2025 07:12:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 03 Jul 2025 07:12:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 03 Jul 2025 07:12:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0250921f7ab11be50266cb10738f072e37c42956edd9e3e9e34995893e4a9`  
		Last Modified: Wed, 13 Aug 2025 01:53:46 GMT  
		Size: 74.6 MB (74619092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2502a6b5926e0e9baed02a4f2c77acc1b086e4e5d13b521368b94485b22b14`  
		Last Modified: Wed, 13 Aug 2025 01:53:38 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.7` - unknown; unknown

```console
$ docker pull emqx@sha256:3406a1ecd76594eb194d546286f985c03fd504fafe77953b1be4dc1a1e6f808f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2754104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b091ada8ef738d5274e52a6c8783812ae611c5a156dc07537bb6b66b5cc066a`

```dockerfile
```

-	Layers:
	-	`sha256:a5d94c538902b9ba5f36e1ab178ec8d23f5194e1b49e1df4f7135fec0f0345a4`  
		Last Modified: Wed, 13 Aug 2025 02:27:21 GMT  
		Size: 2.7 MB (2741471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d4e1e4651e483833655d43d66d611d4e420a1983d081a3657d4e84fb27e049`  
		Last Modified: Wed, 13 Aug 2025 02:27:22 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:caa0f45146f33639c5c6f8710b8a9827f05a03d0b64a575e25e70f069dc803b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:a369506b3b5375cac4bba0107dd15334366569d218ebba773b2f9f67eef4b180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105580770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a001fc438393528e457bc550accd33e99916a24c698f7a0309261343d57449`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 03 Jul 2025 07:12:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 03 Jul 2025 07:12:29 GMT
ENV EMQX_VERSION=5.8.7
# Thu, 03 Jul 2025 07:12:29 GMT
ENV AMD64_SHA256=a4ac9db115ab06e3d8dfdeefa71dbfb96ac039279e55df98575e14ba34ed2b1d
# Thu, 03 Jul 2025 07:12:29 GMT
ENV ARM64_SHA256=6efd454c0a0ef0d01ad22f804c91e4502287834de0f5cd3c70381daed43d398f
# Thu, 03 Jul 2025 07:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 03 Jul 2025 07:12:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
WORKDIR /opt/emqx
# Thu, 03 Jul 2025 07:12:29 GMT
USER emqx
# Thu, 03 Jul 2025 07:12:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 03 Jul 2025 07:12:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 03 Jul 2025 07:12:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 03 Jul 2025 07:12:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6234a3529fb6b81fd0596a3f25c72865dd2b42d1ebacf7bbfe55339f829ce4e6`  
		Last Modified: Tue, 12 Aug 2025 23:27:34 GMT  
		Size: 77.3 MB (77349451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74f0ffefb82cb27fca6387b280c5befc0446298d8b7f5cc93a6a6e804aa4ba`  
		Last Modified: Tue, 12 Aug 2025 21:22:46 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:c7fa268c509023a7405749b5fce6d4d775f4ca671a6028d6d6f655ca471635b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f8dc640a37d560a806e9438ea954e2693668b06cc5099f64f6d3bd78ccf5f2`

```dockerfile
```

-	Layers:
	-	`sha256:635b722526cd962e11fedf4c91633abfaecfd9c97e7c3a1d3f07f68b65e67007`  
		Last Modified: Tue, 12 Aug 2025 23:27:18 GMT  
		Size: 2.7 MB (2741191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12af576a93f53948073290b1545e46c8334d85d0982a9ebe20e4fb9170e10235`  
		Last Modified: Tue, 12 Aug 2025 23:27:19 GMT  
		Size: 12.5 KB (12528 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6b8f40b0ad4c6732169d425ec2c76a6d95fe539e25f57851073dacf5a2b7c013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102702155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca01bcb9a39310052fc89d8eb96a445599a49a446883f57c5285fdad7cb97840`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 03 Jul 2025 07:12:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 03 Jul 2025 07:12:29 GMT
ENV EMQX_VERSION=5.8.7
# Thu, 03 Jul 2025 07:12:29 GMT
ENV AMD64_SHA256=a4ac9db115ab06e3d8dfdeefa71dbfb96ac039279e55df98575e14ba34ed2b1d
# Thu, 03 Jul 2025 07:12:29 GMT
ENV ARM64_SHA256=6efd454c0a0ef0d01ad22f804c91e4502287834de0f5cd3c70381daed43d398f
# Thu, 03 Jul 2025 07:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 03 Jul 2025 07:12:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
WORKDIR /opt/emqx
# Thu, 03 Jul 2025 07:12:29 GMT
USER emqx
# Thu, 03 Jul 2025 07:12:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 03 Jul 2025 07:12:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 03 Jul 2025 07:12:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 03 Jul 2025 07:12:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 03 Jul 2025 07:12:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0250921f7ab11be50266cb10738f072e37c42956edd9e3e9e34995893e4a9`  
		Last Modified: Wed, 13 Aug 2025 01:53:46 GMT  
		Size: 74.6 MB (74619092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2502a6b5926e0e9baed02a4f2c77acc1b086e4e5d13b521368b94485b22b14`  
		Last Modified: Wed, 13 Aug 2025 01:53:38 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:3406a1ecd76594eb194d546286f985c03fd504fafe77953b1be4dc1a1e6f808f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2754104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b091ada8ef738d5274e52a6c8783812ae611c5a156dc07537bb6b66b5cc066a`

```dockerfile
```

-	Layers:
	-	`sha256:a5d94c538902b9ba5f36e1ab178ec8d23f5194e1b49e1df4f7135fec0f0345a4`  
		Last Modified: Wed, 13 Aug 2025 02:27:21 GMT  
		Size: 2.7 MB (2741471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d4e1e4651e483833655d43d66d611d4e420a1983d081a3657d4e84fb27e049`  
		Last Modified: Wed, 13 Aug 2025 02:27:22 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
