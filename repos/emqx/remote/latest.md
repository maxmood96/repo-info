## `emqx:latest`

```console
$ docker pull emqx@sha256:983d885bc1b76818bb769b1a1f4b8d713e7284e3ba72f931dc622cb4f97bfcfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:73f08b2ec0fb38e8c6b5222d2031058f92bae434e7781710f66f23f3de5dd2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109909273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c07a2f6f89b0a41ceb960016e53260246391c1ab3809ea8b1bf34e5e8f79310`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001c341bcd760753ca192f57aac4c3ca6fe825b997840e0c18c72be1918b846`  
		Last Modified: Tue, 22 Oct 2024 16:56:08 GMT  
		Size: 80.8 MB (80781921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6d3bf26a86d0be8a04317b104743cef6703e83474b5dce305c1224feb82b4a`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:2825e8d0751787152a7b58a9df04c82cdb4ee14e63a0b6a66b84490578ec6523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e15900551528293de41105bd08e012a64b57684f45c442d67b625e48a6dc4b8`

```dockerfile
```

-	Layers:
	-	`sha256:dcc3d0d5953a5fcf16da7dcada7a76eb83a75caf0345a35b14ba0a91978afb0f`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 2.6 MB (2624750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb19138927642c0126a5d50f64367e4fc24e72878dde16f28c07a091b1d2a8f7`  
		Last Modified: Tue, 22 Oct 2024 16:56:06 GMT  
		Size: 12.3 KB (12315 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bf84a3fdb8b744f65cc83b078fe6f6bbc09eac84de5c2c2d257cee6d0b2b65fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107097129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32632f41a7369effd68aa93f80c8a37c96bc903fe868f0e38de6fb9e2fba076d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d196bcfe1e1b9d831f9206be1909867be476ebcc4cd14abf81cc717c29d7274a`  
		Last Modified: Tue, 22 Oct 2024 16:55:57 GMT  
		Size: 77.9 MB (77939724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5321e15b65b59f02dfcb34cd289b3fff03c36a88b952fb2dcb95a257a524d`  
		Last Modified: Tue, 22 Oct 2024 16:55:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:285fbd3d644a00c7a1e9426c8ecbb2642f5dc8752c49f7a06099b11cdbd9012a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84222ce87ed3bdeb1128239b1854b6149b40427373de46897280f30b997cc808`

```dockerfile
```

-	Layers:
	-	`sha256:a06dcdbccb3564a9fde3d56f720598ebc16df41eb292bbc083e813bdf7c8b299`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 2.6 MB (2625029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bccbfcfd1900f2bab668677abbdc31bd269ea5c79d3d821c6bccc538d669d6bd`  
		Last Modified: Tue, 22 Oct 2024 16:55:55 GMT  
		Size: 12.4 KB (12437 bytes)  
		MIME: application/vnd.in-toto+json
