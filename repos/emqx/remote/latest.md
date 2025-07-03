## `emqx:latest`

```console
$ docker pull emqx@sha256:eee2b59a9b60f71b19b2f95ba03d3aa1e10072e01e6280f43e6103fca64ac2fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:2911c1442d1099b4370ec8cafb3ccfb959f114798f0442da1571edf76628f620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105580869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31100f4e889c626fc0c08a28580ea526deaab0740a10a7faabf76a6d3ce5cca`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f03e4bafd83e87c46081d5b2146bc2c22efa5e7f40b556ad4223895a2c2892`  
		Last Modified: Thu, 03 Jul 2025 17:03:17 GMT  
		Size: 77.3 MB (77349665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878fa6e297da1f79ab461aa8ed7d34b665caad1d02b5b7e702c00f958de93ca4`  
		Last Modified: Thu, 03 Jul 2025 17:03:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:f9efa484180f77de524889d2f340306a7b2a55588e44befe630bcd5e088e9334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6512ddc09cf0611c58299c4eaea99b38e66ae0c652819ac8abd4d43cdf932c8f`

```dockerfile
```

-	Layers:
	-	`sha256:26e24ac2a8d02a260655fc3192b2ec5f9c86bd367539077f6ee90ee073620cff`  
		Last Modified: Thu, 03 Jul 2025 17:27:21 GMT  
		Size: 2.7 MB (2741191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db668ffd7a604c7265d7e2acc89037348bad452d9bbc2176dd8be6c200df436f`  
		Last Modified: Thu, 03 Jul 2025 17:27:22 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:778848504b94b67aa22123b3f47fa044a93fd662a26dd824edd0b0ab63ef5495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102688026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cb92f7cad7e67090ceb8fcf0c004915cea6d66f5656a4c39e097455be9c477`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c28d2422859f388a0137099a090d1f56edcf474fb76cb547800d029386b2fb6`  
		Last Modified: Thu, 03 Jul 2025 17:02:30 GMT  
		Size: 74.6 MB (74609285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e17e5d41b4d87d754471d68c0f80d2a3ca1cd23a43f7debee1409b09e6e22`  
		Last Modified: Thu, 03 Jul 2025 17:02:23 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:8a7770c4b08acff6cb25ca8d2d63eb2ef7b9cc4837a2cc61d03a4447f514e379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2754104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a30fdc8e142d70ad5f331aa038bdc8dd6254b75b370cd198a601271bdce55d8`

```dockerfile
```

-	Layers:
	-	`sha256:00293fd16f4fe3b0fe0d7db846e3b384fcf2f6b279b06efa9cd7244537a018fd`  
		Last Modified: Thu, 03 Jul 2025 17:27:26 GMT  
		Size: 2.7 MB (2741471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3807891fa993c329164a5c710a8005dd21f6de654b726d68d33e734d167e0f49`  
		Last Modified: Thu, 03 Jul 2025 17:27:26 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
