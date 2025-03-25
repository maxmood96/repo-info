<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.6`](#emqx586)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:c0831dfc8b411ea901cec960525432821f0798b5980f1300a2fe1127aaefa2d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:cb6640b2cc2a6fd938af12ca28284feda2811b243139a74c770babc810a1b6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105481388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f8d7b8b37cb2d5cb5a99d26d44be25b5631a731da2afff01e4e08d5567daad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c3849f578c0c6628fc4790503844c09b092d93df58d4331d42113f967e8b8`  
		Last Modified: Tue, 25 Mar 2025 20:56:58 GMT  
		Size: 77.3 MB (77275457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb94386d02a536e149af06ecfc91169322972534411c08733b7b5b8861dd748`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:2b098e62542b78e7b93b95c168e7a262e0a1f0b9b56e43c2acedb24750f8667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54dbbaff263bd4cb5d85d550be78347e918197b384fdb7e474de729c4cc44adf`

```dockerfile
```

-	Layers:
	-	`sha256:6ee6a80a1686bfa83cc5201b0f4e65fe9bbc5329b754d7bfddabdfe55891a84d`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 2.6 MB (2614518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c060c3bd2f51e444da4435471fa7dcbf9b6cec2208c47ae91470ad8704edd8e2`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8cf1b426db7e7b444056244992bc0bda791705810b43f55c06f76890b3453bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102595006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dd45e38223a6d7b65e7d9f86faec5511eaae2bcf6e3d6a0a341e6832144161`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f89ccda1ed8650a3ce57d4f64f40541c7438e3e20c3967b1898151b0dc8b016`  
		Last Modified: Tue, 25 Mar 2025 20:56:30 GMT  
		Size: 74.5 MB (74549906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e882a7b9f79bc29aea9b1e799d4d24e0d523c12f4eb8b7d7b04042f3f3ddd557`  
		Last Modified: Tue, 25 Mar 2025 20:56:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:4182e9290f6c5d562eaf44a1332319a894bd3f84e59ea763987ec8aa85ba489a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10894c2d4c92e83b2eae115c549fd59eabe234e35158d4a7f748c47932c7337`

```dockerfile
```

-	Layers:
	-	`sha256:9842809cf7c0ee1dc90936881035a5864f209b40b0cfc3f6ba51da5ee90e0947`  
		Last Modified: Tue, 25 Mar 2025 20:56:28 GMT  
		Size: 2.6 MB (2614798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccb0f704c5eb3254a6d6684a10c41a0f381e7b29d2035422a8bd27d86ea28ba`  
		Last Modified: Tue, 25 Mar 2025 20:56:28 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:9a3522c6aa90e185fc503baf6f428c60c49428dd7a029d78824936e82a8b0dd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:3a3c7b620559ce83c17ba4fae6ce0ff24026b26ea831a160a6c36cfbbd7ded02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125353882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed69cbffdb51187de2b2cd07c4f99ee213df9d0c2ecaee0dd9c170ecc13e2f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a9952e19ffe8de7b43dee788754c3e7aa7e006bc48a2020ed20e137bf284a`  
		Last Modified: Mon, 17 Mar 2025 23:12:36 GMT  
		Size: 97.1 MB (97147955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65f3af15e5991942024404577817f290093c6cc73c306b9b5457f2e02b74b93`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:1850adedac86f3aaefac09cea3a9bf16e6d3faaf143e6df5a12f8c54b4ba63e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49132a604e0a3fbf56b6e41f5f2cb3693d6d59293956a829115ae05fda234a5c`

```dockerfile
```

-	Layers:
	-	`sha256:befe33bf1c163a3f2dda4585fe0106984a68e38ad4a383afdfa27b52ce198b3e`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 2.6 MB (2623911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcc2a157ead6fa4ad55697a82730fb68e1dae6fd5969bd09d71803b77270723`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c7621498c23d6575fa7853cd279ea1dc5eb3dcea077a0931d30d1ac656b6e897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121740954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0013969d3ded04ae09073cf79ec202ecdc60b7ab8706b22bf872023e4a845a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739b932bb5a341ed63b5cfe55c0081d8647a08fbedcc986a5f341a609dee57f`  
		Last Modified: Tue, 18 Mar 2025 07:59:54 GMT  
		Size: 93.7 MB (93695853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf52800b2085b98c149b26b53961a983a0f3c8f51f7eccf4563d07df48f1e71`  
		Last Modified: Tue, 18 Mar 2025 07:59:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:3e771a04d025fcff669afe1c6057c7e3ab2abdd5ea94733376df0ca141f20354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ccdce77592a77235216072f3f78a043986322097813e6de7c33288ede19338`

```dockerfile
```

-	Layers:
	-	`sha256:ff3ece614268901dd8d296c346d0b993a7df64009c4b4f8d01b45d4b901f843a`  
		Last Modified: Tue, 18 Mar 2025 07:59:52 GMT  
		Size: 2.6 MB (2624167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6856b13198cac42997e28a3c83b7808ed45e0b94f581d345737637ae63b6b56e`  
		Last Modified: Tue, 18 Mar 2025 07:59:52 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:9a3522c6aa90e185fc503baf6f428c60c49428dd7a029d78824936e82a8b0dd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:3a3c7b620559ce83c17ba4fae6ce0ff24026b26ea831a160a6c36cfbbd7ded02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125353882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed69cbffdb51187de2b2cd07c4f99ee213df9d0c2ecaee0dd9c170ecc13e2f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a9952e19ffe8de7b43dee788754c3e7aa7e006bc48a2020ed20e137bf284a`  
		Last Modified: Mon, 17 Mar 2025 23:12:36 GMT  
		Size: 97.1 MB (97147955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65f3af15e5991942024404577817f290093c6cc73c306b9b5457f2e02b74b93`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:1850adedac86f3aaefac09cea3a9bf16e6d3faaf143e6df5a12f8c54b4ba63e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49132a604e0a3fbf56b6e41f5f2cb3693d6d59293956a829115ae05fda234a5c`

```dockerfile
```

-	Layers:
	-	`sha256:befe33bf1c163a3f2dda4585fe0106984a68e38ad4a383afdfa27b52ce198b3e`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 2.6 MB (2623911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcc2a157ead6fa4ad55697a82730fb68e1dae6fd5969bd09d71803b77270723`  
		Last Modified: Mon, 17 Mar 2025 23:12:34 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c7621498c23d6575fa7853cd279ea1dc5eb3dcea077a0931d30d1ac656b6e897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121740954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0013969d3ded04ae09073cf79ec202ecdc60b7ab8706b22bf872023e4a845a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739b932bb5a341ed63b5cfe55c0081d8647a08fbedcc986a5f341a609dee57f`  
		Last Modified: Tue, 18 Mar 2025 07:59:54 GMT  
		Size: 93.7 MB (93695853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf52800b2085b98c149b26b53961a983a0f3c8f51f7eccf4563d07df48f1e71`  
		Last Modified: Tue, 18 Mar 2025 07:59:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:3e771a04d025fcff669afe1c6057c7e3ab2abdd5ea94733376df0ca141f20354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ccdce77592a77235216072f3f78a043986322097813e6de7c33288ede19338`

```dockerfile
```

-	Layers:
	-	`sha256:ff3ece614268901dd8d296c346d0b993a7df64009c4b4f8d01b45d4b901f843a`  
		Last Modified: Tue, 18 Mar 2025 07:59:52 GMT  
		Size: 2.6 MB (2624167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6856b13198cac42997e28a3c83b7808ed45e0b94f581d345737637ae63b6b56e`  
		Last Modified: Tue, 18 Mar 2025 07:59:52 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:c0831dfc8b411ea901cec960525432821f0798b5980f1300a2fe1127aaefa2d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:cb6640b2cc2a6fd938af12ca28284feda2811b243139a74c770babc810a1b6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105481388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f8d7b8b37cb2d5cb5a99d26d44be25b5631a731da2afff01e4e08d5567daad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c3849f578c0c6628fc4790503844c09b092d93df58d4331d42113f967e8b8`  
		Last Modified: Tue, 25 Mar 2025 20:56:58 GMT  
		Size: 77.3 MB (77275457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb94386d02a536e149af06ecfc91169322972534411c08733b7b5b8861dd748`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:2b098e62542b78e7b93b95c168e7a262e0a1f0b9b56e43c2acedb24750f8667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54dbbaff263bd4cb5d85d550be78347e918197b384fdb7e474de729c4cc44adf`

```dockerfile
```

-	Layers:
	-	`sha256:6ee6a80a1686bfa83cc5201b0f4e65fe9bbc5329b754d7bfddabdfe55891a84d`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 2.6 MB (2614518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c060c3bd2f51e444da4435471fa7dcbf9b6cec2208c47ae91470ad8704edd8e2`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8cf1b426db7e7b444056244992bc0bda791705810b43f55c06f76890b3453bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102595006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dd45e38223a6d7b65e7d9f86faec5511eaae2bcf6e3d6a0a341e6832144161`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f89ccda1ed8650a3ce57d4f64f40541c7438e3e20c3967b1898151b0dc8b016`  
		Last Modified: Tue, 25 Mar 2025 20:56:30 GMT  
		Size: 74.5 MB (74549906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e882a7b9f79bc29aea9b1e799d4d24e0d523c12f4eb8b7d7b04042f3f3ddd557`  
		Last Modified: Tue, 25 Mar 2025 20:56:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:4182e9290f6c5d562eaf44a1332319a894bd3f84e59ea763987ec8aa85ba489a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10894c2d4c92e83b2eae115c549fd59eabe234e35158d4a7f748c47932c7337`

```dockerfile
```

-	Layers:
	-	`sha256:9842809cf7c0ee1dc90936881035a5864f209b40b0cfc3f6ba51da5ee90e0947`  
		Last Modified: Tue, 25 Mar 2025 20:56:28 GMT  
		Size: 2.6 MB (2614798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccb0f704c5eb3254a6d6684a10c41a0f381e7b29d2035422a8bd27d86ea28ba`  
		Last Modified: Tue, 25 Mar 2025 20:56:28 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.6`

```console
$ docker pull emqx@sha256:c0831dfc8b411ea901cec960525432821f0798b5980f1300a2fe1127aaefa2d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.6` - linux; amd64

```console
$ docker pull emqx@sha256:cb6640b2cc2a6fd938af12ca28284feda2811b243139a74c770babc810a1b6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105481388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f8d7b8b37cb2d5cb5a99d26d44be25b5631a731da2afff01e4e08d5567daad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c3849f578c0c6628fc4790503844c09b092d93df58d4331d42113f967e8b8`  
		Last Modified: Tue, 25 Mar 2025 20:56:58 GMT  
		Size: 77.3 MB (77275457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb94386d02a536e149af06ecfc91169322972534411c08733b7b5b8861dd748`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.6` - unknown; unknown

```console
$ docker pull emqx@sha256:2b098e62542b78e7b93b95c168e7a262e0a1f0b9b56e43c2acedb24750f8667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54dbbaff263bd4cb5d85d550be78347e918197b384fdb7e474de729c4cc44adf`

```dockerfile
```

-	Layers:
	-	`sha256:6ee6a80a1686bfa83cc5201b0f4e65fe9bbc5329b754d7bfddabdfe55891a84d`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 2.6 MB (2614518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c060c3bd2f51e444da4435471fa7dcbf9b6cec2208c47ae91470ad8704edd8e2`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8cf1b426db7e7b444056244992bc0bda791705810b43f55c06f76890b3453bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102595006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dd45e38223a6d7b65e7d9f86faec5511eaae2bcf6e3d6a0a341e6832144161`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f89ccda1ed8650a3ce57d4f64f40541c7438e3e20c3967b1898151b0dc8b016`  
		Last Modified: Tue, 25 Mar 2025 20:56:30 GMT  
		Size: 74.5 MB (74549906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e882a7b9f79bc29aea9b1e799d4d24e0d523c12f4eb8b7d7b04042f3f3ddd557`  
		Last Modified: Tue, 25 Mar 2025 20:56:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.6` - unknown; unknown

```console
$ docker pull emqx@sha256:4182e9290f6c5d562eaf44a1332319a894bd3f84e59ea763987ec8aa85ba489a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10894c2d4c92e83b2eae115c549fd59eabe234e35158d4a7f748c47932c7337`

```dockerfile
```

-	Layers:
	-	`sha256:9842809cf7c0ee1dc90936881035a5864f209b40b0cfc3f6ba51da5ee90e0947`  
		Last Modified: Tue, 25 Mar 2025 20:56:28 GMT  
		Size: 2.6 MB (2614798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccb0f704c5eb3254a6d6684a10c41a0f381e7b29d2035422a8bd27d86ea28ba`  
		Last Modified: Tue, 25 Mar 2025 20:56:28 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:c0831dfc8b411ea901cec960525432821f0798b5980f1300a2fe1127aaefa2d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:cb6640b2cc2a6fd938af12ca28284feda2811b243139a74c770babc810a1b6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105481388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f8d7b8b37cb2d5cb5a99d26d44be25b5631a731da2afff01e4e08d5567daad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c3849f578c0c6628fc4790503844c09b092d93df58d4331d42113f967e8b8`  
		Last Modified: Tue, 25 Mar 2025 20:56:58 GMT  
		Size: 77.3 MB (77275457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb94386d02a536e149af06ecfc91169322972534411c08733b7b5b8861dd748`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:2b098e62542b78e7b93b95c168e7a262e0a1f0b9b56e43c2acedb24750f8667e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54dbbaff263bd4cb5d85d550be78347e918197b384fdb7e474de729c4cc44adf`

```dockerfile
```

-	Layers:
	-	`sha256:6ee6a80a1686bfa83cc5201b0f4e65fe9bbc5329b754d7bfddabdfe55891a84d`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 2.6 MB (2614518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c060c3bd2f51e444da4435471fa7dcbf9b6cec2208c47ae91470ad8704edd8e2`  
		Last Modified: Tue, 25 Mar 2025 20:56:55 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8cf1b426db7e7b444056244992bc0bda791705810b43f55c06f76890b3453bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102595006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dd45e38223a6d7b65e7d9f86faec5511eaae2bcf6e3d6a0a341e6832144161`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f89ccda1ed8650a3ce57d4f64f40541c7438e3e20c3967b1898151b0dc8b016`  
		Last Modified: Tue, 25 Mar 2025 20:56:30 GMT  
		Size: 74.5 MB (74549906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e882a7b9f79bc29aea9b1e799d4d24e0d523c12f4eb8b7d7b04042f3f3ddd557`  
		Last Modified: Tue, 25 Mar 2025 20:56:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:4182e9290f6c5d562eaf44a1332319a894bd3f84e59ea763987ec8aa85ba489a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10894c2d4c92e83b2eae115c549fd59eabe234e35158d4a7f748c47932c7337`

```dockerfile
```

-	Layers:
	-	`sha256:9842809cf7c0ee1dc90936881035a5864f209b40b0cfc3f6ba51da5ee90e0947`  
		Last Modified: Tue, 25 Mar 2025 20:56:28 GMT  
		Size: 2.6 MB (2614798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccb0f704c5eb3254a6d6684a10c41a0f381e7b29d2035422a8bd27d86ea28ba`  
		Last Modified: Tue, 25 Mar 2025 20:56:28 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json
