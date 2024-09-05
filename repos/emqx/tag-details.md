<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.6`](#emqx516)
-	[`emqx:5.2`](#emqx52)
-	[`emqx:5.2.1`](#emqx521)
-	[`emqx:5.3`](#emqx53)
-	[`emqx:5.3.2`](#emqx532)
-	[`emqx:5.4`](#emqx54)
-	[`emqx:5.4.1`](#emqx541)
-	[`emqx:5.5`](#emqx55)
-	[`emqx:5.5.1`](#emqx551)
-	[`emqx:5.6`](#emqx56)
-	[`emqx:5.6.1`](#emqx561)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.0`](#emqx580)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:ff45a44441aefe8182dff4ac38ef5cef17023e819c93aac152ef42a0108e7ea9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

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

### `emqx:5` - unknown; unknown

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

### `emqx:5` - linux; arm64 variant v8

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

### `emqx:5` - unknown; unknown

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

## `emqx:5.1`

```console
$ docker pull emqx@sha256:10f05ae3c11244ee56c5413c1ceac77898dbef51c7323143d665e8508828df99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:e5675d81e7dc62c7e7ee8b43c1e19d0543efe55b6a8b48c81f6afd15c078a841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102401805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e8db48a11c88865acba9e2d917c51b9a7a65f7a44e70910f0f1e277413d813`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca37f1e9cc723f321890f328a7b262adec89234daea0ee8833b1a8551655325`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 3.0 MB (2987624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4693f3008874b0f6d7c0a29077f34011129bc6ec6dc7c7958aebc5f13127e1ea`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 4.0 KB (3988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b170406f66f01ab8998c93a9844cfd464c7b9dc7851150b964c6ac08a0c0c8`  
		Last Modified: Wed, 04 Sep 2024 23:08:02 GMT  
		Size: 68.0 MB (67980582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba398efd3d3648d6a9e16ddd633d869323fff692a3c568ee82ef3de1a9a5bc`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:2ac6a8b95c312d0d31ee04a41fe38000433000b26ede5a15d397b7b6a50e9805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112a47dcd6441e2adac33abb25dffb741a65e19477bab4c602d5c3d0867565`

```dockerfile
```

-	Layers:
	-	`sha256:bb5f3fb92df1ddd459ef8292ae5fa99a4e666f366cfaa104254af76dd24d2c9a`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 2.9 MB (2861668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96aca9b58601faf17f2400b4f4efef10a42642f794856843bb1c2568d5dc69a6`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 15.1 KB (15128 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fb2eea38f16dd90a51db5af6f89eab0386b0e504170e47dd8ce4ac572e9e6bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e213931ac85be667ec38232befc727b6c9b294d63b9093a208c4c9677a6e43`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6968dcc960eef68790cec519070afcea85494a8c94ccf4ce235a7b9cb79ce6`  
		Last Modified: Tue, 13 Aug 2024 06:51:57 GMT  
		Size: 3.0 MB (3003785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a13fa41b485c35ae128a8e8ecdf2985755432728ced2b7d172b43a8f6680ca`  
		Last Modified: Tue, 13 Aug 2024 06:51:56 GMT  
		Size: 4.0 KB (3994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13628ca158dc5ac9b4e7e509bafcc7ee936c565db5fd8a71bc1fb6947d11b3a`  
		Last Modified: Tue, 13 Aug 2024 06:51:59 GMT  
		Size: 59.6 MB (59620292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25019171c062c4e47f4de6252edaf2f0c492ab7f4d3f6d4d32b43bbe42ff2ad0`  
		Last Modified: Tue, 13 Aug 2024 06:51:57 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:58e7faf9b7c42017743ba88ef67e764fd3a1872b89744b865fbcd892d6aaa629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a160d1320d68d05ed203068f8fae506ae6da1c3d5b1765e75b6b33d7a8227829`

```dockerfile
```

-	Layers:
	-	`sha256:b09c8d69203469e86fbababf80ac4938699fa917b53db5c9979bc3a4b7275953`  
		Last Modified: Tue, 13 Aug 2024 06:51:57 GMT  
		Size: 2.9 MB (2861915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8b223911338430e8f825a3955c0ac7baa198f917532981ccea07ad7d99747f`  
		Last Modified: Tue, 13 Aug 2024 06:51:56 GMT  
		Size: 15.4 KB (15407 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:10f05ae3c11244ee56c5413c1ceac77898dbef51c7323143d665e8508828df99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:e5675d81e7dc62c7e7ee8b43c1e19d0543efe55b6a8b48c81f6afd15c078a841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102401805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e8db48a11c88865acba9e2d917c51b9a7a65f7a44e70910f0f1e277413d813`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca37f1e9cc723f321890f328a7b262adec89234daea0ee8833b1a8551655325`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 3.0 MB (2987624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4693f3008874b0f6d7c0a29077f34011129bc6ec6dc7c7958aebc5f13127e1ea`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 4.0 KB (3988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b170406f66f01ab8998c93a9844cfd464c7b9dc7851150b964c6ac08a0c0c8`  
		Last Modified: Wed, 04 Sep 2024 23:08:02 GMT  
		Size: 68.0 MB (67980582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba398efd3d3648d6a9e16ddd633d869323fff692a3c568ee82ef3de1a9a5bc`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 902.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:2ac6a8b95c312d0d31ee04a41fe38000433000b26ede5a15d397b7b6a50e9805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf112a47dcd6441e2adac33abb25dffb741a65e19477bab4c602d5c3d0867565`

```dockerfile
```

-	Layers:
	-	`sha256:bb5f3fb92df1ddd459ef8292ae5fa99a4e666f366cfaa104254af76dd24d2c9a`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 2.9 MB (2861668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96aca9b58601faf17f2400b4f4efef10a42642f794856843bb1c2568d5dc69a6`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 15.1 KB (15128 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fb2eea38f16dd90a51db5af6f89eab0386b0e504170e47dd8ce4ac572e9e6bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e213931ac85be667ec38232befc727b6c9b294d63b9093a208c4c9677a6e43`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6968dcc960eef68790cec519070afcea85494a8c94ccf4ce235a7b9cb79ce6`  
		Last Modified: Tue, 13 Aug 2024 06:51:57 GMT  
		Size: 3.0 MB (3003785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a13fa41b485c35ae128a8e8ecdf2985755432728ced2b7d172b43a8f6680ca`  
		Last Modified: Tue, 13 Aug 2024 06:51:56 GMT  
		Size: 4.0 KB (3994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13628ca158dc5ac9b4e7e509bafcc7ee936c565db5fd8a71bc1fb6947d11b3a`  
		Last Modified: Tue, 13 Aug 2024 06:51:59 GMT  
		Size: 59.6 MB (59620292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25019171c062c4e47f4de6252edaf2f0c492ab7f4d3f6d4d32b43bbe42ff2ad0`  
		Last Modified: Tue, 13 Aug 2024 06:51:57 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:58e7faf9b7c42017743ba88ef67e764fd3a1872b89744b865fbcd892d6aaa629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a160d1320d68d05ed203068f8fae506ae6da1c3d5b1765e75b6b33d7a8227829`

```dockerfile
```

-	Layers:
	-	`sha256:b09c8d69203469e86fbababf80ac4938699fa917b53db5c9979bc3a4b7275953`  
		Last Modified: Tue, 13 Aug 2024 06:51:57 GMT  
		Size: 2.9 MB (2861915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8b223911338430e8f825a3955c0ac7baa198f917532981ccea07ad7d99747f`  
		Last Modified: Tue, 13 Aug 2024 06:51:56 GMT  
		Size: 15.4 KB (15407 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2`

```console
$ docker pull emqx@sha256:b74c2169af1a0bb821fcf963408d1bccdd31925c7e9a81397e245763455e6a0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:cd02cafe1fabdc9a212348b1d8b48d2aef73532cfa7c5fb1d05604cc73f3789c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100956465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e473ae38622ad92e8af1c70a83756bdb90d309d8a00d3f399f88ad4ce738ac`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d0f23b8991c29c08f9b6be20b228b0c008d7f9929ed2ea50c11f6ee2b88d43`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 1.6 MB (1629043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e7233da3c82217d3cc8a25719db50203b8bf946b987e29dc289b785be4aa5b`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 4.0 KB (3986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f4c5d07db494f68df8e15c0ec993b27cb8580727fb1a40b5fb9c4838e08a15`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 67.9 MB (67893828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14efe86cd1a368733e83e888a7a3edcd149aee2c21b46dd687b5fad63098441`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:05dfed387ac6d4c0a23d2a023b4d6483f3f9021984fecf0822c88a021ca21f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c9a79367bb729d5a7de5725002ea248cd88906bc261de98813bd3c2f4af347`

```dockerfile
```

-	Layers:
	-	`sha256:af4969e7a0a367503711c27b59fd03a2b6fc8a11bfd34db1e8a93c3a91d503e7`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 2.8 MB (2805848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207be04582e135991d218ec42e1d9086cc0c3c09503c01f548b47dedef84779b`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:e4b210ca4403965cb2b6020c05771f478bc9f6a70bdb1cd8835b9c1160ae5f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91261912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f341cdca1e580e08ca5a245e915ea18dbe43ce0cd6a878fae7ce7123ca575b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54bf463a6d2d327c4038d35b6f2bce8f4aed0fac9481747ed139acd9033ebd9`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 1.6 MB (1643694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fde0cd803312434a3267581b6de3d573df1964001c65d657bc746ea2fc129db`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 4.0 KB (3997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1232f5cd8f11e5c7947366882b58dbc935e165216ff11cab61620babac9cc7`  
		Last Modified: Tue, 13 Aug 2024 06:52:35 GMT  
		Size: 59.5 MB (59537202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a76dd7aa304631df392da276cc8d63908dac2a27443761302690f5d88b460b5`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:76054097cede8901f639ddd9813e9449fe27bdd915b60092a1385c513d3dab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34272158cc1a62b74883eef66f505c5d23195b95efe69cfe73e04887e962fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:7e64183174bc1a732a2d83231458574c981cab276b08f83689f2c5b7a37faee0`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 2.8 MB (2806083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc51619d83df1d32b4e2c2668548c249eaadf0ccbb15b3341e6d593cb33cd1c4`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 15.9 KB (15909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:b74c2169af1a0bb821fcf963408d1bccdd31925c7e9a81397e245763455e6a0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:cd02cafe1fabdc9a212348b1d8b48d2aef73532cfa7c5fb1d05604cc73f3789c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (100956465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e473ae38622ad92e8af1c70a83756bdb90d309d8a00d3f399f88ad4ce738ac`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d0f23b8991c29c08f9b6be20b228b0c008d7f9929ed2ea50c11f6ee2b88d43`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 1.6 MB (1629043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e7233da3c82217d3cc8a25719db50203b8bf946b987e29dc289b785be4aa5b`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 4.0 KB (3986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f4c5d07db494f68df8e15c0ec993b27cb8580727fb1a40b5fb9c4838e08a15`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 67.9 MB (67893828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14efe86cd1a368733e83e888a7a3edcd149aee2c21b46dd687b5fad63098441`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:05dfed387ac6d4c0a23d2a023b4d6483f3f9021984fecf0822c88a021ca21f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c9a79367bb729d5a7de5725002ea248cd88906bc261de98813bd3c2f4af347`

```dockerfile
```

-	Layers:
	-	`sha256:af4969e7a0a367503711c27b59fd03a2b6fc8a11bfd34db1e8a93c3a91d503e7`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 2.8 MB (2805848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207be04582e135991d218ec42e1d9086cc0c3c09503c01f548b47dedef84779b`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 15.6 KB (15630 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:e4b210ca4403965cb2b6020c05771f478bc9f6a70bdb1cd8835b9c1160ae5f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91261912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f341cdca1e580e08ca5a245e915ea18dbe43ce0cd6a878fae7ce7123ca575b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54bf463a6d2d327c4038d35b6f2bce8f4aed0fac9481747ed139acd9033ebd9`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 1.6 MB (1643694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fde0cd803312434a3267581b6de3d573df1964001c65d657bc746ea2fc129db`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 4.0 KB (3997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1232f5cd8f11e5c7947366882b58dbc935e165216ff11cab61620babac9cc7`  
		Last Modified: Tue, 13 Aug 2024 06:52:35 GMT  
		Size: 59.5 MB (59537202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a76dd7aa304631df392da276cc8d63908dac2a27443761302690f5d88b460b5`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:76054097cede8901f639ddd9813e9449fe27bdd915b60092a1385c513d3dab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2821992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34272158cc1a62b74883eef66f505c5d23195b95efe69cfe73e04887e962fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:7e64183174bc1a732a2d83231458574c981cab276b08f83689f2c5b7a37faee0`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 2.8 MB (2806083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc51619d83df1d32b4e2c2668548c249eaadf0ccbb15b3341e6d593cb33cd1c4`  
		Last Modified: Tue, 13 Aug 2024 06:52:33 GMT  
		Size: 15.9 KB (15909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3`

```console
$ docker pull emqx@sha256:cb888ffa65e13d34c2834b98100533c368dd48eb9c1a7ae2206deacf3c193baa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:ee0b5806d868e36f9be87ea00856b24c5d8f6cc57f8c288058728fb7640e6c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101789115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c427e0b86e0044ae54109d5f2d021917f663ced17d6beebfb54fa239087493f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4512e4239a49ecda1e60a2ebcd7460155abd3d727d71380777bebfdf30aa5946`  
		Last Modified: Wed, 04 Sep 2024 23:07:50 GMT  
		Size: 70.4 MB (70359507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef3123eda05e695d4af464c0c60d52b4b0dcea3fd036ae9b644753fe930dd73`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:cf6b3f1b2a868116d29be66d9846a6e58ce15e688bba4d3f32e60a792edfbceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7369b22804afc81bb1f65a1140dc1d132ce3d7817eecdf516d9c87c3037960eb`

```dockerfile
```

-	Layers:
	-	`sha256:4d0db09bb1a5b05f56d7f63ed6d86518c69f3bbb1da81159415d823136dbb598`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 2.8 MB (2817191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1161b9014e49632e01e3e6d05be7d71f24bc31b55392c82ea7e2597025833eb8`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:af11d02647eb6c82e390e19b21d0afe51093e285b188c5cc9766385d4aad80c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92087757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e3698dd3d7017221df57a71971c3212459a15750125b961cbdda0533ccdbcf`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff531037b4c354100d8ee6f9ac6ca377cfd662a5b9cfe8d212454f0d8ba5819`  
		Last Modified: Tue, 13 Aug 2024 06:53:08 GMT  
		Size: 62.0 MB (62010738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b5d2eee69ff12ac612a9911e712717334a118de93fd9039cd4ff4f29b159e`  
		Last Modified: Tue, 13 Aug 2024 06:53:06 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:ed6a8f2622fa44097a4292d8505b9d48741cc6fa55fecc3af218fe8143c1a0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d9378e2a2efae428ae47a5ea0c848c3ab74623906cc43790fbf4f86ef26c18`

```dockerfile
```

-	Layers:
	-	`sha256:e157603af112f97de444a2a029aac234420fd79021df3a772e335089e355eacf`  
		Last Modified: Tue, 13 Aug 2024 06:53:07 GMT  
		Size: 2.8 MB (2817426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ba46e2a43d6b4a5819da64eb98c1624f7f1f535e5315e5d4df58c7f20b5e8d`  
		Last Modified: Tue, 13 Aug 2024 06:53:06 GMT  
		Size: 12.8 KB (12837 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:cb888ffa65e13d34c2834b98100533c368dd48eb9c1a7ae2206deacf3c193baa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:ee0b5806d868e36f9be87ea00856b24c5d8f6cc57f8c288058728fb7640e6c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101789115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c427e0b86e0044ae54109d5f2d021917f663ced17d6beebfb54fa239087493f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4512e4239a49ecda1e60a2ebcd7460155abd3d727d71380777bebfdf30aa5946`  
		Last Modified: Wed, 04 Sep 2024 23:07:50 GMT  
		Size: 70.4 MB (70359507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef3123eda05e695d4af464c0c60d52b4b0dcea3fd036ae9b644753fe930dd73`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:cf6b3f1b2a868116d29be66d9846a6e58ce15e688bba4d3f32e60a792edfbceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7369b22804afc81bb1f65a1140dc1d132ce3d7817eecdf516d9c87c3037960eb`

```dockerfile
```

-	Layers:
	-	`sha256:4d0db09bb1a5b05f56d7f63ed6d86518c69f3bbb1da81159415d823136dbb598`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 2.8 MB (2817191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1161b9014e49632e01e3e6d05be7d71f24bc31b55392c82ea7e2597025833eb8`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:af11d02647eb6c82e390e19b21d0afe51093e285b188c5cc9766385d4aad80c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92087757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e3698dd3d7017221df57a71971c3212459a15750125b961cbdda0533ccdbcf`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff531037b4c354100d8ee6f9ac6ca377cfd662a5b9cfe8d212454f0d8ba5819`  
		Last Modified: Tue, 13 Aug 2024 06:53:08 GMT  
		Size: 62.0 MB (62010738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b5d2eee69ff12ac612a9911e712717334a118de93fd9039cd4ff4f29b159e`  
		Last Modified: Tue, 13 Aug 2024 06:53:06 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:ed6a8f2622fa44097a4292d8505b9d48741cc6fa55fecc3af218fe8143c1a0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2830263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d9378e2a2efae428ae47a5ea0c848c3ab74623906cc43790fbf4f86ef26c18`

```dockerfile
```

-	Layers:
	-	`sha256:e157603af112f97de444a2a029aac234420fd79021df3a772e335089e355eacf`  
		Last Modified: Tue, 13 Aug 2024 06:53:07 GMT  
		Size: 2.8 MB (2817426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ba46e2a43d6b4a5819da64eb98c1624f7f1f535e5315e5d4df58c7f20b5e8d`  
		Last Modified: Tue, 13 Aug 2024 06:53:06 GMT  
		Size: 12.8 KB (12837 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4`

```console
$ docker pull emqx@sha256:f53995718831dbd03cdbc1fd22d76d4be7ebe3d38f52ba6ee96bcb6cdf9073ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:f49989e401de49b8a8438ff5ff4d2a5089f4374b89f41c77c3b0621c62c86b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118702856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5006554af5f328d6525c82115057fe31f18b2fda1e50d8bb41be99ad1c474015`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389d2e1de38154ea407258526621bb88b72f723848e5960f58534dd577d77f71`  
		Last Modified: Wed, 04 Sep 2024 23:09:07 GMT  
		Size: 87.3 MB (87273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cccf681833c762015adf0bc9a6a6f493d03c797add7a7a48e96cf0feb5011d7`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:0883f9a4e6321f76eeb031308acaaaee8f040979cbb3614f56f0f7937f9aa94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4261956643a598417e33fd16f8c81d2ceb34449842dfa96411357afb00e86798`

```dockerfile
```

-	Layers:
	-	`sha256:28e4730c4829b067115fbe15c95ede6893b2a4dde17edb66cba62bba77345a91`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 2.8 MB (2810516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01731282cab00d8c52d012f4ff1bce0b8b871b41bb7a34d890a576d98fe7e59d`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 12.5 KB (12503 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f41e3a98778246b646046d8db0f90a9b1ad43d476079a1453bc44f20d855b283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108486024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365097500b21073d2594bcdcdf9749806719a782cd357d90be86c00f0cacd7e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125acff6b73bc58a5d0dd12844d633401b05b2dc65a32c78be112765af4e8cc1`  
		Last Modified: Tue, 13 Aug 2024 06:53:47 GMT  
		Size: 78.4 MB (78409004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d44abafc8af2b2ca986ccc781140edc8eb24bf40897500af0d60754e3f1b96`  
		Last Modified: Tue, 13 Aug 2024 06:53:45 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:17c44d069faf21ba52db481ced79189729614941a9ad7fbe637093826a0e4510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e1124f5df879109ba0acf786b728c4d54e6daa158e5f093f9c65c15824e08e`

```dockerfile
```

-	Layers:
	-	`sha256:d9961f93e1edb8ae3603b9885a92422be0f2648c009fbccef8e00c112549a7c9`  
		Last Modified: Tue, 13 Aug 2024 06:53:45 GMT  
		Size: 2.8 MB (2810751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0334068b96a160dee08b64c8ddbf2f2a8b8b4b2c4b3d4515f2af8e0032a3477c`  
		Last Modified: Tue, 13 Aug 2024 06:53:45 GMT  
		Size: 12.8 KB (12781 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:f53995718831dbd03cdbc1fd22d76d4be7ebe3d38f52ba6ee96bcb6cdf9073ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:f49989e401de49b8a8438ff5ff4d2a5089f4374b89f41c77c3b0621c62c86b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118702856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5006554af5f328d6525c82115057fe31f18b2fda1e50d8bb41be99ad1c474015`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389d2e1de38154ea407258526621bb88b72f723848e5960f58534dd577d77f71`  
		Last Modified: Wed, 04 Sep 2024 23:09:07 GMT  
		Size: 87.3 MB (87273248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cccf681833c762015adf0bc9a6a6f493d03c797add7a7a48e96cf0feb5011d7`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:0883f9a4e6321f76eeb031308acaaaee8f040979cbb3614f56f0f7937f9aa94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4261956643a598417e33fd16f8c81d2ceb34449842dfa96411357afb00e86798`

```dockerfile
```

-	Layers:
	-	`sha256:28e4730c4829b067115fbe15c95ede6893b2a4dde17edb66cba62bba77345a91`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 2.8 MB (2810516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01731282cab00d8c52d012f4ff1bce0b8b871b41bb7a34d890a576d98fe7e59d`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 12.5 KB (12503 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f41e3a98778246b646046d8db0f90a9b1ad43d476079a1453bc44f20d855b283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108486024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365097500b21073d2594bcdcdf9749806719a782cd357d90be86c00f0cacd7e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125acff6b73bc58a5d0dd12844d633401b05b2dc65a32c78be112765af4e8cc1`  
		Last Modified: Tue, 13 Aug 2024 06:53:47 GMT  
		Size: 78.4 MB (78409004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d44abafc8af2b2ca986ccc781140edc8eb24bf40897500af0d60754e3f1b96`  
		Last Modified: Tue, 13 Aug 2024 06:53:45 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:17c44d069faf21ba52db481ced79189729614941a9ad7fbe637093826a0e4510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e1124f5df879109ba0acf786b728c4d54e6daa158e5f093f9c65c15824e08e`

```dockerfile
```

-	Layers:
	-	`sha256:d9961f93e1edb8ae3603b9885a92422be0f2648c009fbccef8e00c112549a7c9`  
		Last Modified: Tue, 13 Aug 2024 06:53:45 GMT  
		Size: 2.8 MB (2810751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0334068b96a160dee08b64c8ddbf2f2a8b8b4b2c4b3d4515f2af8e0032a3477c`  
		Last Modified: Tue, 13 Aug 2024 06:53:45 GMT  
		Size: 12.8 KB (12781 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5`

```console
$ docker pull emqx@sha256:793fccd6196f94d2c0042200761fba10ea8d0d8c8aec5aecd154d3c2d8412149
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:07c2869522379e6857c9b5700b94edbcae4ffee710e119380f83223e8c02dc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155cecef612ea6d727d1d59a167ad450a023073577be6f9549f67a6cde8a72d4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fb12e487eb0ea40e0d42a8e8c1b533977c5575285aa164bb60fbe5f48aacd3`  
		Last Modified: Wed, 04 Sep 2024 23:08:59 GMT  
		Size: 89.8 MB (89839224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d46e79d16d8277f8e5c27836bdba36ba08534dd34b114c83c3963eb05b3628`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:567cf88cdb8786872959bf838da120b62517b2da7d3d1d1a709f2668db6cd54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9caa0b2a8aed2b6027e798c78094a4be1539f861cb5859b7e093c7cc575fe5d`

```dockerfile
```

-	Layers:
	-	`sha256:c9269ae10936e726f16233f69d57c6dbb4c9192f5c7630f7fcd709b898db4f76`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 2.8 MB (2810477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76b042abaa449b7fe1a5837511a5f1a776d1643c4b7a95e237576b5d7ad1bf`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 12.6 KB (12604 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0d0df4e0647a5ceeeaa72544b8fe09626d268b0d6596f1c2f8306a20ab572704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116784415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53a35f2af8433afe7f016979230400fe688c7fcc1261a99e978a5487bc73ab6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3745f0fe383266f4058e8079b053ab3a4c14967e6db03c48624b9a0c83a4f5ed`  
		Last Modified: Tue, 13 Aug 2024 06:54:26 GMT  
		Size: 86.7 MB (86707268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7d9f77ddb0b20a411e52491fe7a1c3ef97fd0ee65177b4373baee003d3fc4b`  
		Last Modified: Tue, 13 Aug 2024 06:54:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:1b05c9ae101593ea252ec0c7431539c28215467143f135cc74dd20bdc4d8876a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167777dae47d1f41d4dd790d92211bffe11e6effa2d5fefced369e5adb5440f`

```dockerfile
```

-	Layers:
	-	`sha256:03b151e4528fc87fd6f7bbc9ea4fbacd96f67eae76c94e2b5f0421aaa8c3637c`  
		Last Modified: Tue, 13 Aug 2024 06:54:24 GMT  
		Size: 2.8 MB (2810712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c129a2ca78910a62e965f2a1f9b49993dde7a671fdfc7b81917096ea70294f35`  
		Last Modified: Tue, 13 Aug 2024 06:54:24 GMT  
		Size: 12.9 KB (12884 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:793fccd6196f94d2c0042200761fba10ea8d0d8c8aec5aecd154d3c2d8412149
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:07c2869522379e6857c9b5700b94edbcae4ffee710e119380f83223e8c02dc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155cecef612ea6d727d1d59a167ad450a023073577be6f9549f67a6cde8a72d4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fb12e487eb0ea40e0d42a8e8c1b533977c5575285aa164bb60fbe5f48aacd3`  
		Last Modified: Wed, 04 Sep 2024 23:08:59 GMT  
		Size: 89.8 MB (89839224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d46e79d16d8277f8e5c27836bdba36ba08534dd34b114c83c3963eb05b3628`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:567cf88cdb8786872959bf838da120b62517b2da7d3d1d1a709f2668db6cd54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9caa0b2a8aed2b6027e798c78094a4be1539f861cb5859b7e093c7cc575fe5d`

```dockerfile
```

-	Layers:
	-	`sha256:c9269ae10936e726f16233f69d57c6dbb4c9192f5c7630f7fcd709b898db4f76`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 2.8 MB (2810477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76b042abaa449b7fe1a5837511a5f1a776d1643c4b7a95e237576b5d7ad1bf`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 12.6 KB (12604 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0d0df4e0647a5ceeeaa72544b8fe09626d268b0d6596f1c2f8306a20ab572704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116784415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53a35f2af8433afe7f016979230400fe688c7fcc1261a99e978a5487bc73ab6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3745f0fe383266f4058e8079b053ab3a4c14967e6db03c48624b9a0c83a4f5ed`  
		Last Modified: Tue, 13 Aug 2024 06:54:26 GMT  
		Size: 86.7 MB (86707268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7d9f77ddb0b20a411e52491fe7a1c3ef97fd0ee65177b4373baee003d3fc4b`  
		Last Modified: Tue, 13 Aug 2024 06:54:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:1b05c9ae101593ea252ec0c7431539c28215467143f135cc74dd20bdc4d8876a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2823596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4167777dae47d1f41d4dd790d92211bffe11e6effa2d5fefced369e5adb5440f`

```dockerfile
```

-	Layers:
	-	`sha256:03b151e4528fc87fd6f7bbc9ea4fbacd96f67eae76c94e2b5f0421aaa8c3637c`  
		Last Modified: Tue, 13 Aug 2024 06:54:24 GMT  
		Size: 2.8 MB (2810712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c129a2ca78910a62e965f2a1f9b49993dde7a671fdfc7b81917096ea70294f35`  
		Last Modified: Tue, 13 Aug 2024 06:54:24 GMT  
		Size: 12.9 KB (12884 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6`

```console
$ docker pull emqx@sha256:d420973bdd79a7af285a5e625ffc94615b43dc5757651e3156aa51deca56676b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:75bb9fa5888941cf6e6c58f2ee9c9419e49cfc0065d761aa0be016f8bbf9411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124182356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a72726d2d1880d90c27c1f41971c4a2163c6c929759d92090be174335f960af`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256e7cc898007d8852022e148e8a621054a4f76dfe00a3afee7b29601cb06f19`  
		Last Modified: Wed, 04 Sep 2024 23:08:59 GMT  
		Size: 95.1 MB (95054809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5829716e0561c4cc8c11f0d5be94afb2ffa0f27492e3c5668f800f50952ef91b`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:5e26a96481b5816c72ce71f372e28ac1176f72f7763abf7225ed49ec064e33ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a659686ea496bee4f505363e1765838de112992745dfe11cd3782bfbf38aaddf`

```dockerfile
```

-	Layers:
	-	`sha256:6a274512684fa001aa0d4d2e6d2f8ff7328434348bca22999ab1afb9a885e279`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 2.6 MB (2591425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18341b26f4aa53c07e203e3e8893f98656ad3b6edcd58e5d83af4900ae5de489`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 11.7 KB (11727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:738a1e7e23fa8559a0c39acaa0277cfc004e2d6e07d5d6c478fad9761fe667dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120774798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d746ea1758b0fac5ec6f92bf80f8eb11efa2648e21e5427b35ec746bbb78860a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2f2ad5a1ac31ae14dd64a5abf2649297a7a28f15e8e61250f8708af86004b1`  
		Last Modified: Tue, 13 Aug 2024 06:55:09 GMT  
		Size: 91.6 MB (91617209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56420d17b613f26c0ab6b6a32b239fa28c3ce8e425fb2320342e452af95fa70`  
		Last Modified: Tue, 13 Aug 2024 06:55:06 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:984955444270d80221c2488208cdd61d0ee3182fb324bd7416d55b2bafe97325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12b5fd2d1fab55faa60177751d6360768b8167359dbb8d96f1adfa703a14b5f`

```dockerfile
```

-	Layers:
	-	`sha256:438c74e418987f2923bcc20969389b1250abc6388867b4fc932ca13a1098de6a`  
		Last Modified: Tue, 13 Aug 2024 06:55:06 GMT  
		Size: 2.6 MB (2591680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ad49580719ea9af4e77d4042fe2f9aa3f51800f67ffd0493143c6e8f68ef35`  
		Last Modified: Tue, 13 Aug 2024 06:55:06 GMT  
		Size: 12.0 KB (12006 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:d420973bdd79a7af285a5e625ffc94615b43dc5757651e3156aa51deca56676b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:75bb9fa5888941cf6e6c58f2ee9c9419e49cfc0065d761aa0be016f8bbf9411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124182356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a72726d2d1880d90c27c1f41971c4a2163c6c929759d92090be174335f960af`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256e7cc898007d8852022e148e8a621054a4f76dfe00a3afee7b29601cb06f19`  
		Last Modified: Wed, 04 Sep 2024 23:08:59 GMT  
		Size: 95.1 MB (95054809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5829716e0561c4cc8c11f0d5be94afb2ffa0f27492e3c5668f800f50952ef91b`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:5e26a96481b5816c72ce71f372e28ac1176f72f7763abf7225ed49ec064e33ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a659686ea496bee4f505363e1765838de112992745dfe11cd3782bfbf38aaddf`

```dockerfile
```

-	Layers:
	-	`sha256:6a274512684fa001aa0d4d2e6d2f8ff7328434348bca22999ab1afb9a885e279`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 2.6 MB (2591425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18341b26f4aa53c07e203e3e8893f98656ad3b6edcd58e5d83af4900ae5de489`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 11.7 KB (11727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:738a1e7e23fa8559a0c39acaa0277cfc004e2d6e07d5d6c478fad9761fe667dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120774798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d746ea1758b0fac5ec6f92bf80f8eb11efa2648e21e5427b35ec746bbb78860a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2f2ad5a1ac31ae14dd64a5abf2649297a7a28f15e8e61250f8708af86004b1`  
		Last Modified: Tue, 13 Aug 2024 06:55:09 GMT  
		Size: 91.6 MB (91617209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56420d17b613f26c0ab6b6a32b239fa28c3ce8e425fb2320342e452af95fa70`  
		Last Modified: Tue, 13 Aug 2024 06:55:06 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:984955444270d80221c2488208cdd61d0ee3182fb324bd7416d55b2bafe97325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12b5fd2d1fab55faa60177751d6360768b8167359dbb8d96f1adfa703a14b5f`

```dockerfile
```

-	Layers:
	-	`sha256:438c74e418987f2923bcc20969389b1250abc6388867b4fc932ca13a1098de6a`  
		Last Modified: Tue, 13 Aug 2024 06:55:06 GMT  
		Size: 2.6 MB (2591680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ad49580719ea9af4e77d4042fe2f9aa3f51800f67ffd0493143c6e8f68ef35`  
		Last Modified: Tue, 13 Aug 2024 06:55:06 GMT  
		Size: 12.0 KB (12006 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:60821f8f379b06f6da608aae59e48fb7acc88f39e318ff006ed9d542d0176eba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:675c242de82b1b7a5e4c82c8d7d97cebdbe2a2e576c6d883969a8ca790c7647b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126274631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b1d95f3e1098f01d845fa49918d215649507ea8e646fd15952fa0470bd3124`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
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
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582fb5cea98f2ce948fd31f7a40ccbbb31d1d7539864fc547bf374298cee90f`  
		Last Modified: Wed, 04 Sep 2024 23:09:54 GMT  
		Size: 97.1 MB (97147083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a185cb435c88bcbdb91251360a81bf109c3536afd1d7329ad09ffdb0c3138bb`  
		Last Modified: Wed, 04 Sep 2024 23:09:53 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:7f836714058b0091936e45f50c355dbd0be6e53828f73a4e95d4e6a1be6ceb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2610906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762258c8d72771018459614b12216b522a198246a854d2aad0a6fc0bb975289e`

```dockerfile
```

-	Layers:
	-	`sha256:c0c23657de1a750ad777a1dda26488e9923bd7ce74f55e187cea626789d308ae`  
		Last Modified: Wed, 04 Sep 2024 23:09:53 GMT  
		Size: 2.6 MB (2599179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7665dce532ee002440fd7aa3a13fded5703c6f9aee5c1ed8ee6fe34bf56edaf`  
		Last Modified: Wed, 04 Sep 2024 23:09:53 GMT  
		Size: 11.7 KB (11727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:881e9fadbc0db50f51fb324cb3a192fbe9cc2625ae5e1f8239b32573329699f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122852517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ae313d42002ff80fe4a2f76247ac4289fbebcb7f0ecdf65474e6482b751b67`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e41154c687fd0aa501f237c963af962e1a6c6e1e8571484f590a01c9f5cdbf`  
		Last Modified: Tue, 13 Aug 2024 06:55:49 GMT  
		Size: 93.7 MB (93694928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0a5d0dfda0372ce455aa2184bccfcc550572063012afb92fd33b21f2ff1224`  
		Last Modified: Tue, 13 Aug 2024 06:55:47 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:3cb017ff7aad805427939a983555718d6216aca58e4a99279e845da71d15b2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf87cfd70112087d151719465e4883540833494ef53dc4c94ddc4aa1a9b1477`

```dockerfile
```

-	Layers:
	-	`sha256:99f1b23d84a7cc4367b2a399429f89e1f6a0ed69a0dd0b3678a34453accac364`  
		Last Modified: Tue, 13 Aug 2024 06:55:47 GMT  
		Size: 2.6 MB (2600036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10da3e7dc8ca8780a00a53d7ba6dd420ce9c6d55bd78fc54b6ab3d1e4cb87597`  
		Last Modified: Tue, 13 Aug 2024 06:55:47 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:60821f8f379b06f6da608aae59e48fb7acc88f39e318ff006ed9d542d0176eba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:675c242de82b1b7a5e4c82c8d7d97cebdbe2a2e576c6d883969a8ca790c7647b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126274631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b1d95f3e1098f01d845fa49918d215649507ea8e646fd15952fa0470bd3124`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
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
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582fb5cea98f2ce948fd31f7a40ccbbb31d1d7539864fc547bf374298cee90f`  
		Last Modified: Wed, 04 Sep 2024 23:09:54 GMT  
		Size: 97.1 MB (97147083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a185cb435c88bcbdb91251360a81bf109c3536afd1d7329ad09ffdb0c3138bb`  
		Last Modified: Wed, 04 Sep 2024 23:09:53 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:7f836714058b0091936e45f50c355dbd0be6e53828f73a4e95d4e6a1be6ceb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2610906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762258c8d72771018459614b12216b522a198246a854d2aad0a6fc0bb975289e`

```dockerfile
```

-	Layers:
	-	`sha256:c0c23657de1a750ad777a1dda26488e9923bd7ce74f55e187cea626789d308ae`  
		Last Modified: Wed, 04 Sep 2024 23:09:53 GMT  
		Size: 2.6 MB (2599179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7665dce532ee002440fd7aa3a13fded5703c6f9aee5c1ed8ee6fe34bf56edaf`  
		Last Modified: Wed, 04 Sep 2024 23:09:53 GMT  
		Size: 11.7 KB (11727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:881e9fadbc0db50f51fb324cb3a192fbe9cc2625ae5e1f8239b32573329699f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122852517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ae313d42002ff80fe4a2f76247ac4289fbebcb7f0ecdf65474e6482b751b67`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e41154c687fd0aa501f237c963af962e1a6c6e1e8571484f590a01c9f5cdbf`  
		Last Modified: Tue, 13 Aug 2024 06:55:49 GMT  
		Size: 93.7 MB (93694928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0a5d0dfda0372ce455aa2184bccfcc550572063012afb92fd33b21f2ff1224`  
		Last Modified: Tue, 13 Aug 2024 06:55:47 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:3cb017ff7aad805427939a983555718d6216aca58e4a99279e845da71d15b2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf87cfd70112087d151719465e4883540833494ef53dc4c94ddc4aa1a9b1477`

```dockerfile
```

-	Layers:
	-	`sha256:99f1b23d84a7cc4367b2a399429f89e1f6a0ed69a0dd0b3678a34453accac364`  
		Last Modified: Tue, 13 Aug 2024 06:55:47 GMT  
		Size: 2.6 MB (2600036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10da3e7dc8ca8780a00a53d7ba6dd420ce9c6d55bd78fc54b6ab3d1e4cb87597`  
		Last Modified: Tue, 13 Aug 2024 06:55:47 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:ff45a44441aefe8182dff4ac38ef5cef17023e819c93aac152ef42a0108e7ea9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

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

### `emqx:5.8` - unknown; unknown

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

### `emqx:5.8` - linux; arm64 variant v8

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

### `emqx:5.8` - unknown; unknown

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

## `emqx:5.8.0`

```console
$ docker pull emqx@sha256:ff45a44441aefe8182dff4ac38ef5cef17023e819c93aac152ef42a0108e7ea9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.0` - linux; amd64

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

### `emqx:5.8.0` - unknown; unknown

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

### `emqx:5.8.0` - linux; arm64 variant v8

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

### `emqx:5.8.0` - unknown; unknown

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
