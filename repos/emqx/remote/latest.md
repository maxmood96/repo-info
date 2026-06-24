## `emqx:latest`

```console
$ docker pull emqx@sha256:2eb7ca866279e39883a77e15af3fc6a8cef8399d590be76bd5439aca3897366d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:d0e61cbcda9eb01db956897efbf9fe69840cb946ec90d3b3acd42fc3a9390f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108411669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c532308d6cc03979df4ba6b8f7e8905daca5b862863f86d82281ca4b782ce8fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:15:24 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 24 Jun 2026 01:15:24 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 24 Jun 2026 01:15:24 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 24 Jun 2026 01:15:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Jun 2026 01:15:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 24 Jun 2026 01:15:24 GMT
WORKDIR /opt/emqx
# Wed, 24 Jun 2026 01:15:24 GMT
USER emqx
# Wed, 24 Jun 2026 01:15:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Jun 2026 01:15:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 24 Jun 2026 01:15:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 24 Jun 2026 01:15:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:15:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995dd6c24dfa1f55f8d3c0128165b6a0b2f5b31d949093aa7c16bc420ef54fe7`  
		Last Modified: Wed, 24 Jun 2026 01:15:40 GMT  
		Size: 78.6 MB (78625187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ac6294d300642ed9f08cad03a1b2930e1bf142d77bc3cb314659c7b9377162`  
		Last Modified: Wed, 24 Jun 2026 01:15:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:5f5eca78bd250541e81b7cd82b4370459b8a755b5c8e0a3455e13d51c93cc702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a687195a1f2fb810e17c6e92f5940183465a8300b35086fe3288c78513a3d1d`

```dockerfile
```

-	Layers:
	-	`sha256:0c9eb90c08321dd43962a09b76f7f49b63f143d3913d7dca15115eb628b5f1cd`  
		Last Modified: Wed, 24 Jun 2026 01:15:38 GMT  
		Size: 2.4 MB (2403669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e693f50fed9079902f537f712866a94d1d29a34c298b974947c484d7184e567c`  
		Last Modified: Wed, 24 Jun 2026 01:15:37 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f2380ed687d668909794ab28714b3dce6b64b8803c397619f1031a2c0dab1d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106682153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd6b516072cc06b719786807764123661ee084f41f24abd7033aee4730af0f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:16:07 GMT
ENV EMQX_VERSION=5.8.8
# Wed, 24 Jun 2026 01:16:07 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Wed, 24 Jun 2026 01:16:07 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Wed, 24 Jun 2026 01:16:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Jun 2026 01:16:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 24 Jun 2026 01:16:07 GMT
WORKDIR /opt/emqx
# Wed, 24 Jun 2026 01:16:07 GMT
USER emqx
# Wed, 24 Jun 2026 01:16:07 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Jun 2026 01:16:07 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 24 Jun 2026 01:16:07 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 24 Jun 2026 01:16:07 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:16:07 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbbafa968801bb842f807932c96037fc4bb1917f9f4665391c91f0ee10140c4`  
		Last Modified: Wed, 24 Jun 2026 01:16:24 GMT  
		Size: 76.5 MB (76532540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae21aaec650b53bcde01cfec6a8420ead8154dd50b270290e73856c734424d4b`  
		Last Modified: Wed, 24 Jun 2026 01:16:21 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:46fe2fae42f0a1ea5e31c68cc554f5ddb0f511fd2cba8888adbf31c83b47aef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f662177bfed3b700af8abf762e3615e3f1c2b51676f9c2af5db617347000b67`

```dockerfile
```

-	Layers:
	-	`sha256:7ad5875c299627ba17daf853bdd12d1963b039517f891b814faeef54130cd75d`  
		Last Modified: Wed, 24 Jun 2026 01:16:21 GMT  
		Size: 2.4 MB (2403950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635baa7e2a39a925d37d09f8c04393e9173de06befc3c1181773335d62191be6`  
		Last Modified: Wed, 24 Jun 2026 01:16:21 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
