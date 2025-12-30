<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.8`](#emqx588)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:9058650b64bdd38110038826fe5edff65338cf3853292363d38817080e5a295e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:5e14b71b5688a6bd7dbf3ec2a1b71de168c26950a76785cae362288ecbd86e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7457b8a28f2f7192330e7635feb5890d4066cc7a76237356cf936322e9aa88b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:14:17 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 29 Dec 2025 23:14:17 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 29 Dec 2025 23:14:17 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 29 Dec 2025 23:14:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:14:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:14:17 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:14:17 GMT
USER emqx
# Mon, 29 Dec 2025 23:14:17 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:14:17 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:14:17 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:14:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:14:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ec90c829025d29b21230ebb8a950fc2ebe3f6b75eb570cc51e0ff1b3044c93`  
		Last Modified: Mon, 29 Dec 2025 23:14:54 GMT  
		Size: 78.6 MB (78621595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2f6d3a0dfd06a996b6cd78b46d7f93e1bb5e51ac7682cd3cc48953d6b52235`  
		Last Modified: Mon, 29 Dec 2025 23:14:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:ed6b5f35fd47982a4ede37f81ae1ea16e3e689a3dc921005ecf46e2ec1e62f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96cfdc5bdf40446ae765b468fb0cbd089804b6f42cbb8d348a5af12664e6cb8`

```dockerfile
```

-	Layers:
	-	`sha256:a749a078094d246e6062fd40e2e15cfcfd12d219ca48ad2011d9fb7d00b5838d`  
		Last Modified: Tue, 30 Dec 2025 03:28:27 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43a07883eb3caae343725a4ecf7c48af22a438db5d7d6352c894bb13388c5f1`  
		Last Modified: Tue, 30 Dec 2025 03:28:28 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:93d88ffec675ee2b3904b4cda40d3e389aa90aa5ccd93719decdc6a104ef0078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dd8156939a927179fbd656bcc6813e55fdfb1e93a21aab06f0ff52319c1311`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:14 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 29 Dec 2025 23:15:14 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 29 Dec 2025 23:15:14 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 29 Dec 2025 23:15:14 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:15:14 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:15:14 GMT
USER emqx
# Mon, 29 Dec 2025 23:15:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:15:14 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:15:14 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a597bf78cb38e4f521269eddeab6d75181e9aab61c5744d1daa7c6075816ece`  
		Last Modified: Mon, 29 Dec 2025 23:15:43 GMT  
		Size: 76.5 MB (76530442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22781dd1b0e87eaff66c003d8655285792759e019d3ad9ff0beb129dc7e8bca7`  
		Last Modified: Mon, 29 Dec 2025 23:15:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:b8c01ade6dbc4ffe66907392d14984c5e652577fc9563511dae252c624da0e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208e88da75dd9f12eda9907a8fa962944aa4a8d8b883a310dc42b20936eb1a66`

```dockerfile
```

-	Layers:
	-	`sha256:efba2564538624a3d550cdc5cdc7381797bfabfc59353084276ff329e84d5578`  
		Last Modified: Tue, 30 Dec 2025 03:28:31 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c96eb9aa20a65403f75abd0a9390aac4e762e953493e4908d57c0f4b103ba24`  
		Last Modified: Tue, 30 Dec 2025 03:28:32 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:87cc337fc2d32d4d102bb7444864b0f0030b4d000ec591c044258a7bd10d22bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:489e4fd53330c2220ef1cb2c6b8d00794874e21af315527c54334bae462a129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c371f78f9251cd098442e829923b0b2ba9e3aace78ebd289426028cf1b17f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:15:32 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 29 Dec 2025 23:15:32 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 29 Dec 2025 23:15:32 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 29 Dec 2025 23:15:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:15:32 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:15:32 GMT
USER emqx
# Mon, 29 Dec 2025 23:15:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:15:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:15:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c5d7b7f3bc4c6e5d245d98417404800b515fc340f364c88b66f3e062c6769d`  
		Last Modified: Mon, 29 Dec 2025 23:16:01 GMT  
		Size: 97.2 MB (97155104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf85742d92d21a958da5a0da5443cb7c2d60387cee147a05da503b98f607a9a9`  
		Last Modified: Mon, 29 Dec 2025 23:15:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:5e8e3e912d43545c8ddd81d43f75f988a85f5dd5a910c726a1154ad346864644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648e307a1d04076bea5dd20be9809ae2382b1a578ef364abeada43460368ca96`

```dockerfile
```

-	Layers:
	-	`sha256:87b6e2d8fbfffab7d3ee2fa4f0d4b137ce7539b736c80f34a8785608ef5b7153`  
		Last Modified: Tue, 30 Dec 2025 03:28:35 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb3fcf31165c4055bdf546ce07d85b98c11bcb5946b55014e1ca2894ad37f41`  
		Last Modified: Tue, 30 Dec 2025 03:28:35 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:021f9dcd2c33ff86d62439ee8a77355f40a3e263c697b18fa79c2dce0cadc628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bb4475963469e7de08bbe4da6d49c304f6c52fcb868b7bb5d8ca98b94bb5f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:15:17 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 29 Dec 2025 23:15:17 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 29 Dec 2025 23:15:17 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 29 Dec 2025 23:15:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:15:17 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:15:17 GMT
USER emqx
# Mon, 29 Dec 2025 23:15:17 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:15:17 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:15:17 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c2fb5157a6e26e55434217f2a9ee2681d5daa49d98bca42511312b8c27053`  
		Last Modified: Mon, 29 Dec 2025 23:15:48 GMT  
		Size: 93.7 MB (93715129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4b1f3efa4f0e843dffa7cd2378edc4fb4837e139d5a8f87a9e807ad643890a`  
		Last Modified: Mon, 29 Dec 2025 23:15:42 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:7f2ee7e48d73b4a35d457b54d6139a9c2fe5a37066cb2a724e5e1e083cec2fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb35f6c9422b63cc22f91b9dc42b5c61022c249e2f3463a463eb350aa4c38e2`

```dockerfile
```

-	Layers:
	-	`sha256:37e319812d4f03aa0955388fd4912e5167697007f3e2da8a165e4273cb435e26`  
		Last Modified: Tue, 30 Dec 2025 03:28:39 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:084d418d86a62b4ce31312adede64033df58f8c604e5c998fcf069ad1d0ac53b`  
		Last Modified: Tue, 30 Dec 2025 03:28:40 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:87cc337fc2d32d4d102bb7444864b0f0030b4d000ec591c044258a7bd10d22bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:489e4fd53330c2220ef1cb2c6b8d00794874e21af315527c54334bae462a129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c371f78f9251cd098442e829923b0b2ba9e3aace78ebd289426028cf1b17f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:15:32 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 29 Dec 2025 23:15:32 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 29 Dec 2025 23:15:32 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 29 Dec 2025 23:15:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:15:32 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:15:32 GMT
USER emqx
# Mon, 29 Dec 2025 23:15:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:15:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:15:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c5d7b7f3bc4c6e5d245d98417404800b515fc340f364c88b66f3e062c6769d`  
		Last Modified: Mon, 29 Dec 2025 23:16:01 GMT  
		Size: 97.2 MB (97155104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf85742d92d21a958da5a0da5443cb7c2d60387cee147a05da503b98f607a9a9`  
		Last Modified: Mon, 29 Dec 2025 23:15:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:5e8e3e912d43545c8ddd81d43f75f988a85f5dd5a910c726a1154ad346864644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648e307a1d04076bea5dd20be9809ae2382b1a578ef364abeada43460368ca96`

```dockerfile
```

-	Layers:
	-	`sha256:87b6e2d8fbfffab7d3ee2fa4f0d4b137ce7539b736c80f34a8785608ef5b7153`  
		Last Modified: Tue, 30 Dec 2025 03:28:35 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb3fcf31165c4055bdf546ce07d85b98c11bcb5946b55014e1ca2894ad37f41`  
		Last Modified: Tue, 30 Dec 2025 03:28:35 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:021f9dcd2c33ff86d62439ee8a77355f40a3e263c697b18fa79c2dce0cadc628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bb4475963469e7de08bbe4da6d49c304f6c52fcb868b7bb5d8ca98b94bb5f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:15:17 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 29 Dec 2025 23:15:17 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 29 Dec 2025 23:15:17 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 29 Dec 2025 23:15:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:15:17 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:15:17 GMT
USER emqx
# Mon, 29 Dec 2025 23:15:17 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:15:17 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:15:17 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c2fb5157a6e26e55434217f2a9ee2681d5daa49d98bca42511312b8c27053`  
		Last Modified: Mon, 29 Dec 2025 23:15:48 GMT  
		Size: 93.7 MB (93715129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4b1f3efa4f0e843dffa7cd2378edc4fb4837e139d5a8f87a9e807ad643890a`  
		Last Modified: Mon, 29 Dec 2025 23:15:42 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:7f2ee7e48d73b4a35d457b54d6139a9c2fe5a37066cb2a724e5e1e083cec2fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb35f6c9422b63cc22f91b9dc42b5c61022c249e2f3463a463eb350aa4c38e2`

```dockerfile
```

-	Layers:
	-	`sha256:37e319812d4f03aa0955388fd4912e5167697007f3e2da8a165e4273cb435e26`  
		Last Modified: Tue, 30 Dec 2025 03:28:39 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:084d418d86a62b4ce31312adede64033df58f8c604e5c998fcf069ad1d0ac53b`  
		Last Modified: Tue, 30 Dec 2025 03:28:40 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:9058650b64bdd38110038826fe5edff65338cf3853292363d38817080e5a295e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:5e14b71b5688a6bd7dbf3ec2a1b71de168c26950a76785cae362288ecbd86e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7457b8a28f2f7192330e7635feb5890d4066cc7a76237356cf936322e9aa88b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:14:17 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 29 Dec 2025 23:14:17 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 29 Dec 2025 23:14:17 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 29 Dec 2025 23:14:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:14:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:14:17 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:14:17 GMT
USER emqx
# Mon, 29 Dec 2025 23:14:17 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:14:17 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:14:17 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:14:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:14:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ec90c829025d29b21230ebb8a950fc2ebe3f6b75eb570cc51e0ff1b3044c93`  
		Last Modified: Mon, 29 Dec 2025 23:14:54 GMT  
		Size: 78.6 MB (78621595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2f6d3a0dfd06a996b6cd78b46d7f93e1bb5e51ac7682cd3cc48953d6b52235`  
		Last Modified: Mon, 29 Dec 2025 23:14:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:ed6b5f35fd47982a4ede37f81ae1ea16e3e689a3dc921005ecf46e2ec1e62f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96cfdc5bdf40446ae765b468fb0cbd089804b6f42cbb8d348a5af12664e6cb8`

```dockerfile
```

-	Layers:
	-	`sha256:a749a078094d246e6062fd40e2e15cfcfd12d219ca48ad2011d9fb7d00b5838d`  
		Last Modified: Tue, 30 Dec 2025 03:28:27 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43a07883eb3caae343725a4ecf7c48af22a438db5d7d6352c894bb13388c5f1`  
		Last Modified: Tue, 30 Dec 2025 03:28:28 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:93d88ffec675ee2b3904b4cda40d3e389aa90aa5ccd93719decdc6a104ef0078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dd8156939a927179fbd656bcc6813e55fdfb1e93a21aab06f0ff52319c1311`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:14 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 29 Dec 2025 23:15:14 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 29 Dec 2025 23:15:14 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 29 Dec 2025 23:15:14 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:15:14 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:15:14 GMT
USER emqx
# Mon, 29 Dec 2025 23:15:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:15:14 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:15:14 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a597bf78cb38e4f521269eddeab6d75181e9aab61c5744d1daa7c6075816ece`  
		Last Modified: Mon, 29 Dec 2025 23:15:43 GMT  
		Size: 76.5 MB (76530442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22781dd1b0e87eaff66c003d8655285792759e019d3ad9ff0beb129dc7e8bca7`  
		Last Modified: Mon, 29 Dec 2025 23:15:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:b8c01ade6dbc4ffe66907392d14984c5e652577fc9563511dae252c624da0e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208e88da75dd9f12eda9907a8fa962944aa4a8d8b883a310dc42b20936eb1a66`

```dockerfile
```

-	Layers:
	-	`sha256:efba2564538624a3d550cdc5cdc7381797bfabfc59353084276ff329e84d5578`  
		Last Modified: Tue, 30 Dec 2025 03:28:31 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c96eb9aa20a65403f75abd0a9390aac4e762e953493e4908d57c0f4b103ba24`  
		Last Modified: Tue, 30 Dec 2025 03:28:32 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:9058650b64bdd38110038826fe5edff65338cf3853292363d38817080e5a295e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:5e14b71b5688a6bd7dbf3ec2a1b71de168c26950a76785cae362288ecbd86e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7457b8a28f2f7192330e7635feb5890d4066cc7a76237356cf936322e9aa88b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:14:17 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 29 Dec 2025 23:14:17 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 29 Dec 2025 23:14:17 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 29 Dec 2025 23:14:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:14:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:14:17 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:14:17 GMT
USER emqx
# Mon, 29 Dec 2025 23:14:17 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:14:17 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:14:17 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:14:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:14:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ec90c829025d29b21230ebb8a950fc2ebe3f6b75eb570cc51e0ff1b3044c93`  
		Last Modified: Mon, 29 Dec 2025 23:14:54 GMT  
		Size: 78.6 MB (78621595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2f6d3a0dfd06a996b6cd78b46d7f93e1bb5e51ac7682cd3cc48953d6b52235`  
		Last Modified: Mon, 29 Dec 2025 23:14:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:ed6b5f35fd47982a4ede37f81ae1ea16e3e689a3dc921005ecf46e2ec1e62f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96cfdc5bdf40446ae765b468fb0cbd089804b6f42cbb8d348a5af12664e6cb8`

```dockerfile
```

-	Layers:
	-	`sha256:a749a078094d246e6062fd40e2e15cfcfd12d219ca48ad2011d9fb7d00b5838d`  
		Last Modified: Tue, 30 Dec 2025 03:28:27 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43a07883eb3caae343725a4ecf7c48af22a438db5d7d6352c894bb13388c5f1`  
		Last Modified: Tue, 30 Dec 2025 03:28:28 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:93d88ffec675ee2b3904b4cda40d3e389aa90aa5ccd93719decdc6a104ef0078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dd8156939a927179fbd656bcc6813e55fdfb1e93a21aab06f0ff52319c1311`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:14 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 29 Dec 2025 23:15:14 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 29 Dec 2025 23:15:14 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 29 Dec 2025 23:15:14 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:15:14 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:15:14 GMT
USER emqx
# Mon, 29 Dec 2025 23:15:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:15:14 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:15:14 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a597bf78cb38e4f521269eddeab6d75181e9aab61c5744d1daa7c6075816ece`  
		Last Modified: Mon, 29 Dec 2025 23:15:43 GMT  
		Size: 76.5 MB (76530442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22781dd1b0e87eaff66c003d8655285792759e019d3ad9ff0beb129dc7e8bca7`  
		Last Modified: Mon, 29 Dec 2025 23:15:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:b8c01ade6dbc4ffe66907392d14984c5e652577fc9563511dae252c624da0e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208e88da75dd9f12eda9907a8fa962944aa4a8d8b883a310dc42b20936eb1a66`

```dockerfile
```

-	Layers:
	-	`sha256:efba2564538624a3d550cdc5cdc7381797bfabfc59353084276ff329e84d5578`  
		Last Modified: Tue, 30 Dec 2025 03:28:31 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c96eb9aa20a65403f75abd0a9390aac4e762e953493e4908d57c0f4b103ba24`  
		Last Modified: Tue, 30 Dec 2025 03:28:32 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:9058650b64bdd38110038826fe5edff65338cf3853292363d38817080e5a295e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:5e14b71b5688a6bd7dbf3ec2a1b71de168c26950a76785cae362288ecbd86e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7457b8a28f2f7192330e7635feb5890d4066cc7a76237356cf936322e9aa88b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:14:17 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 29 Dec 2025 23:14:17 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 29 Dec 2025 23:14:17 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 29 Dec 2025 23:14:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:14:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:14:17 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:14:17 GMT
USER emqx
# Mon, 29 Dec 2025 23:14:17 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:14:17 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:14:17 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:14:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:14:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ec90c829025d29b21230ebb8a950fc2ebe3f6b75eb570cc51e0ff1b3044c93`  
		Last Modified: Mon, 29 Dec 2025 23:14:54 GMT  
		Size: 78.6 MB (78621595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2f6d3a0dfd06a996b6cd78b46d7f93e1bb5e51ac7682cd3cc48953d6b52235`  
		Last Modified: Mon, 29 Dec 2025 23:14:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:ed6b5f35fd47982a4ede37f81ae1ea16e3e689a3dc921005ecf46e2ec1e62f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96cfdc5bdf40446ae765b468fb0cbd089804b6f42cbb8d348a5af12664e6cb8`

```dockerfile
```

-	Layers:
	-	`sha256:a749a078094d246e6062fd40e2e15cfcfd12d219ca48ad2011d9fb7d00b5838d`  
		Last Modified: Tue, 30 Dec 2025 03:28:27 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43a07883eb3caae343725a4ecf7c48af22a438db5d7d6352c894bb13388c5f1`  
		Last Modified: Tue, 30 Dec 2025 03:28:28 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:93d88ffec675ee2b3904b4cda40d3e389aa90aa5ccd93719decdc6a104ef0078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dd8156939a927179fbd656bcc6813e55fdfb1e93a21aab06f0ff52319c1311`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:14 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 29 Dec 2025 23:15:14 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 29 Dec 2025 23:15:14 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 29 Dec 2025 23:15:14 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 29 Dec 2025 23:15:14 GMT
WORKDIR /opt/emqx
# Mon, 29 Dec 2025 23:15:14 GMT
USER emqx
# Mon, 29 Dec 2025 23:15:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 29 Dec 2025 23:15:14 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 29 Dec 2025 23:15:14 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 29 Dec 2025 23:15:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:15:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a597bf78cb38e4f521269eddeab6d75181e9aab61c5744d1daa7c6075816ece`  
		Last Modified: Mon, 29 Dec 2025 23:15:43 GMT  
		Size: 76.5 MB (76530442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22781dd1b0e87eaff66c003d8655285792759e019d3ad9ff0beb129dc7e8bca7`  
		Last Modified: Mon, 29 Dec 2025 23:15:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:b8c01ade6dbc4ffe66907392d14984c5e652577fc9563511dae252c624da0e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208e88da75dd9f12eda9907a8fa962944aa4a8d8b883a310dc42b20936eb1a66`

```dockerfile
```

-	Layers:
	-	`sha256:efba2564538624a3d550cdc5cdc7381797bfabfc59353084276ff329e84d5578`  
		Last Modified: Tue, 30 Dec 2025 03:28:31 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c96eb9aa20a65403f75abd0a9390aac4e762e953493e4908d57c0f4b103ba24`  
		Last Modified: Tue, 30 Dec 2025 03:28:32 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
