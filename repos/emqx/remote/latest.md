## `emqx:latest`

```console
$ docker pull emqx@sha256:a3722d82866c1d648a6890f51cbd0a0839158eb7c343e01b471301b6a530160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:8fdfd0ca74d9ecc52a956c9f3b71539910741b5b9a7e89c7a27df68b9e6f77b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100211988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3498af7074104eff8d97408cf66afe6eac4cc3788481cd3ee1a8e52fe99f1c8a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:49:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:49:16 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 12 Jan 2023 19:22:23 GMT
ENV EMQX_VERSION=5.0.14
# Thu, 12 Jan 2023 19:22:23 GMT
ENV AMD64_SHA256=d39b51da45aa6675cc3026965db120c0dd0a4b070cfe7e47ba2075ac8162d077
# Thu, 12 Jan 2023 19:22:24 GMT
ENV ARM64_SHA256=bfa6d03e3acfd6dbd48c626f66742c00778a2f3030bd76c6faf0199e272836a2
# Thu, 12 Jan 2023 19:22:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 12 Jan 2023 19:22:30 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 12 Jan 2023 19:22:30 GMT
WORKDIR /opt/emqx
# Thu, 12 Jan 2023 19:22:31 GMT
USER emqx
# Thu, 12 Jan 2023 19:22:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 12 Jan 2023 19:22:31 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 12 Jan 2023 19:22:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 12 Jan 2023 19:22:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 12 Jan 2023 19:22:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226f5729eeebf1d9e397edf672aef9dc2809741454ab2d1a2f58a4bb3f67eb0`  
		Last Modified: Wed, 11 Jan 2023 03:50:07 GMT  
		Size: 3.0 MB (2987690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786684ff862ef4f11abc26cfb08583cf925746ea80d7c34769aa93aa99660e7`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bef4235e4b540be8534b86673e32a0fba10d7a27c2f2df3e3df7fa12c45ade`  
		Last Modified: Thu, 12 Jan 2023 19:23:23 GMT  
		Size: 65.8 MB (65822318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277fbd542e565fedaa64283fb136e740c1e224d022f890c4098187516b38093`  
		Last Modified: Thu, 12 Jan 2023 19:23:15 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fcb2042112e26ff2438ed0e4eaf737d611375655fbf6d315e062fb66a0d7cfdc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91300415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1526045fe1d480c3bd63bc073bd22c247e984d4c476ba6e2c4e0023f57804f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:30:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:30:55 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 12 Jan 2023 18:39:38 GMT
ENV EMQX_VERSION=5.0.14
# Thu, 12 Jan 2023 18:39:38 GMT
ENV AMD64_SHA256=d39b51da45aa6675cc3026965db120c0dd0a4b070cfe7e47ba2075ac8162d077
# Thu, 12 Jan 2023 18:39:38 GMT
ENV ARM64_SHA256=bfa6d03e3acfd6dbd48c626f66742c00778a2f3030bd76c6faf0199e272836a2
# Thu, 12 Jan 2023 18:39:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 12 Jan 2023 18:39:43 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 12 Jan 2023 18:39:43 GMT
WORKDIR /opt/emqx
# Thu, 12 Jan 2023 18:39:43 GMT
USER emqx
# Thu, 12 Jan 2023 18:39:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 12 Jan 2023 18:39:43 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 12 Jan 2023 18:39:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 12 Jan 2023 18:39:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 12 Jan 2023 18:39:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc2e1d7e4868b505e10f5031690f64d100e27341b52efe1502538f59eb5c6b`  
		Last Modified: Wed, 11 Jan 2023 13:31:41 GMT  
		Size: 3.0 MB (3002805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7657cfec2c515e4133df88eecfb40ffd2d19a87eacd8fb4643dad7696a6f8ffe`  
		Last Modified: Wed, 11 Jan 2023 13:31:40 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ae20404804775f5a9e7579e7a743156cecaa2e67197dfb03ec0f71e46ddb2b`  
		Last Modified: Thu, 12 Jan 2023 18:40:34 GMT  
		Size: 58.2 MB (58247782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5f0df15292d2e67b9eff082eb8e250b4cb24907adc2656d986887cfc10d4e6`  
		Last Modified: Thu, 12 Jan 2023 18:40:28 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
