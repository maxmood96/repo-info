<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.5`](#emqx585)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:9fa8d833ae81578336857b98c88487d55552a724326158b84fef3195257f3624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:8e2bfdc3e7a5b34ca4de77f33753f313eb408fe31a5d519864526d2b38a71db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105462134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4543f20e9b7061d572ed7e9cb889b906e6d473a3f170dfeb38d5aa51b219fbc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54478d76cb26be89195325246b71120e537470a900e575f05745d64fa027f`  
		Last Modified: Mon, 17 Mar 2025 23:12:32 GMT  
		Size: 77.3 MB (77256208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a05e78475e00caa1853725f2e3a7709df919a6a30aaf32bb7eaa8dbf808dc`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:5b2b9f1594ffef5f1442e1683ab1842885a42c5a57e04c047757b5ab28fca42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2291c049078b0bb04b3e8c5c956fb6cf33ee5364baa4ca1f921a4cb7021f746e`

```dockerfile
```

-	Layers:
	-	`sha256:a9f8808066765e582d149ad0b40fc53bc11f7c3513b8e38be07a8765def4ac70`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 2.6 MB (2614515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96ae50fc2db336889bab96ffe2c6a88fec66ac8fbf7b0090283339f807d0363`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d67cc9302b578163e1901e4c5b7b65ac9fa72f4d5a112acb742625341d3c16ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102567593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7184ce0208ab974aa6b381f1be33154ea9a5b2e6d37e2172080f6b07dc7ca3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0303ddb983801e0cf25961f72fc143154f9173fd4575f68f9e0f272994ccd811`  
		Last Modified: Tue, 18 Mar 2025 08:04:26 GMT  
		Size: 74.5 MB (74522492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b6cbcfb5acab7afdc31452fa9ebe39dd5ae8221224d24ff0ae72bba5987c33`  
		Last Modified: Tue, 18 Mar 2025 08:04:23 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:3e30445f10d7772dcf40624a9ee06e0684321299af6b05a0b90d9b03f82f5b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb1021e48f73a33cea5422aceb3536403f84f9a3cbc02ee5594da8e740a6839`

```dockerfile
```

-	Layers:
	-	`sha256:14a0f25b35c5d6f61a4c88d6a7f04f4e6cc4f7f5bba2722507e99ff6ce432bdc`  
		Last Modified: Tue, 18 Mar 2025 08:04:24 GMT  
		Size: 2.6 MB (2614795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363c625d7a79a6ce4fda10f08d2021a6b220b4e8f960645b49cf4d32ed6ca146`  
		Last Modified: Tue, 18 Mar 2025 08:04:23 GMT  
		Size: 12.6 KB (12633 bytes)  
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
$ docker pull emqx@sha256:9fa8d833ae81578336857b98c88487d55552a724326158b84fef3195257f3624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:8e2bfdc3e7a5b34ca4de77f33753f313eb408fe31a5d519864526d2b38a71db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105462134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4543f20e9b7061d572ed7e9cb889b906e6d473a3f170dfeb38d5aa51b219fbc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54478d76cb26be89195325246b71120e537470a900e575f05745d64fa027f`  
		Last Modified: Mon, 17 Mar 2025 23:12:32 GMT  
		Size: 77.3 MB (77256208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a05e78475e00caa1853725f2e3a7709df919a6a30aaf32bb7eaa8dbf808dc`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:5b2b9f1594ffef5f1442e1683ab1842885a42c5a57e04c047757b5ab28fca42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2291c049078b0bb04b3e8c5c956fb6cf33ee5364baa4ca1f921a4cb7021f746e`

```dockerfile
```

-	Layers:
	-	`sha256:a9f8808066765e582d149ad0b40fc53bc11f7c3513b8e38be07a8765def4ac70`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 2.6 MB (2614515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96ae50fc2db336889bab96ffe2c6a88fec66ac8fbf7b0090283339f807d0363`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d67cc9302b578163e1901e4c5b7b65ac9fa72f4d5a112acb742625341d3c16ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102567593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7184ce0208ab974aa6b381f1be33154ea9a5b2e6d37e2172080f6b07dc7ca3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0303ddb983801e0cf25961f72fc143154f9173fd4575f68f9e0f272994ccd811`  
		Last Modified: Tue, 18 Mar 2025 08:04:26 GMT  
		Size: 74.5 MB (74522492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b6cbcfb5acab7afdc31452fa9ebe39dd5ae8221224d24ff0ae72bba5987c33`  
		Last Modified: Tue, 18 Mar 2025 08:04:23 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:3e30445f10d7772dcf40624a9ee06e0684321299af6b05a0b90d9b03f82f5b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb1021e48f73a33cea5422aceb3536403f84f9a3cbc02ee5594da8e740a6839`

```dockerfile
```

-	Layers:
	-	`sha256:14a0f25b35c5d6f61a4c88d6a7f04f4e6cc4f7f5bba2722507e99ff6ce432bdc`  
		Last Modified: Tue, 18 Mar 2025 08:04:24 GMT  
		Size: 2.6 MB (2614795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363c625d7a79a6ce4fda10f08d2021a6b220b4e8f960645b49cf4d32ed6ca146`  
		Last Modified: Tue, 18 Mar 2025 08:04:23 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.5`

```console
$ docker pull emqx@sha256:9fa8d833ae81578336857b98c88487d55552a724326158b84fef3195257f3624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.5` - linux; amd64

```console
$ docker pull emqx@sha256:8e2bfdc3e7a5b34ca4de77f33753f313eb408fe31a5d519864526d2b38a71db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105462134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4543f20e9b7061d572ed7e9cb889b906e6d473a3f170dfeb38d5aa51b219fbc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54478d76cb26be89195325246b71120e537470a900e575f05745d64fa027f`  
		Last Modified: Mon, 17 Mar 2025 23:12:32 GMT  
		Size: 77.3 MB (77256208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a05e78475e00caa1853725f2e3a7709df919a6a30aaf32bb7eaa8dbf808dc`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.5` - unknown; unknown

```console
$ docker pull emqx@sha256:5b2b9f1594ffef5f1442e1683ab1842885a42c5a57e04c047757b5ab28fca42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2291c049078b0bb04b3e8c5c956fb6cf33ee5364baa4ca1f921a4cb7021f746e`

```dockerfile
```

-	Layers:
	-	`sha256:a9f8808066765e582d149ad0b40fc53bc11f7c3513b8e38be07a8765def4ac70`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 2.6 MB (2614515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96ae50fc2db336889bab96ffe2c6a88fec66ac8fbf7b0090283339f807d0363`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d67cc9302b578163e1901e4c5b7b65ac9fa72f4d5a112acb742625341d3c16ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102567593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7184ce0208ab974aa6b381f1be33154ea9a5b2e6d37e2172080f6b07dc7ca3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0303ddb983801e0cf25961f72fc143154f9173fd4575f68f9e0f272994ccd811`  
		Last Modified: Tue, 18 Mar 2025 08:04:26 GMT  
		Size: 74.5 MB (74522492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b6cbcfb5acab7afdc31452fa9ebe39dd5ae8221224d24ff0ae72bba5987c33`  
		Last Modified: Tue, 18 Mar 2025 08:04:23 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.5` - unknown; unknown

```console
$ docker pull emqx@sha256:3e30445f10d7772dcf40624a9ee06e0684321299af6b05a0b90d9b03f82f5b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb1021e48f73a33cea5422aceb3536403f84f9a3cbc02ee5594da8e740a6839`

```dockerfile
```

-	Layers:
	-	`sha256:14a0f25b35c5d6f61a4c88d6a7f04f4e6cc4f7f5bba2722507e99ff6ce432bdc`  
		Last Modified: Tue, 18 Mar 2025 08:04:24 GMT  
		Size: 2.6 MB (2614795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363c625d7a79a6ce4fda10f08d2021a6b220b4e8f960645b49cf4d32ed6ca146`  
		Last Modified: Tue, 18 Mar 2025 08:04:23 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:9fa8d833ae81578336857b98c88487d55552a724326158b84fef3195257f3624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:8e2bfdc3e7a5b34ca4de77f33753f313eb408fe31a5d519864526d2b38a71db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105462134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4543f20e9b7061d572ed7e9cb889b906e6d473a3f170dfeb38d5aa51b219fbc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54478d76cb26be89195325246b71120e537470a900e575f05745d64fa027f`  
		Last Modified: Mon, 17 Mar 2025 23:12:32 GMT  
		Size: 77.3 MB (77256208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a05e78475e00caa1853725f2e3a7709df919a6a30aaf32bb7eaa8dbf808dc`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:5b2b9f1594ffef5f1442e1683ab1842885a42c5a57e04c047757b5ab28fca42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2291c049078b0bb04b3e8c5c956fb6cf33ee5364baa4ca1f921a4cb7021f746e`

```dockerfile
```

-	Layers:
	-	`sha256:a9f8808066765e582d149ad0b40fc53bc11f7c3513b8e38be07a8765def4ac70`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 2.6 MB (2614515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96ae50fc2db336889bab96ffe2c6a88fec66ac8fbf7b0090283339f807d0363`  
		Last Modified: Mon, 17 Mar 2025 23:12:31 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d67cc9302b578163e1901e4c5b7b65ac9fa72f4d5a112acb742625341d3c16ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102567593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7184ce0208ab974aa6b381f1be33154ea9a5b2e6d37e2172080f6b07dc7ca3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 26 Feb 2025 08:28:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 08:28:38 GMT
ENV EMQX_VERSION=5.8.5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV AMD64_SHA256=311fd8f446c2d89474f879643f3c5860fbf8cb4e414e6652f8b61c0608da5628
# Wed, 26 Feb 2025 08:28:38 GMT
ENV ARM64_SHA256=26f3f620c41522f0795911c814160512f455013dc7d9555348c2c457b6cf48f5
# Wed, 26 Feb 2025 08:28:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 26 Feb 2025 08:28:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
WORKDIR /opt/emqx
# Wed, 26 Feb 2025 08:28:38 GMT
USER emqx
# Wed, 26 Feb 2025 08:28:38 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 26 Feb 2025 08:28:38 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 26 Feb 2025 08:28:38 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 26 Feb 2025 08:28:38 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 26 Feb 2025 08:28:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0303ddb983801e0cf25961f72fc143154f9173fd4575f68f9e0f272994ccd811`  
		Last Modified: Tue, 18 Mar 2025 08:04:26 GMT  
		Size: 74.5 MB (74522492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b6cbcfb5acab7afdc31452fa9ebe39dd5ae8221224d24ff0ae72bba5987c33`  
		Last Modified: Tue, 18 Mar 2025 08:04:23 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:3e30445f10d7772dcf40624a9ee06e0684321299af6b05a0b90d9b03f82f5b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb1021e48f73a33cea5422aceb3536403f84f9a3cbc02ee5594da8e740a6839`

```dockerfile
```

-	Layers:
	-	`sha256:14a0f25b35c5d6f61a4c88d6a7f04f4e6cc4f7f5bba2722507e99ff6ce432bdc`  
		Last Modified: Tue, 18 Mar 2025 08:04:24 GMT  
		Size: 2.6 MB (2614795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363c625d7a79a6ce4fda10f08d2021a6b220b4e8f960645b49cf4d32ed6ca146`  
		Last Modified: Tue, 18 Mar 2025 08:04:23 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
