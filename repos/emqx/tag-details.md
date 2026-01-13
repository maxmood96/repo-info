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
$ docker pull emqx@sha256:1a8b6b757a5d19d20924790e3177754512ab407389cb65ca09d41794476686ae
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
$ docker pull emqx@sha256:2afc009a32aad6b0353480873027ef2d0b093bc18824d3cd5c1bdf57b2ae9bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106665479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab77492e6236c24f45b95cce628ae014e396f0145ae841a5217865ef6a9b6edd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:28 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae82769fae53b576f967b5aaba216c788f7e834bb01daa6b9ec3353811e3c30b`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 76.5 MB (76530374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d537084054513975c6621d3f551d5c25fd778faaa9e88e6b1c9e5c501600d`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:18acb9d20698d0fa54c2b5098b6cbe60da3bd7e0f9e4a6f7bb54e2e29dce093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2867c9f7e497ac4ba35cd80100699ce16be85ea61ce383bea338e29500982e`

```dockerfile
```

-	Layers:
	-	`sha256:83bbe8e83cc379af23032e5d9e0bfaabb2eda78d0e6664fb5bf2619e0044ee2f`  
		Last Modified: Tue, 13 Jan 2026 03:28:49 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41188b6e930ba00d90dd4040a070af16891f6c9b8cd375e13e82853587235e83`  
		Last Modified: Tue, 13 Jan 2026 03:28:50 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:7bcf778d0a997503bb1a6dc86921da21b1c3ab42ac7d74f1a660343d0e2d3fce
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
$ docker pull emqx@sha256:38879dd3f65d644b282b35f7a75905548c1d41deb3a8ad687ef6e0138a780723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121825284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712c291c7949a90bf628a0565e9e020f9773ece818e6836f7737ac7e6806318c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:27 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:27 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:27 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:27 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:27 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d84c99c6e08fef0acbfe90da1407373d98ff31c4d0fbaeef0e33ba8c533e9`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 93.7 MB (93716331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5bea8798303aa2d61b52b47f2b48c318068d7e46c3c24e3ae614d2a5019f73`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:71b2128e5182c03e7eb6db846f0dfa5c7d10a7fab755ead3b2f526e1147f0e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19dbec7c55d8b5f04b7aec9d0709d1cd662e2dc8e0837f9fbf3e68294fdaeb9`

```dockerfile
```

-	Layers:
	-	`sha256:dc855847bb841400f02ae4a30c97505baa06284c736e16eadfc46e7e23097e50`  
		Last Modified: Tue, 13 Jan 2026 03:28:52 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45b92534341307f98e5afeedb6ed59f040c60f5ac76a841ba5affe92c39fcdb`  
		Last Modified: Tue, 13 Jan 2026 03:28:53 GMT  
		Size: 12.0 KB (11987 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:7bcf778d0a997503bb1a6dc86921da21b1c3ab42ac7d74f1a660343d0e2d3fce
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
$ docker pull emqx@sha256:38879dd3f65d644b282b35f7a75905548c1d41deb3a8ad687ef6e0138a780723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121825284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712c291c7949a90bf628a0565e9e020f9773ece818e6836f7737ac7e6806318c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:27 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:27 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:27 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:27 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:27 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d84c99c6e08fef0acbfe90da1407373d98ff31c4d0fbaeef0e33ba8c533e9`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 93.7 MB (93716331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5bea8798303aa2d61b52b47f2b48c318068d7e46c3c24e3ae614d2a5019f73`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:71b2128e5182c03e7eb6db846f0dfa5c7d10a7fab755ead3b2f526e1147f0e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19dbec7c55d8b5f04b7aec9d0709d1cd662e2dc8e0837f9fbf3e68294fdaeb9`

```dockerfile
```

-	Layers:
	-	`sha256:dc855847bb841400f02ae4a30c97505baa06284c736e16eadfc46e7e23097e50`  
		Last Modified: Tue, 13 Jan 2026 03:28:52 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45b92534341307f98e5afeedb6ed59f040c60f5ac76a841ba5affe92c39fcdb`  
		Last Modified: Tue, 13 Jan 2026 03:28:53 GMT  
		Size: 12.0 KB (11987 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:1a8b6b757a5d19d20924790e3177754512ab407389cb65ca09d41794476686ae
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
$ docker pull emqx@sha256:2afc009a32aad6b0353480873027ef2d0b093bc18824d3cd5c1bdf57b2ae9bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106665479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab77492e6236c24f45b95cce628ae014e396f0145ae841a5217865ef6a9b6edd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:28 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae82769fae53b576f967b5aaba216c788f7e834bb01daa6b9ec3353811e3c30b`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 76.5 MB (76530374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d537084054513975c6621d3f551d5c25fd778faaa9e88e6b1c9e5c501600d`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:18acb9d20698d0fa54c2b5098b6cbe60da3bd7e0f9e4a6f7bb54e2e29dce093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2867c9f7e497ac4ba35cd80100699ce16be85ea61ce383bea338e29500982e`

```dockerfile
```

-	Layers:
	-	`sha256:83bbe8e83cc379af23032e5d9e0bfaabb2eda78d0e6664fb5bf2619e0044ee2f`  
		Last Modified: Tue, 13 Jan 2026 03:28:49 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41188b6e930ba00d90dd4040a070af16891f6c9b8cd375e13e82853587235e83`  
		Last Modified: Tue, 13 Jan 2026 03:28:50 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:1a8b6b757a5d19d20924790e3177754512ab407389cb65ca09d41794476686ae
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
$ docker pull emqx@sha256:2afc009a32aad6b0353480873027ef2d0b093bc18824d3cd5c1bdf57b2ae9bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106665479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab77492e6236c24f45b95cce628ae014e396f0145ae841a5217865ef6a9b6edd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:28 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae82769fae53b576f967b5aaba216c788f7e834bb01daa6b9ec3353811e3c30b`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 76.5 MB (76530374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d537084054513975c6621d3f551d5c25fd778faaa9e88e6b1c9e5c501600d`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:18acb9d20698d0fa54c2b5098b6cbe60da3bd7e0f9e4a6f7bb54e2e29dce093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2867c9f7e497ac4ba35cd80100699ce16be85ea61ce383bea338e29500982e`

```dockerfile
```

-	Layers:
	-	`sha256:83bbe8e83cc379af23032e5d9e0bfaabb2eda78d0e6664fb5bf2619e0044ee2f`  
		Last Modified: Tue, 13 Jan 2026 03:28:49 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41188b6e930ba00d90dd4040a070af16891f6c9b8cd375e13e82853587235e83`  
		Last Modified: Tue, 13 Jan 2026 03:28:50 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:1a8b6b757a5d19d20924790e3177754512ab407389cb65ca09d41794476686ae
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
$ docker pull emqx@sha256:2afc009a32aad6b0353480873027ef2d0b093bc18824d3cd5c1bdf57b2ae9bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106665479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab77492e6236c24f45b95cce628ae014e396f0145ae841a5217865ef6a9b6edd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:28 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae82769fae53b576f967b5aaba216c788f7e834bb01daa6b9ec3353811e3c30b`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 76.5 MB (76530374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d537084054513975c6621d3f551d5c25fd778faaa9e88e6b1c9e5c501600d`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:18acb9d20698d0fa54c2b5098b6cbe60da3bd7e0f9e4a6f7bb54e2e29dce093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2867c9f7e497ac4ba35cd80100699ce16be85ea61ce383bea338e29500982e`

```dockerfile
```

-	Layers:
	-	`sha256:83bbe8e83cc379af23032e5d9e0bfaabb2eda78d0e6664fb5bf2619e0044ee2f`  
		Last Modified: Tue, 13 Jan 2026 03:28:49 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41188b6e930ba00d90dd4040a070af16891f6c9b8cd375e13e82853587235e83`  
		Last Modified: Tue, 13 Jan 2026 03:28:50 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
