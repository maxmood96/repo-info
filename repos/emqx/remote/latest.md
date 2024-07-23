## `emqx:latest`

```console
$ docker pull emqx@sha256:51c39f5995f6aedd292707e73c7dbfbe8b72b82a5d0e2be5f2ef1c14df09c599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:66c1f31561788effe34d9804299758d4927b7e11d8467297de202a96835f925f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126238122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdc5370bf923bab8c90743b24666bca939fd1f2874c786e47d23fa1fbbfd87b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ea6242b71c16ce1352fcf57a0d11687c2bd0b9fd496834fd62f76dd8f5ebf2`  
		Last Modified: Tue, 23 Jul 2024 07:19:54 GMT  
		Size: 97.1 MB (97110772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312a74d0107a3ee33685af3838ac090917b45e87cb3006fc6192781d92482b4c`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:8e4ad0134f93a3a02b2167fa3392b9b80c19466227b895ce27358ee2077c37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f34cd44ade291f177d0677daa06c10214702867382053ae2ca28173d626e3f8`

```dockerfile
```

-	Layers:
	-	`sha256:7c83086fd6007886c99a90d7d357091c7e561d320beb2faba0c8bbcc497c6298`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 2.6 MB (2599757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4740c9a8c3c0fdbc38c099b4759c70dc685a1bdf61a78e9702f2e6540074d6fb`  
		Last Modified: Tue, 23 Jul 2024 07:19:51 GMT  
		Size: 12.3 KB (12305 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:074ff8d864916263abc6e8c42120a7efa67fea641cb6a3a070a3614a2c5b66d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573da311dffd01ef129754dc5a68bc6494d88d070bb031800b6881927091e973`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31646db1381832e88900fde1500ba647e8458191411a4d10dcc4c8becfe406`  
		Last Modified: Mon, 08 Jul 2024 19:14:23 GMT  
		Size: 93.7 MB (93657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d975f3920ce02bd4da5ca7a8fdc83b4f8f921649f9451c80a10c3edccf678`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:dd3bbbb96dcc4b68baf65342c6a21b9823d447ab4b1885e31b16f99167788509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb517a98e5b34cd172b0be13bd95c2cf36068984db6969a8c563accb9a671403`

```dockerfile
```

-	Layers:
	-	`sha256:5dd0ef27adb8bfba84a8a3bbd60855144597953b9ee86a6b30793bdc44cdb30c`  
		Last Modified: Mon, 08 Jul 2024 19:14:21 GMT  
		Size: 2.6 MB (2559768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ba143a92dd352085be44c5cc683e7846827132d92ab0aa6c287b80b3d3ac`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json
