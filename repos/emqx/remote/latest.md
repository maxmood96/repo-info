## `emqx:latest`

```console
$ docker pull emqx@sha256:1e3008739b2a9826d165563f2a01a37ba1512579a6e4962c1d6c12d2c5f33159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:b61169b9ea180b4b94e80e5270b70cc98d27f7403dbc6ab1862b67598c440c2f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125874711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a1ce4aea8d2a264875f19a6be895364b3c8d26b0323bd39d6303b4b872cf4e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 22:51:01 GMT
ENV EMQX_VERSION=5.7.0
# Tue, 28 May 2024 22:51:01 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Tue, 28 May 2024 22:51:01 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Tue, 28 May 2024 22:51:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 28 May 2024 22:51:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 28 May 2024 22:51:18 GMT
WORKDIR /opt/emqx
# Tue, 28 May 2024 22:51:18 GMT
USER emqx
# Tue, 28 May 2024 22:51:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 28 May 2024 22:51:18 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 28 May 2024 22:51:18 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 28 May 2024 22:51:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 28 May 2024 22:51:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895353a6d3adcc5ecde8b1b0282c168023c4c6632ca780317cc15a07f0b69a6c`  
		Last Modified: Tue, 28 May 2024 22:51:49 GMT  
		Size: 96.7 MB (96723267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24da20449b1d0b327b87538fbc3533b2ff0c0bb7e6c28e7c2378997904904781`  
		Last Modified: Tue, 28 May 2024 22:51:39 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8468c03000265baff59f6e0b9672f48f3c6b97390dd5b4cdff617f5c97442f0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ef707698df6918c8e04ee8441d77ec406bf81d94cc5c1d276a9180b446008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:29:23 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 14 May 2024 02:29:23 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 14 May 2024 02:29:23 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 14 May 2024 02:29:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:29:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 02:29:37 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:29:37 GMT
USER emqx
# Tue, 14 May 2024 02:29:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:29:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:29:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 02:29:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:29:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ebe9d5a7da4209ef18c6868756f65c50af18ae6a0ab8b488ee547abd7dc1`  
		Last Modified: Tue, 14 May 2024 02:31:07 GMT  
		Size: 91.6 MB (91615783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa9fd0acdb66a85f8f5effb30d086ed735a003eb6fe434a2d47984fd6aa4c52`  
		Last Modified: Tue, 14 May 2024 02:30:59 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
