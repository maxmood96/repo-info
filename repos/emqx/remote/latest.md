## `emqx:latest`

```console
$ docker pull emqx@sha256:053a4c75b720fac3d105629c89d2cf8c533161e36826091420db060d6aa769fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:7b09bb25217854d7cf2d57445a1e5f33ce92dcd07da27b2af2b359bf98860122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105502215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8690bdb44c015ce32a9bcf2bfe4c4551a17432c68e8e8f278a3cc454eddb56c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6d894e5594eea8988334e4a1db35a5f05b9422fe3ddb88fa58c9fee6dc6bc`  
		Last Modified: Tue, 03 Jun 2025 13:40:34 GMT  
		Size: 77.3 MB (77275823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ee218c6794551cffd40a1251cec7a70984bab25af57fd6348dd686b537e3f6`  
		Last Modified: Tue, 03 Jun 2025 13:40:19 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:6560eaf1c2eaae0b828df266af312dfdd1dddda8fe08bfa5ae7bf77a4a17fa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2650188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a47b008d77342793aa2632f9314ab217b42c0deb1d62dcc8933b21cc4ffb8b`

```dockerfile
```

-	Layers:
	-	`sha256:449274ae78aa041ac77737214e56193cd43c0881723f2c85bf57c9131b7adc0b`  
		Last Modified: Wed, 04 Jun 2025 13:45:05 GMT  
		Size: 2.6 MB (2637659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ea7e2d146e0e8fea25a6431663c230a255bd6823df1b0e06cc5da2170481d0`  
		Last Modified: Wed, 04 Jun 2025 13:45:06 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:4fc1572855c8386bed69f3a56e44e30f89240a4f55a85eb89aeb87e92fd288a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102617203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564283128683592d8bb282ed7bfca22e0add21c17e9978411e481c46f6c5e4b3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 25 Mar 2025 16:14:46 GMT
ENV EMQX_VERSION=5.8.6
# Tue, 25 Mar 2025 16:14:46 GMT
ENV AMD64_SHA256=430f69c24c0d659a9ce2e902d018c6dd20565519925e0cc893980d824b0a952e
# Tue, 25 Mar 2025 16:14:46 GMT
ENV ARM64_SHA256=dcabedb9d3888e0fb6e8138da6ae3d8ef1afce1f85e4580f26f19d65115ed5c3
# Tue, 25 Mar 2025 16:14:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 25 Mar 2025 16:14:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
WORKDIR /opt/emqx
# Tue, 25 Mar 2025 16:14:46 GMT
USER emqx
# Tue, 25 Mar 2025 16:14:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 25 Mar 2025 16:14:46 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 25 Mar 2025 16:14:46 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 25 Mar 2025 16:14:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 16:14:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00318c88ff4d067987fdcec9d58c2df57447d880bef917c9755a6df78220f015`  
		Last Modified: Tue, 03 Jun 2025 14:05:17 GMT  
		Size: 74.6 MB (74550860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40548ae246694b976ff99dc22898c061aac05acebd2d268ef084256da0079cd`  
		Last Modified: Tue, 03 Jun 2025 14:05:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:9703edb1d241e8a0d47e95657530feb8f4d8aecc68077b19f84673f87a3a413b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2650571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d9e1888a6ebf0cc7c0079013984ebe493977dafeeb8c5ac33ba404c5460095`

```dockerfile
```

-	Layers:
	-	`sha256:910e84a7251a931c3ade04975330447dbf0aab3534ac942cfd7f1c65ec137ff0`  
		Last Modified: Wed, 04 Jun 2025 13:45:04 GMT  
		Size: 2.6 MB (2637939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f639a04a2f1f13461d671647c5f117bf0e9d6758af58a857ce6ecc5f6f05909c`  
		Last Modified: Wed, 04 Jun 2025 13:45:06 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json
