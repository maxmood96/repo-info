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
$ docker pull emqx@sha256:84d10a0b8f24af741eefbf04d4d14177fd8b1c7cb3b8522ca23be67d3c239873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:578367e3b134ccee09f144991fefea34adee25ee97cd0b781a41c2ee6060e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105503846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0485699654555defd6d0ec269e3fe50075da3c9aa4780b36812653eeb8843eaa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb219db5e43313ed9ec9589a7b54567cba14103a3b8219c5e521cb88c1b9ec5`  
		Last Modified: Tue, 08 Apr 2025 01:11:43 GMT  
		Size: 77.3 MB (77275522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57db8344b12cbba58696f6e2510f27c7554fb3e0a0531768914c286870519076`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:8bff4edc918aa2df52f4d02e7cf187b1f6131a924688b787f599511a9e9e98d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af578e13d0fd692752dcce8c8b3cd0e481edc29aa262156cda5ed46a860c910`

```dockerfile
```

-	Layers:
	-	`sha256:b134a4028e6b55edbc72e076200a426d25324ba6356f8ee05b0bd147fe5e14f6`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 2.6 MB (2615858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6421d9a5cdbb04aadd15c6d5bf47e48030dab39f42c9ac0e7520c44715a95305`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8a32981b49ffb46c283fbb57234e3d3470e4bb8bbc262bcf9f034d762e4b7827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102617191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb15a5705f3d6ef0c9b6135303fbcd84279c101cc45479f4388cd96affb992e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709f6200b07d9e377ff2fa7ca8e65301f3a42dd8428c4e12692d15198dc9de79`  
		Last Modified: Tue, 08 Apr 2025 01:14:56 GMT  
		Size: 74.5 MB (74549808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d116251da89092fb32e21e23b522a4d70f06d93629aacb33631e02b9f6f29d`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:1a9a71b8d9ed61a0671d19b0a76817f8756bd6015d135af7343c54e19f5eef0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a67ff0de8488af70c0646e31652f49099c78a122b83a6dbd3df718f47a81695`

```dockerfile
```

-	Layers:
	-	`sha256:55599efb4a3747324f8fd962c1ef6997b8ecd285f4d52038144a805e5ec01aca`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 2.6 MB (2616138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9dae3c4edcc505a293f2641932615dc69315833967bca1dd8a7d6e99ce7e0d`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:b587bbbbb7d4f51d0fd90b30536c82eeae2dd049a81a060bd8dad2c3796afb3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:9b24a1e4aed44d7791f733fc494df697e3153f30dc1da148150bdbea88a9785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125376241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444ac034fbac1d7c4221b7d9604fdffb9e5fc82995ad891e3677dec392090961`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87a5df34960a5366e891273aa5d596bd30678b8c383ba9841fca14be0ba6d1d`  
		Last Modified: Tue, 08 Apr 2025 01:11:43 GMT  
		Size: 97.1 MB (97147920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ae77bb4a4a708ca03f38b05a88fa906b13e8d77fff5677c1fa059e8f351344`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:1230715d812301a4f2ab3b0be04c97607f655a70350d47107421f6bdb66b1d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f74d5344b6368e711babfb8636abce4c9547fa85d2b66225882f8c0d3920d49`

```dockerfile
```

-	Layers:
	-	`sha256:5f3339a44a68747232c184cf536549435805c8cb326493fac2928fcc2f3b0ff5`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 2.6 MB (2625251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277b688fd5916a8a95d4c658c1d06a3b17c8126c05a585cce5fe7994b0707440`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c44503c13c46cf7f066c7927695e1dd362cbe99da5b87ee6023cfc0e00a1dced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121763175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6191f9b69418d2a33cbc97c29a598d3a54b10441b57fc7a679ed43a1f1e6fd1f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36550bbea26618210509c53259c59b26864ae5d7e1106cd7ee91bb31cfa3620f`  
		Last Modified: Tue, 08 Apr 2025 01:14:21 GMT  
		Size: 93.7 MB (93695791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a2b1573419950a7bf6f68c6715f908636e466c5804fa65a16696928d683079`  
		Last Modified: Tue, 08 Apr 2025 01:14:18 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:47b61ac75f5fb4fa983382a317e10c568045ad94389232c05a14e5011bab8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378586d6f846a9974f909f89483f93033fbbee6a2bb3dd2ab4cac4283c312c72`

```dockerfile
```

-	Layers:
	-	`sha256:b5c9abeeaf13f739e971b890c2013f850067040a56c196ad019b340f4916353c`  
		Last Modified: Tue, 08 Apr 2025 01:14:18 GMT  
		Size: 2.6 MB (2625507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0e9363ab6b50c355c1e77c52a8f68a962c75c0c6688995b76926ba092d1c5d`  
		Last Modified: Tue, 08 Apr 2025 01:14:18 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:b587bbbbb7d4f51d0fd90b30536c82eeae2dd049a81a060bd8dad2c3796afb3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:9b24a1e4aed44d7791f733fc494df697e3153f30dc1da148150bdbea88a9785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125376241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444ac034fbac1d7c4221b7d9604fdffb9e5fc82995ad891e3677dec392090961`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87a5df34960a5366e891273aa5d596bd30678b8c383ba9841fca14be0ba6d1d`  
		Last Modified: Tue, 08 Apr 2025 01:11:43 GMT  
		Size: 97.1 MB (97147920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ae77bb4a4a708ca03f38b05a88fa906b13e8d77fff5677c1fa059e8f351344`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:1230715d812301a4f2ab3b0be04c97607f655a70350d47107421f6bdb66b1d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f74d5344b6368e711babfb8636abce4c9547fa85d2b66225882f8c0d3920d49`

```dockerfile
```

-	Layers:
	-	`sha256:5f3339a44a68747232c184cf536549435805c8cb326493fac2928fcc2f3b0ff5`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 2.6 MB (2625251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277b688fd5916a8a95d4c658c1d06a3b17c8126c05a585cce5fe7994b0707440`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c44503c13c46cf7f066c7927695e1dd362cbe99da5b87ee6023cfc0e00a1dced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121763175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6191f9b69418d2a33cbc97c29a598d3a54b10441b57fc7a679ed43a1f1e6fd1f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36550bbea26618210509c53259c59b26864ae5d7e1106cd7ee91bb31cfa3620f`  
		Last Modified: Tue, 08 Apr 2025 01:14:21 GMT  
		Size: 93.7 MB (93695791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a2b1573419950a7bf6f68c6715f908636e466c5804fa65a16696928d683079`  
		Last Modified: Tue, 08 Apr 2025 01:14:18 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:47b61ac75f5fb4fa983382a317e10c568045ad94389232c05a14e5011bab8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378586d6f846a9974f909f89483f93033fbbee6a2bb3dd2ab4cac4283c312c72`

```dockerfile
```

-	Layers:
	-	`sha256:b5c9abeeaf13f739e971b890c2013f850067040a56c196ad019b340f4916353c`  
		Last Modified: Tue, 08 Apr 2025 01:14:18 GMT  
		Size: 2.6 MB (2625507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0e9363ab6b50c355c1e77c52a8f68a962c75c0c6688995b76926ba092d1c5d`  
		Last Modified: Tue, 08 Apr 2025 01:14:18 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:84d10a0b8f24af741eefbf04d4d14177fd8b1c7cb3b8522ca23be67d3c239873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:578367e3b134ccee09f144991fefea34adee25ee97cd0b781a41c2ee6060e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105503846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0485699654555defd6d0ec269e3fe50075da3c9aa4780b36812653eeb8843eaa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb219db5e43313ed9ec9589a7b54567cba14103a3b8219c5e521cb88c1b9ec5`  
		Last Modified: Tue, 08 Apr 2025 01:11:43 GMT  
		Size: 77.3 MB (77275522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57db8344b12cbba58696f6e2510f27c7554fb3e0a0531768914c286870519076`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:8bff4edc918aa2df52f4d02e7cf187b1f6131a924688b787f599511a9e9e98d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af578e13d0fd692752dcce8c8b3cd0e481edc29aa262156cda5ed46a860c910`

```dockerfile
```

-	Layers:
	-	`sha256:b134a4028e6b55edbc72e076200a426d25324ba6356f8ee05b0bd147fe5e14f6`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 2.6 MB (2615858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6421d9a5cdbb04aadd15c6d5bf47e48030dab39f42c9ac0e7520c44715a95305`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8a32981b49ffb46c283fbb57234e3d3470e4bb8bbc262bcf9f034d762e4b7827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102617191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb15a5705f3d6ef0c9b6135303fbcd84279c101cc45479f4388cd96affb992e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709f6200b07d9e377ff2fa7ca8e65301f3a42dd8428c4e12692d15198dc9de79`  
		Last Modified: Tue, 08 Apr 2025 01:14:56 GMT  
		Size: 74.5 MB (74549808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d116251da89092fb32e21e23b522a4d70f06d93629aacb33631e02b9f6f29d`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:1a9a71b8d9ed61a0671d19b0a76817f8756bd6015d135af7343c54e19f5eef0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a67ff0de8488af70c0646e31652f49099c78a122b83a6dbd3df718f47a81695`

```dockerfile
```

-	Layers:
	-	`sha256:55599efb4a3747324f8fd962c1ef6997b8ecd285f4d52038144a805e5ec01aca`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 2.6 MB (2616138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9dae3c4edcc505a293f2641932615dc69315833967bca1dd8a7d6e99ce7e0d`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.6`

```console
$ docker pull emqx@sha256:84d10a0b8f24af741eefbf04d4d14177fd8b1c7cb3b8522ca23be67d3c239873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.6` - linux; amd64

```console
$ docker pull emqx@sha256:578367e3b134ccee09f144991fefea34adee25ee97cd0b781a41c2ee6060e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105503846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0485699654555defd6d0ec269e3fe50075da3c9aa4780b36812653eeb8843eaa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb219db5e43313ed9ec9589a7b54567cba14103a3b8219c5e521cb88c1b9ec5`  
		Last Modified: Tue, 08 Apr 2025 01:11:43 GMT  
		Size: 77.3 MB (77275522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57db8344b12cbba58696f6e2510f27c7554fb3e0a0531768914c286870519076`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.6` - unknown; unknown

```console
$ docker pull emqx@sha256:8bff4edc918aa2df52f4d02e7cf187b1f6131a924688b787f599511a9e9e98d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af578e13d0fd692752dcce8c8b3cd0e481edc29aa262156cda5ed46a860c910`

```dockerfile
```

-	Layers:
	-	`sha256:b134a4028e6b55edbc72e076200a426d25324ba6356f8ee05b0bd147fe5e14f6`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 2.6 MB (2615858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6421d9a5cdbb04aadd15c6d5bf47e48030dab39f42c9ac0e7520c44715a95305`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8a32981b49ffb46c283fbb57234e3d3470e4bb8bbc262bcf9f034d762e4b7827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102617191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb15a5705f3d6ef0c9b6135303fbcd84279c101cc45479f4388cd96affb992e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709f6200b07d9e377ff2fa7ca8e65301f3a42dd8428c4e12692d15198dc9de79`  
		Last Modified: Tue, 08 Apr 2025 01:14:56 GMT  
		Size: 74.5 MB (74549808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d116251da89092fb32e21e23b522a4d70f06d93629aacb33631e02b9f6f29d`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.6` - unknown; unknown

```console
$ docker pull emqx@sha256:1a9a71b8d9ed61a0671d19b0a76817f8756bd6015d135af7343c54e19f5eef0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a67ff0de8488af70c0646e31652f49099c78a122b83a6dbd3df718f47a81695`

```dockerfile
```

-	Layers:
	-	`sha256:55599efb4a3747324f8fd962c1ef6997b8ecd285f4d52038144a805e5ec01aca`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 2.6 MB (2616138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9dae3c4edcc505a293f2641932615dc69315833967bca1dd8a7d6e99ce7e0d`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:84d10a0b8f24af741eefbf04d4d14177fd8b1c7cb3b8522ca23be67d3c239873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:578367e3b134ccee09f144991fefea34adee25ee97cd0b781a41c2ee6060e0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105503846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0485699654555defd6d0ec269e3fe50075da3c9aa4780b36812653eeb8843eaa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb219db5e43313ed9ec9589a7b54567cba14103a3b8219c5e521cb88c1b9ec5`  
		Last Modified: Tue, 08 Apr 2025 01:11:43 GMT  
		Size: 77.3 MB (77275522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57db8344b12cbba58696f6e2510f27c7554fb3e0a0531768914c286870519076`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:8bff4edc918aa2df52f4d02e7cf187b1f6131a924688b787f599511a9e9e98d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af578e13d0fd692752dcce8c8b3cd0e481edc29aa262156cda5ed46a860c910`

```dockerfile
```

-	Layers:
	-	`sha256:b134a4028e6b55edbc72e076200a426d25324ba6356f8ee05b0bd147fe5e14f6`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 2.6 MB (2615858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6421d9a5cdbb04aadd15c6d5bf47e48030dab39f42c9ac0e7520c44715a95305`  
		Last Modified: Tue, 08 Apr 2025 01:11:42 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8a32981b49ffb46c283fbb57234e3d3470e4bb8bbc262bcf9f034d762e4b7827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.6 MB (102617191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb15a5705f3d6ef0c9b6135303fbcd84279c101cc45479f4388cd96affb992e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 25 Mar 2025 16:14:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709f6200b07d9e377ff2fa7ca8e65301f3a42dd8428c4e12692d15198dc9de79`  
		Last Modified: Tue, 08 Apr 2025 01:14:56 GMT  
		Size: 74.5 MB (74549808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d116251da89092fb32e21e23b522a4d70f06d93629aacb33631e02b9f6f29d`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:1a9a71b8d9ed61a0671d19b0a76817f8756bd6015d135af7343c54e19f5eef0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a67ff0de8488af70c0646e31652f49099c78a122b83a6dbd3df718f47a81695`

```dockerfile
```

-	Layers:
	-	`sha256:55599efb4a3747324f8fd962c1ef6997b8ecd285f4d52038144a805e5ec01aca`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 2.6 MB (2616138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9dae3c4edcc505a293f2641932615dc69315833967bca1dd8a7d6e99ce7e0d`  
		Last Modified: Tue, 08 Apr 2025 01:14:54 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
