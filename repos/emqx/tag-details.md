<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.4`](#emqx584)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:79b1b2925e5f0f792679385364079f213203c31f1dfe045d5be5d88c00afd8f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:befc995804db661dcb5676d3f6e48d7b3f5f4a2c8eedb6cfa15920012beae7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105350249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdb1f9111a02e167750ccc13460175afa606ad15bb5f9863084a7cf98f3837f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59c99e5135984db710b8c3b03d08c1c4dac84c70e6583ca7aafc9702402af27`  
		Last Modified: Tue, 04 Feb 2025 04:21:53 GMT  
		Size: 77.1 MB (77136885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281e320adda9d86da0ae50198ec4803708e30d8910ea2d4db4ee200309e1c466`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:605da76845f5c2b3168b54d863fee012319aab8f7525e3097e861f60614e100c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014dc5f24904413d62e7b4e0ca850bedb65cc7ad4aaa7143359ae422e1072b1b`

```dockerfile
```

-	Layers:
	-	`sha256:69bb9263813d22e1181c149d9697460a679699a5752d370515356b583b46b959`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 2.5 MB (2470546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c82b75edfa022d3b65922ff32bdeb42417f1fe2deffffd4e3f408a6f29ef00`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bb4f87d7d3a6116acabab76f27d35cba214b11baa6d2e31f9aed5e76116e43e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102457966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93c89683094d71279385fd2d6dc21d36570f45298bf66605ed86f6670200756`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5b469ad917972405d37e069f91a116dd976b97cf678e0690d0622c01bf2a`  
		Last Modified: Tue, 25 Feb 2025 02:19:07 GMT  
		Size: 74.4 MB (74408477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f64e39954115c3c2337a4140f13ceef8da269cf842eeedbf4a548fd8ec08a`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:e6053c2d522e4981890e166ba0e036044f59383d92ac7a3d2b5af33efed83565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6a595128f2a02f8d5b6a605c188c0413bc21a1d3a5fe6a428dc9a0800c0a76`

```dockerfile
```

-	Layers:
	-	`sha256:f7b05da203bf1d9874b7d2966dee910af35010ccb8f578aaa61af08141c648b2`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 2.6 MB (2614780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9bd5667c99e9a4035c31bf4b1e4c3c9f6112814fc03dc0874b33945077322d`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:7ece5014fde535debe1cabffce340f7bf21f0f2b0e56183f7a12389eb4ec8a77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:7b3c63f3e035db28e8ffe65d4537403918e90ad939771ddcdbc06efa2aba9bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125361204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2384bafe7e3ced491dd15713be0e7e9cdafe4f46f48c7c426f2c0c927ec29d27`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb44fe30ebf0d7921ab3e0540fb589917f3cadaf5d093045faece7673ad23c49`  
		Last Modified: Tue, 04 Feb 2025 04:21:56 GMT  
		Size: 97.1 MB (97147838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3592113309d90bcd086c8e58287e94dcbeb4be957cf4f506878e668adba72a`  
		Last Modified: Tue, 04 Feb 2025 04:21:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:53a344c386f7137bfd4fad2d773869e64d192c9c7820a47be4c4b3011fac2929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46ac7c9109eac6eab3991b3dddfc9082f1a66b037467dc34c2a43f0a74b8fbc`

```dockerfile
```

-	Layers:
	-	`sha256:e4dd75569c6dc5db98c3365bd177fa11a4ef4a2490f7447534224d67ab7e9915`  
		Last Modified: Tue, 04 Feb 2025 04:21:54 GMT  
		Size: 2.5 MB (2469968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d587abd3133c2a29729d5b4c5f418d71a639825649582db13b8dde83ba8535a`  
		Last Modified: Tue, 04 Feb 2025 04:21:54 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fc1f0bc72480373cb6026e537271120d66f5427ac865d2da3ffcff7f73a5d5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121745136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b464c6dcfc92f136330077d779362fb41087d4c6c4fc26fa9f59708f25960c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b75f0ae6ae2f3d7a07935e2e953a9049f63039114decfe8ccf4ff4ce987b69`  
		Last Modified: Tue, 25 Feb 2025 02:18:37 GMT  
		Size: 93.7 MB (93695648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a672a2c5d502e4285088b479ad1934c813f4ca20c43001bbce878b5280609cf`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:95ee8343bc0b25fd940a40884b66c2bc621e8bf24aa36e413f9bf92e1cdd1e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e166d78a7d069dc27968deff9034284ccf029123ce40b9d3c1d7327c89d140c`

```dockerfile
```

-	Layers:
	-	`sha256:3600e2fee9d3ba1ffbe41bc43ebb773cf8787a74c9a03b19eba34b807b12c693`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 2.6 MB (2624155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598f302a8cb26e3042885c9f04bc95a726d89ee978c4b495d7c546f524e08942`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:7ece5014fde535debe1cabffce340f7bf21f0f2b0e56183f7a12389eb4ec8a77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:7b3c63f3e035db28e8ffe65d4537403918e90ad939771ddcdbc06efa2aba9bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125361204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2384bafe7e3ced491dd15713be0e7e9cdafe4f46f48c7c426f2c0c927ec29d27`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb44fe30ebf0d7921ab3e0540fb589917f3cadaf5d093045faece7673ad23c49`  
		Last Modified: Tue, 04 Feb 2025 04:21:56 GMT  
		Size: 97.1 MB (97147838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3592113309d90bcd086c8e58287e94dcbeb4be957cf4f506878e668adba72a`  
		Last Modified: Tue, 04 Feb 2025 04:21:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:53a344c386f7137bfd4fad2d773869e64d192c9c7820a47be4c4b3011fac2929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46ac7c9109eac6eab3991b3dddfc9082f1a66b037467dc34c2a43f0a74b8fbc`

```dockerfile
```

-	Layers:
	-	`sha256:e4dd75569c6dc5db98c3365bd177fa11a4ef4a2490f7447534224d67ab7e9915`  
		Last Modified: Tue, 04 Feb 2025 04:21:54 GMT  
		Size: 2.5 MB (2469968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d587abd3133c2a29729d5b4c5f418d71a639825649582db13b8dde83ba8535a`  
		Last Modified: Tue, 04 Feb 2025 04:21:54 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fc1f0bc72480373cb6026e537271120d66f5427ac865d2da3ffcff7f73a5d5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121745136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b464c6dcfc92f136330077d779362fb41087d4c6c4fc26fa9f59708f25960c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b75f0ae6ae2f3d7a07935e2e953a9049f63039114decfe8ccf4ff4ce987b69`  
		Last Modified: Tue, 25 Feb 2025 02:18:37 GMT  
		Size: 93.7 MB (93695648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a672a2c5d502e4285088b479ad1934c813f4ca20c43001bbce878b5280609cf`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:95ee8343bc0b25fd940a40884b66c2bc621e8bf24aa36e413f9bf92e1cdd1e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e166d78a7d069dc27968deff9034284ccf029123ce40b9d3c1d7327c89d140c`

```dockerfile
```

-	Layers:
	-	`sha256:3600e2fee9d3ba1ffbe41bc43ebb773cf8787a74c9a03b19eba34b807b12c693`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 2.6 MB (2624155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598f302a8cb26e3042885c9f04bc95a726d89ee978c4b495d7c546f524e08942`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:79b1b2925e5f0f792679385364079f213203c31f1dfe045d5be5d88c00afd8f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:befc995804db661dcb5676d3f6e48d7b3f5f4a2c8eedb6cfa15920012beae7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105350249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdb1f9111a02e167750ccc13460175afa606ad15bb5f9863084a7cf98f3837f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59c99e5135984db710b8c3b03d08c1c4dac84c70e6583ca7aafc9702402af27`  
		Last Modified: Tue, 04 Feb 2025 04:21:53 GMT  
		Size: 77.1 MB (77136885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281e320adda9d86da0ae50198ec4803708e30d8910ea2d4db4ee200309e1c466`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:605da76845f5c2b3168b54d863fee012319aab8f7525e3097e861f60614e100c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014dc5f24904413d62e7b4e0ca850bedb65cc7ad4aaa7143359ae422e1072b1b`

```dockerfile
```

-	Layers:
	-	`sha256:69bb9263813d22e1181c149d9697460a679699a5752d370515356b583b46b959`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 2.5 MB (2470546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c82b75edfa022d3b65922ff32bdeb42417f1fe2deffffd4e3f408a6f29ef00`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bb4f87d7d3a6116acabab76f27d35cba214b11baa6d2e31f9aed5e76116e43e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102457966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93c89683094d71279385fd2d6dc21d36570f45298bf66605ed86f6670200756`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5b469ad917972405d37e069f91a116dd976b97cf678e0690d0622c01bf2a`  
		Last Modified: Tue, 25 Feb 2025 02:19:07 GMT  
		Size: 74.4 MB (74408477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f64e39954115c3c2337a4140f13ceef8da269cf842eeedbf4a548fd8ec08a`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:e6053c2d522e4981890e166ba0e036044f59383d92ac7a3d2b5af33efed83565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6a595128f2a02f8d5b6a605c188c0413bc21a1d3a5fe6a428dc9a0800c0a76`

```dockerfile
```

-	Layers:
	-	`sha256:f7b05da203bf1d9874b7d2966dee910af35010ccb8f578aaa61af08141c648b2`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 2.6 MB (2614780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9bd5667c99e9a4035c31bf4b1e4c3c9f6112814fc03dc0874b33945077322d`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.4`

```console
$ docker pull emqx@sha256:79b1b2925e5f0f792679385364079f213203c31f1dfe045d5be5d88c00afd8f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.4` - linux; amd64

```console
$ docker pull emqx@sha256:befc995804db661dcb5676d3f6e48d7b3f5f4a2c8eedb6cfa15920012beae7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105350249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdb1f9111a02e167750ccc13460175afa606ad15bb5f9863084a7cf98f3837f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59c99e5135984db710b8c3b03d08c1c4dac84c70e6583ca7aafc9702402af27`  
		Last Modified: Tue, 04 Feb 2025 04:21:53 GMT  
		Size: 77.1 MB (77136885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281e320adda9d86da0ae50198ec4803708e30d8910ea2d4db4ee200309e1c466`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.4` - unknown; unknown

```console
$ docker pull emqx@sha256:605da76845f5c2b3168b54d863fee012319aab8f7525e3097e861f60614e100c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014dc5f24904413d62e7b4e0ca850bedb65cc7ad4aaa7143359ae422e1072b1b`

```dockerfile
```

-	Layers:
	-	`sha256:69bb9263813d22e1181c149d9697460a679699a5752d370515356b583b46b959`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 2.5 MB (2470546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c82b75edfa022d3b65922ff32bdeb42417f1fe2deffffd4e3f408a6f29ef00`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bb4f87d7d3a6116acabab76f27d35cba214b11baa6d2e31f9aed5e76116e43e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102457966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93c89683094d71279385fd2d6dc21d36570f45298bf66605ed86f6670200756`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5b469ad917972405d37e069f91a116dd976b97cf678e0690d0622c01bf2a`  
		Last Modified: Tue, 25 Feb 2025 02:19:07 GMT  
		Size: 74.4 MB (74408477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f64e39954115c3c2337a4140f13ceef8da269cf842eeedbf4a548fd8ec08a`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.4` - unknown; unknown

```console
$ docker pull emqx@sha256:e6053c2d522e4981890e166ba0e036044f59383d92ac7a3d2b5af33efed83565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6a595128f2a02f8d5b6a605c188c0413bc21a1d3a5fe6a428dc9a0800c0a76`

```dockerfile
```

-	Layers:
	-	`sha256:f7b05da203bf1d9874b7d2966dee910af35010ccb8f578aaa61af08141c648b2`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 2.6 MB (2614780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9bd5667c99e9a4035c31bf4b1e4c3c9f6112814fc03dc0874b33945077322d`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:79b1b2925e5f0f792679385364079f213203c31f1dfe045d5be5d88c00afd8f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:befc995804db661dcb5676d3f6e48d7b3f5f4a2c8eedb6cfa15920012beae7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105350249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdb1f9111a02e167750ccc13460175afa606ad15bb5f9863084a7cf98f3837f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59c99e5135984db710b8c3b03d08c1c4dac84c70e6583ca7aafc9702402af27`  
		Last Modified: Tue, 04 Feb 2025 04:21:53 GMT  
		Size: 77.1 MB (77136885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281e320adda9d86da0ae50198ec4803708e30d8910ea2d4db4ee200309e1c466`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:605da76845f5c2b3168b54d863fee012319aab8f7525e3097e861f60614e100c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014dc5f24904413d62e7b4e0ca850bedb65cc7ad4aaa7143359ae422e1072b1b`

```dockerfile
```

-	Layers:
	-	`sha256:69bb9263813d22e1181c149d9697460a679699a5752d370515356b583b46b959`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 2.5 MB (2470546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c82b75edfa022d3b65922ff32bdeb42417f1fe2deffffd4e3f408a6f29ef00`  
		Last Modified: Tue, 04 Feb 2025 04:21:52 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bb4f87d7d3a6116acabab76f27d35cba214b11baa6d2e31f9aed5e76116e43e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102457966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93c89683094d71279385fd2d6dc21d36570f45298bf66605ed86f6670200756`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5b469ad917972405d37e069f91a116dd976b97cf678e0690d0622c01bf2a`  
		Last Modified: Tue, 25 Feb 2025 02:19:07 GMT  
		Size: 74.4 MB (74408477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f64e39954115c3c2337a4140f13ceef8da269cf842eeedbf4a548fd8ec08a`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:e6053c2d522e4981890e166ba0e036044f59383d92ac7a3d2b5af33efed83565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6a595128f2a02f8d5b6a605c188c0413bc21a1d3a5fe6a428dc9a0800c0a76`

```dockerfile
```

-	Layers:
	-	`sha256:f7b05da203bf1d9874b7d2966dee910af35010ccb8f578aaa61af08141c648b2`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 2.6 MB (2614780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9bd5667c99e9a4035c31bf4b1e4c3c9f6112814fc03dc0874b33945077322d`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
