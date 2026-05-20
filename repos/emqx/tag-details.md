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
$ docker pull emqx@sha256:037db7e735a795d92b943ed9213d19b76cbc484e3faea4e1508cc79452dae8a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:4f6bad906895f2cefba3480bf5c53826f24530873a94e18e0eccea22cbd5955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108406053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b1ebbbe051ea04e35c094a95670c05ad219a6451eb4b411415d8dfedddf41b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:46 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 19 May 2026 22:58:46 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 19 May 2026 22:58:46 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 19 May 2026 22:58:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:58:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:58:46 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:58:46 GMT
USER emqx
# Tue, 19 May 2026 22:58:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:58:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:58:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:58:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488dcea6725f9302e215530c31927d7f86591528625bf1f3a949440b9515f89f`  
		Last Modified: Tue, 19 May 2026 22:59:00 GMT  
		Size: 78.6 MB (78625065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e4901702235f6109a1332f77a15b3ba204a9d5a21ffe0164bc326edc684f39`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:84b4aaede4492c0f385dd4277c9132c58c88d11f62bb8a58fd66b1f9079b89bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07d6fef08a881213bdc3b4c8febe547c090bcb26a7e8666b9ae742e6863c8a5`

```dockerfile
```

-	Layers:
	-	`sha256:fba577b3f04ff5dfe3ad4c45fb639fb8f05da9880384d559ff6c874fb30b6efc`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 2.4 MB (2403579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a733767c3522fffff4204e2687ecce87f9df0e2ff60ec0fefc189fca92701ed3`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 12.5 KB (12485 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0d2c49808220103e223773f07b8c9f451b4e3d6cd05c798edcb5aea1f4b719f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106675729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796be0a9911cdab54ed7517797017e42e2637b270897acd1f3d6daeb399070d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:56:09 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 19 May 2026 22:56:09 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 19 May 2026 22:56:09 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 19 May 2026 22:56:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:56:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:56:09 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:56:09 GMT
USER emqx
# Tue, 19 May 2026 22:56:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:56:09 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:56:09 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:56:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:56:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50319fd60744bc1658c14ef4726d7cc07e1ddadeb4561a9ec5a625f6471cab41`  
		Last Modified: Tue, 19 May 2026 22:56:25 GMT  
		Size: 76.5 MB (76532746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ca3ed1a35d0c2678fe53911c5faa117b7d50e4f5f86f7d78345ca8ff14721`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:465c5a77f0800b1b0050da15c1935023364d3a1c1f2bcdb982fef5dd14df951a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b251c0d042bc2e4d758e2ba3a94a70abbfd6fd1c83134b06684dd23c7ce605a`

```dockerfile
```

-	Layers:
	-	`sha256:441c627f67f3609a65cb74b13a4c54b34d395925bd2160c92ca8fa9c51dd1e88`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 2.4 MB (2403860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8cacf7129222937f3ee7287585271752a0c1c6a820fe7a6f2c0f49f5fb6646f`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:9cb0a92400a413aa978b2d229c59ba2c6ad6647c34b1046bdd1e643c37afa9a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:ec9e4517b59e47339890857b18b8a61f110ac39704f8b44b611af21781f90ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125391989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c87173acaab38c8583af6d9cc2f51c0fa22212e80b4de80e57b72bf3f8a6161`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:58:35 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 19 May 2026 22:58:35 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 19 May 2026 22:58:35 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 19 May 2026 22:58:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:58:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:58:35 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:58:35 GMT
USER emqx
# Tue, 19 May 2026 22:58:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:58:35 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:58:35 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:58:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:35 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bfc5f862d590e0c2be4578649ae83bc5bc734553d64594a03f59a42f861baf`  
		Last Modified: Tue, 19 May 2026 22:58:52 GMT  
		Size: 97.2 MB (97157382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c4d0e7002927f465400599828cdfae9fde77d330f7dcd4bfa4304c587cbab1`  
		Last Modified: Tue, 19 May 2026 22:58:50 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:6d0d6127f92a19c68a4adfdbe747a9476521a052081486975352ecde7acc0a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2812700db6f489d921b847edace36f9319564f2548578801333cb2f13fd07138`

```dockerfile
```

-	Layers:
	-	`sha256:3063d89a3dec6a2139b6be82265876e79cfae42118aae05fa6261b47501beb2a`  
		Last Modified: Tue, 19 May 2026 22:58:50 GMT  
		Size: 2.8 MB (2751416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190faa5f35d7f6e7ea214f49fd56b1b77817d214131a3dbd0a2a61ba46a9c379`  
		Last Modified: Tue, 19 May 2026 22:58:50 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6e55aaf2bddfea4cf06328ac9f93f063cc52bcb77a82e417e058c4a46f8719a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121835448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85775491bd54d54e33d393fc7ef305a09fdba198c63fb05c06198ca5e2ac825`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:56:09 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 19 May 2026 22:56:09 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 19 May 2026 22:56:09 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 19 May 2026 22:56:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:56:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:56:09 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:56:09 GMT
USER emqx
# Tue, 19 May 2026 22:56:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:56:09 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:56:09 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:56:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:56:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a46820df8fee89d1c43d2cb0f5640c3f708ed450e279c142b3d4a616bcc7318`  
		Last Modified: Tue, 19 May 2026 22:56:26 GMT  
		Size: 93.7 MB (93719341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e14b25e48ae4cf407329e108562157ce7318badba56bb5447b5fbae72ba694`  
		Last Modified: Tue, 19 May 2026 22:56:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:421f8fe55845c0663701557ae50d1dc59fe5970849c5cbb3daa0c95a268da6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329f6aa279c9d60f63f216e8d768094e734615398ce68e09116327142a957751`

```dockerfile
```

-	Layers:
	-	`sha256:ea4b333fb4da6bc7c70269c9b83492796def6a8117e49c9fb3cc2f7f1473e8cc`  
		Last Modified: Tue, 19 May 2026 22:56:24 GMT  
		Size: 2.8 MB (2751672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4333c5d9b5037b0592962fcefe2e9e49ebabd11b81096e73a2a1d103107b1f2c`  
		Last Modified: Tue, 19 May 2026 22:56:23 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:9cb0a92400a413aa978b2d229c59ba2c6ad6647c34b1046bdd1e643c37afa9a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:ec9e4517b59e47339890857b18b8a61f110ac39704f8b44b611af21781f90ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125391989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c87173acaab38c8583af6d9cc2f51c0fa22212e80b4de80e57b72bf3f8a6161`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:58:35 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 19 May 2026 22:58:35 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 19 May 2026 22:58:35 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 19 May 2026 22:58:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:58:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:58:35 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:58:35 GMT
USER emqx
# Tue, 19 May 2026 22:58:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:58:35 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:58:35 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:58:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:35 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bfc5f862d590e0c2be4578649ae83bc5bc734553d64594a03f59a42f861baf`  
		Last Modified: Tue, 19 May 2026 22:58:52 GMT  
		Size: 97.2 MB (97157382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c4d0e7002927f465400599828cdfae9fde77d330f7dcd4bfa4304c587cbab1`  
		Last Modified: Tue, 19 May 2026 22:58:50 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:6d0d6127f92a19c68a4adfdbe747a9476521a052081486975352ecde7acc0a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2812700db6f489d921b847edace36f9319564f2548578801333cb2f13fd07138`

```dockerfile
```

-	Layers:
	-	`sha256:3063d89a3dec6a2139b6be82265876e79cfae42118aae05fa6261b47501beb2a`  
		Last Modified: Tue, 19 May 2026 22:58:50 GMT  
		Size: 2.8 MB (2751416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190faa5f35d7f6e7ea214f49fd56b1b77817d214131a3dbd0a2a61ba46a9c379`  
		Last Modified: Tue, 19 May 2026 22:58:50 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6e55aaf2bddfea4cf06328ac9f93f063cc52bcb77a82e417e058c4a46f8719a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121835448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85775491bd54d54e33d393fc7ef305a09fdba198c63fb05c06198ca5e2ac825`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:56:09 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 19 May 2026 22:56:09 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 19 May 2026 22:56:09 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 19 May 2026 22:56:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:56:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:56:09 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:56:09 GMT
USER emqx
# Tue, 19 May 2026 22:56:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:56:09 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:56:09 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:56:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:56:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a46820df8fee89d1c43d2cb0f5640c3f708ed450e279c142b3d4a616bcc7318`  
		Last Modified: Tue, 19 May 2026 22:56:26 GMT  
		Size: 93.7 MB (93719341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e14b25e48ae4cf407329e108562157ce7318badba56bb5447b5fbae72ba694`  
		Last Modified: Tue, 19 May 2026 22:56:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:421f8fe55845c0663701557ae50d1dc59fe5970849c5cbb3daa0c95a268da6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329f6aa279c9d60f63f216e8d768094e734615398ce68e09116327142a957751`

```dockerfile
```

-	Layers:
	-	`sha256:ea4b333fb4da6bc7c70269c9b83492796def6a8117e49c9fb3cc2f7f1473e8cc`  
		Last Modified: Tue, 19 May 2026 22:56:24 GMT  
		Size: 2.8 MB (2751672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4333c5d9b5037b0592962fcefe2e9e49ebabd11b81096e73a2a1d103107b1f2c`  
		Last Modified: Tue, 19 May 2026 22:56:23 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:037db7e735a795d92b943ed9213d19b76cbc484e3faea4e1508cc79452dae8a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:4f6bad906895f2cefba3480bf5c53826f24530873a94e18e0eccea22cbd5955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108406053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b1ebbbe051ea04e35c094a95670c05ad219a6451eb4b411415d8dfedddf41b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:46 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 19 May 2026 22:58:46 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 19 May 2026 22:58:46 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 19 May 2026 22:58:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:58:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:58:46 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:58:46 GMT
USER emqx
# Tue, 19 May 2026 22:58:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:58:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:58:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:58:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488dcea6725f9302e215530c31927d7f86591528625bf1f3a949440b9515f89f`  
		Last Modified: Tue, 19 May 2026 22:59:00 GMT  
		Size: 78.6 MB (78625065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e4901702235f6109a1332f77a15b3ba204a9d5a21ffe0164bc326edc684f39`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:84b4aaede4492c0f385dd4277c9132c58c88d11f62bb8a58fd66b1f9079b89bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07d6fef08a881213bdc3b4c8febe547c090bcb26a7e8666b9ae742e6863c8a5`

```dockerfile
```

-	Layers:
	-	`sha256:fba577b3f04ff5dfe3ad4c45fb639fb8f05da9880384d559ff6c874fb30b6efc`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 2.4 MB (2403579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a733767c3522fffff4204e2687ecce87f9df0e2ff60ec0fefc189fca92701ed3`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 12.5 KB (12485 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0d2c49808220103e223773f07b8c9f451b4e3d6cd05c798edcb5aea1f4b719f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106675729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796be0a9911cdab54ed7517797017e42e2637b270897acd1f3d6daeb399070d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:56:09 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 19 May 2026 22:56:09 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 19 May 2026 22:56:09 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 19 May 2026 22:56:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:56:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:56:09 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:56:09 GMT
USER emqx
# Tue, 19 May 2026 22:56:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:56:09 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:56:09 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:56:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:56:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50319fd60744bc1658c14ef4726d7cc07e1ddadeb4561a9ec5a625f6471cab41`  
		Last Modified: Tue, 19 May 2026 22:56:25 GMT  
		Size: 76.5 MB (76532746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ca3ed1a35d0c2678fe53911c5faa117b7d50e4f5f86f7d78345ca8ff14721`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:465c5a77f0800b1b0050da15c1935023364d3a1c1f2bcdb982fef5dd14df951a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b251c0d042bc2e4d758e2ba3a94a70abbfd6fd1c83134b06684dd23c7ce605a`

```dockerfile
```

-	Layers:
	-	`sha256:441c627f67f3609a65cb74b13a4c54b34d395925bd2160c92ca8fa9c51dd1e88`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 2.4 MB (2403860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8cacf7129222937f3ee7287585271752a0c1c6a820fe7a6f2c0f49f5fb6646f`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:037db7e735a795d92b943ed9213d19b76cbc484e3faea4e1508cc79452dae8a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:4f6bad906895f2cefba3480bf5c53826f24530873a94e18e0eccea22cbd5955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108406053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b1ebbbe051ea04e35c094a95670c05ad219a6451eb4b411415d8dfedddf41b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:46 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 19 May 2026 22:58:46 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 19 May 2026 22:58:46 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 19 May 2026 22:58:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:58:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:58:46 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:58:46 GMT
USER emqx
# Tue, 19 May 2026 22:58:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:58:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:58:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:58:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488dcea6725f9302e215530c31927d7f86591528625bf1f3a949440b9515f89f`  
		Last Modified: Tue, 19 May 2026 22:59:00 GMT  
		Size: 78.6 MB (78625065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e4901702235f6109a1332f77a15b3ba204a9d5a21ffe0164bc326edc684f39`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:84b4aaede4492c0f385dd4277c9132c58c88d11f62bb8a58fd66b1f9079b89bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07d6fef08a881213bdc3b4c8febe547c090bcb26a7e8666b9ae742e6863c8a5`

```dockerfile
```

-	Layers:
	-	`sha256:fba577b3f04ff5dfe3ad4c45fb639fb8f05da9880384d559ff6c874fb30b6efc`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 2.4 MB (2403579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a733767c3522fffff4204e2687ecce87f9df0e2ff60ec0fefc189fca92701ed3`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 12.5 KB (12485 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0d2c49808220103e223773f07b8c9f451b4e3d6cd05c798edcb5aea1f4b719f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106675729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796be0a9911cdab54ed7517797017e42e2637b270897acd1f3d6daeb399070d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:56:09 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 19 May 2026 22:56:09 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 19 May 2026 22:56:09 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 19 May 2026 22:56:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:56:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:56:09 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:56:09 GMT
USER emqx
# Tue, 19 May 2026 22:56:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:56:09 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:56:09 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:56:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:56:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50319fd60744bc1658c14ef4726d7cc07e1ddadeb4561a9ec5a625f6471cab41`  
		Last Modified: Tue, 19 May 2026 22:56:25 GMT  
		Size: 76.5 MB (76532746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ca3ed1a35d0c2678fe53911c5faa117b7d50e4f5f86f7d78345ca8ff14721`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:465c5a77f0800b1b0050da15c1935023364d3a1c1f2bcdb982fef5dd14df951a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b251c0d042bc2e4d758e2ba3a94a70abbfd6fd1c83134b06684dd23c7ce605a`

```dockerfile
```

-	Layers:
	-	`sha256:441c627f67f3609a65cb74b13a4c54b34d395925bd2160c92ca8fa9c51dd1e88`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 2.4 MB (2403860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8cacf7129222937f3ee7287585271752a0c1c6a820fe7a6f2c0f49f5fb6646f`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:037db7e735a795d92b943ed9213d19b76cbc484e3faea4e1508cc79452dae8a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:4f6bad906895f2cefba3480bf5c53826f24530873a94e18e0eccea22cbd5955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108406053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b1ebbbe051ea04e35c094a95670c05ad219a6451eb4b411415d8dfedddf41b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:46 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 19 May 2026 22:58:46 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 19 May 2026 22:58:46 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 19 May 2026 22:58:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:58:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:58:46 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:58:46 GMT
USER emqx
# Tue, 19 May 2026 22:58:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:58:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:58:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:58:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488dcea6725f9302e215530c31927d7f86591528625bf1f3a949440b9515f89f`  
		Last Modified: Tue, 19 May 2026 22:59:00 GMT  
		Size: 78.6 MB (78625065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e4901702235f6109a1332f77a15b3ba204a9d5a21ffe0164bc326edc684f39`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:84b4aaede4492c0f385dd4277c9132c58c88d11f62bb8a58fd66b1f9079b89bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07d6fef08a881213bdc3b4c8febe547c090bcb26a7e8666b9ae742e6863c8a5`

```dockerfile
```

-	Layers:
	-	`sha256:fba577b3f04ff5dfe3ad4c45fb639fb8f05da9880384d559ff6c874fb30b6efc`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 2.4 MB (2403579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a733767c3522fffff4204e2687ecce87f9df0e2ff60ec0fefc189fca92701ed3`  
		Last Modified: Tue, 19 May 2026 22:58:58 GMT  
		Size: 12.5 KB (12485 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0d2c49808220103e223773f07b8c9f451b4e3d6cd05c798edcb5aea1f4b719f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106675729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796be0a9911cdab54ed7517797017e42e2637b270897acd1f3d6daeb399070d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:56:09 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 19 May 2026 22:56:09 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 19 May 2026 22:56:09 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 19 May 2026 22:56:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 May 2026 22:56:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 19 May 2026 22:56:09 GMT
WORKDIR /opt/emqx
# Tue, 19 May 2026 22:56:09 GMT
USER emqx
# Tue, 19 May 2026 22:56:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 May 2026 22:56:09 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 19 May 2026 22:56:09 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 19 May 2026 22:56:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 May 2026 22:56:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50319fd60744bc1658c14ef4726d7cc07e1ddadeb4561a9ec5a625f6471cab41`  
		Last Modified: Tue, 19 May 2026 22:56:25 GMT  
		Size: 76.5 MB (76532746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ca3ed1a35d0c2678fe53911c5faa117b7d50e4f5f86f7d78345ca8ff14721`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:465c5a77f0800b1b0050da15c1935023364d3a1c1f2bcdb982fef5dd14df951a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b251c0d042bc2e4d758e2ba3a94a70abbfd6fd1c83134b06684dd23c7ce605a`

```dockerfile
```

-	Layers:
	-	`sha256:441c627f67f3609a65cb74b13a4c54b34d395925bd2160c92ca8fa9c51dd1e88`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 2.4 MB (2403860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8cacf7129222937f3ee7287585271752a0c1c6a820fe7a6f2c0f49f5fb6646f`  
		Last Modified: Tue, 19 May 2026 22:56:22 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
