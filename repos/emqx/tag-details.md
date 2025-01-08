<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.4`](#emqx584)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:612712becf3cc151e37232cdc8250889f18a3311091934706fda863944f6a454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:7b5314043efb114086daffac0a2b60782bed4c592849b83d9dbf9db0fb2c4884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105175729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3465475d11b3098d649755d821a3f1049c91528c7e19ffaa51f73f82bfc93`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd2d1c5b251014e0a52ca7a69dbefed8d933867370b13a3f6d203bc51278b4b`  
		Last Modified: Tue, 07 Jan 2025 18:31:01 GMT  
		Size: 76.9 MB (76943086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81b99930f3545c597062bab5642e9f2807ecbba64b127f512f21e140ae5be87`  
		Last Modified: Tue, 07 Jan 2025 18:31:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:2fa0228527b50ccdc3e2384e38c44e2096e6e4873a26f38d824082142d242a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3cdeaeefff951f93b4998db111178a56a07ccef3d7c36fb87a52382ff8b3b5`

```dockerfile
```

-	Layers:
	-	`sha256:3e528e63b70a8cdfdb883dd5f084fe35d1686d27181c9eeeef6fb2792986d16b`  
		Last Modified: Wed, 08 Jan 2025 04:31:20 GMT  
		Size: 2.6 MB (2614482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f54cc4b9a7377f8d2ff12f63517a95a950da469f7ca3ddd7a406acee6886a6`  
		Last Modified: Tue, 07 Jan 2025 18:31:00 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bd0034c650f1565900a38a15b9ef3cb5b1eacdf934c08683d9a92bdf3789b4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102274531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5799cbcd42b83cf17452964964e8b5d590bd936847b6e26acf3b96263f2144f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fac58b55455ead0081238236fd8730a3c887ce10fd59af3295cb36951a6cac6`  
		Size: 74.2 MB (74214743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98880b9fe16cfe30e1d04ef4b9db08d0ac29a650071284a281caf265714ef627`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:dc2d24b720ea8ac9b17ec3def392176e2a3ff2d7f1e3ffaea7f242c9823f53dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d43d8bf8a2498067df4f45d8a07aa829304ef84b76785e647d771a89cfac63b`

```dockerfile
```

-	Layers:
	-	`sha256:fb626610a7e76fa308371e14436961b173bac518d6c04c699646e444c9159ab9`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 2.6 MB (2614762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c6debf75a6e8b3bd558616d98f8ae38c6e4f8e430e76f2159c2d9e341e1974`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:5dd6d2840bc201e305370f7d22f714b9c14e0c4fa4cdb1febeb980de74c18736
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:401f96244b6757f961fcb04b31fd2f62323568ae3d18ca208cb743d743582ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125187548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3ae969ede07aca8b8a7341b5ab2110eda3d65111168f8c105e6b6f0e1b8c55`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515f97f0ee1b22d4e2bdb4800ac02827a1350e99bf8074c4521f05e18db17d57`  
		Last Modified: Tue, 24 Dec 2024 22:14:04 GMT  
		Size: 97.0 MB (96954906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818bb7a04444d50238dca1f7bf207d39dee7505a7aa52f1b8cca07886f368f56`  
		Last Modified: Tue, 24 Dec 2024 22:14:03 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:a72033764eccf9728af689beccab221222415ae8671f6ff30996371834fe934f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27962659af058ee647f843f1b2ec7ea85e5449fad971e7736253fe5cfa69d421`

```dockerfile
```

-	Layers:
	-	`sha256:b9368bf50f734755d6d9bc231103056994efc46e41bb4e31ef13b0a9b85c9172`  
		Last Modified: Tue, 24 Dec 2024 22:14:03 GMT  
		Size: 2.6 MB (2623881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1a716c37c9724b2b7db6645ec825f3bb26f801a5005f1e9e5526ad3f356b44`  
		Last Modified: Wed, 08 Jan 2025 04:31:23 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:93335799d014b14d3cdce1b52c486553e8db424737c9c52cc6438d6abfa8e902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121561437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ec54846e498254a906bee479bf3447095ab0c83e52a679cfcece8e029c7a4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df6b9f78bf616a9b9da10972c6ebe598a7f5ea5f6a38db7da34f820762d3136`  
		Last Modified: Tue, 24 Dec 2024 22:20:56 GMT  
		Size: 93.5 MB (93501651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9b08a6b52e1584d21b18bed83f0a3affd2b587803ca59e33e0faf1219f0d22`  
		Last Modified: Tue, 24 Dec 2024 22:20:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:c582e7b8710ca3d96261491a67eee81b23dbae0374f075182f20c35323fcdc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56518e6eca72895ad0261586e4722067e7d8a1c030b9f77e2f750d7c55ee2cef`

```dockerfile
```

-	Layers:
	-	`sha256:da5d2e9d1c67461752b9263c8fda683270a68f0b979ecd20543cf40006e1017b`  
		Last Modified: Tue, 24 Dec 2024 22:20:54 GMT  
		Size: 2.6 MB (2624137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1179376bbc4030fc578b292e98b1ede52c0749525e4377e99137b2b91697e6f5`  
		Last Modified: Tue, 24 Dec 2024 22:20:53 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:5dd6d2840bc201e305370f7d22f714b9c14e0c4fa4cdb1febeb980de74c18736
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:401f96244b6757f961fcb04b31fd2f62323568ae3d18ca208cb743d743582ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125187548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3ae969ede07aca8b8a7341b5ab2110eda3d65111168f8c105e6b6f0e1b8c55`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515f97f0ee1b22d4e2bdb4800ac02827a1350e99bf8074c4521f05e18db17d57`  
		Last Modified: Tue, 24 Dec 2024 22:14:04 GMT  
		Size: 97.0 MB (96954906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818bb7a04444d50238dca1f7bf207d39dee7505a7aa52f1b8cca07886f368f56`  
		Last Modified: Tue, 24 Dec 2024 22:14:03 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:a72033764eccf9728af689beccab221222415ae8671f6ff30996371834fe934f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27962659af058ee647f843f1b2ec7ea85e5449fad971e7736253fe5cfa69d421`

```dockerfile
```

-	Layers:
	-	`sha256:b9368bf50f734755d6d9bc231103056994efc46e41bb4e31ef13b0a9b85c9172`  
		Last Modified: Tue, 24 Dec 2024 22:14:03 GMT  
		Size: 2.6 MB (2623881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1a716c37c9724b2b7db6645ec825f3bb26f801a5005f1e9e5526ad3f356b44`  
		Last Modified: Wed, 08 Jan 2025 04:31:23 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:93335799d014b14d3cdce1b52c486553e8db424737c9c52cc6438d6abfa8e902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121561437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528ec54846e498254a906bee479bf3447095ab0c83e52a679cfcece8e029c7a4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df6b9f78bf616a9b9da10972c6ebe598a7f5ea5f6a38db7da34f820762d3136`  
		Last Modified: Tue, 24 Dec 2024 22:20:56 GMT  
		Size: 93.5 MB (93501651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9b08a6b52e1584d21b18bed83f0a3affd2b587803ca59e33e0faf1219f0d22`  
		Last Modified: Tue, 24 Dec 2024 22:20:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:c582e7b8710ca3d96261491a67eee81b23dbae0374f075182f20c35323fcdc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56518e6eca72895ad0261586e4722067e7d8a1c030b9f77e2f750d7c55ee2cef`

```dockerfile
```

-	Layers:
	-	`sha256:da5d2e9d1c67461752b9263c8fda683270a68f0b979ecd20543cf40006e1017b`  
		Last Modified: Tue, 24 Dec 2024 22:20:54 GMT  
		Size: 2.6 MB (2624137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1179376bbc4030fc578b292e98b1ede52c0749525e4377e99137b2b91697e6f5`  
		Last Modified: Tue, 24 Dec 2024 22:20:53 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:612712becf3cc151e37232cdc8250889f18a3311091934706fda863944f6a454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:7b5314043efb114086daffac0a2b60782bed4c592849b83d9dbf9db0fb2c4884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105175729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3465475d11b3098d649755d821a3f1049c91528c7e19ffaa51f73f82bfc93`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd2d1c5b251014e0a52ca7a69dbefed8d933867370b13a3f6d203bc51278b4b`  
		Last Modified: Tue, 07 Jan 2025 18:31:01 GMT  
		Size: 76.9 MB (76943086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81b99930f3545c597062bab5642e9f2807ecbba64b127f512f21e140ae5be87`  
		Last Modified: Tue, 07 Jan 2025 18:31:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:2fa0228527b50ccdc3e2384e38c44e2096e6e4873a26f38d824082142d242a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3cdeaeefff951f93b4998db111178a56a07ccef3d7c36fb87a52382ff8b3b5`

```dockerfile
```

-	Layers:
	-	`sha256:3e528e63b70a8cdfdb883dd5f084fe35d1686d27181c9eeeef6fb2792986d16b`  
		Last Modified: Wed, 08 Jan 2025 04:31:20 GMT  
		Size: 2.6 MB (2614482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f54cc4b9a7377f8d2ff12f63517a95a950da469f7ca3ddd7a406acee6886a6`  
		Last Modified: Tue, 07 Jan 2025 18:31:00 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bd0034c650f1565900a38a15b9ef3cb5b1eacdf934c08683d9a92bdf3789b4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102274531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5799cbcd42b83cf17452964964e8b5d590bd936847b6e26acf3b96263f2144f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fac58b55455ead0081238236fd8730a3c887ce10fd59af3295cb36951a6cac6`  
		Size: 74.2 MB (74214743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98880b9fe16cfe30e1d04ef4b9db08d0ac29a650071284a281caf265714ef627`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:dc2d24b720ea8ac9b17ec3def392176e2a3ff2d7f1e3ffaea7f242c9823f53dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d43d8bf8a2498067df4f45d8a07aa829304ef84b76785e647d771a89cfac63b`

```dockerfile
```

-	Layers:
	-	`sha256:fb626610a7e76fa308371e14436961b173bac518d6c04c699646e444c9159ab9`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 2.6 MB (2614762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c6debf75a6e8b3bd558616d98f8ae38c6e4f8e430e76f2159c2d9e341e1974`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.4`

```console
$ docker pull emqx@sha256:612712becf3cc151e37232cdc8250889f18a3311091934706fda863944f6a454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.4` - linux; amd64

```console
$ docker pull emqx@sha256:7b5314043efb114086daffac0a2b60782bed4c592849b83d9dbf9db0fb2c4884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105175729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3465475d11b3098d649755d821a3f1049c91528c7e19ffaa51f73f82bfc93`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd2d1c5b251014e0a52ca7a69dbefed8d933867370b13a3f6d203bc51278b4b`  
		Last Modified: Tue, 07 Jan 2025 18:31:01 GMT  
		Size: 76.9 MB (76943086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81b99930f3545c597062bab5642e9f2807ecbba64b127f512f21e140ae5be87`  
		Last Modified: Tue, 07 Jan 2025 18:31:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.4` - unknown; unknown

```console
$ docker pull emqx@sha256:2fa0228527b50ccdc3e2384e38c44e2096e6e4873a26f38d824082142d242a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3cdeaeefff951f93b4998db111178a56a07ccef3d7c36fb87a52382ff8b3b5`

```dockerfile
```

-	Layers:
	-	`sha256:3e528e63b70a8cdfdb883dd5f084fe35d1686d27181c9eeeef6fb2792986d16b`  
		Last Modified: Wed, 08 Jan 2025 04:31:20 GMT  
		Size: 2.6 MB (2614482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f54cc4b9a7377f8d2ff12f63517a95a950da469f7ca3ddd7a406acee6886a6`  
		Last Modified: Tue, 07 Jan 2025 18:31:00 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bd0034c650f1565900a38a15b9ef3cb5b1eacdf934c08683d9a92bdf3789b4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102274531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5799cbcd42b83cf17452964964e8b5d590bd936847b6e26acf3b96263f2144f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fac58b55455ead0081238236fd8730a3c887ce10fd59af3295cb36951a6cac6`  
		Size: 74.2 MB (74214743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98880b9fe16cfe30e1d04ef4b9db08d0ac29a650071284a281caf265714ef627`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.4` - unknown; unknown

```console
$ docker pull emqx@sha256:dc2d24b720ea8ac9b17ec3def392176e2a3ff2d7f1e3ffaea7f242c9823f53dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d43d8bf8a2498067df4f45d8a07aa829304ef84b76785e647d771a89cfac63b`

```dockerfile
```

-	Layers:
	-	`sha256:fb626610a7e76fa308371e14436961b173bac518d6c04c699646e444c9159ab9`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 2.6 MB (2614762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c6debf75a6e8b3bd558616d98f8ae38c6e4f8e430e76f2159c2d9e341e1974`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:612712becf3cc151e37232cdc8250889f18a3311091934706fda863944f6a454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:7b5314043efb114086daffac0a2b60782bed4c592849b83d9dbf9db0fb2c4884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105175729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3465475d11b3098d649755d821a3f1049c91528c7e19ffaa51f73f82bfc93`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd2d1c5b251014e0a52ca7a69dbefed8d933867370b13a3f6d203bc51278b4b`  
		Last Modified: Tue, 07 Jan 2025 18:31:01 GMT  
		Size: 76.9 MB (76943086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81b99930f3545c597062bab5642e9f2807ecbba64b127f512f21e140ae5be87`  
		Last Modified: Tue, 07 Jan 2025 18:31:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:2fa0228527b50ccdc3e2384e38c44e2096e6e4873a26f38d824082142d242a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3cdeaeefff951f93b4998db111178a56a07ccef3d7c36fb87a52382ff8b3b5`

```dockerfile
```

-	Layers:
	-	`sha256:3e528e63b70a8cdfdb883dd5f084fe35d1686d27181c9eeeef6fb2792986d16b`  
		Last Modified: Wed, 08 Jan 2025 04:31:20 GMT  
		Size: 2.6 MB (2614482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f54cc4b9a7377f8d2ff12f63517a95a950da469f7ca3ddd7a406acee6886a6`  
		Last Modified: Tue, 07 Jan 2025 18:31:00 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bd0034c650f1565900a38a15b9ef3cb5b1eacdf934c08683d9a92bdf3789b4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102274531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5799cbcd42b83cf17452964964e8b5d590bd936847b6e26acf3b96263f2144f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fac58b55455ead0081238236fd8730a3c887ce10fd59af3295cb36951a6cac6`  
		Size: 74.2 MB (74214743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98880b9fe16cfe30e1d04ef4b9db08d0ac29a650071284a281caf265714ef627`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:dc2d24b720ea8ac9b17ec3def392176e2a3ff2d7f1e3ffaea7f242c9823f53dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d43d8bf8a2498067df4f45d8a07aa829304ef84b76785e647d771a89cfac63b`

```dockerfile
```

-	Layers:
	-	`sha256:fb626610a7e76fa308371e14436961b173bac518d6c04c699646e444c9159ab9`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 2.6 MB (2614762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c6debf75a6e8b3bd558616d98f8ae38c6e4f8e430e76f2159c2d9e341e1974`  
		Last Modified: Tue, 07 Jan 2025 18:38:18 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
