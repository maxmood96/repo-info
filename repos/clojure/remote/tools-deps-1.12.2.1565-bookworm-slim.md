## `clojure:tools-deps-1.12.2.1565-bookworm-slim`

```console
$ docker pull clojure@sha256:3312a654af32c17db52878009bd5a3a1e92a1b3ed6fb1f3017ce6e334ac45deb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:31ebe9499a8cfa59176dd5e970f89f1d31dfe99f50dec21ab65c2046fb3a9760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255712421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7528d5e6135a410a5c78a67930cc118c8254889b9adbc3ab32b5ab4bec7b5117`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7ea8756661d0db5d98b7e82f895cc95328a91770f7c258805f62f76e27eba8`  
		Last Modified: Tue, 02 Sep 2025 00:17:52 GMT  
		Size: 157.8 MB (157804819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef65154e5f85e81d5e5aa60eea3601ccdc972d4d4842ea165c645d75f781aa17`  
		Last Modified: Tue, 02 Sep 2025 01:54:13 GMT  
		Size: 69.7 MB (69676302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0335dc83014f16711266191704143cbd95fd0f80d09b807579172ae464e9cdcb`  
		Last Modified: Tue, 02 Sep 2025 01:51:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdd16fa2054092d0ab53650dd8194b1d2a36f0cd0a52f3d68e8330262394675`  
		Last Modified: Tue, 02 Sep 2025 01:51:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:68cf65b8082566f1fef5b06e37265bacd1c0b273a5cb77c2f317f65987c97963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79fec7bc314f2c83db0315cbc8ec5248ef268acb102966dfbdc0bc97958e3e6`

```dockerfile
```

-	Layers:
	-	`sha256:dbaebb71f1cc121c497053af27f39b6b1a03642bf5c3cd5b8b2ea7cdf5bf2267`  
		Last Modified: Tue, 02 Sep 2025 03:40:56 GMT  
		Size: 5.1 MB (5115071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc8d28bb0c6b927cbdf83bd0a5ef8bbad49d588f75b94032b4b31a597a2026d`  
		Last Modified: Tue, 02 Sep 2025 03:40:57 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1ddff4da9f14136b35e43f633f4ce67c0cfd1cf7738bec21a0e6c5fa737131b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253713757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b3dd1001816565ce3b1bd8359e765dbf2c868dc6a367920985ca2ac64d1dae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7991a92c7ee87da171852566b076064998d9091210c9e1f68f8874a4a0f1ef`  
		Last Modified: Mon, 18 Aug 2025 20:51:19 GMT  
		Size: 156.1 MB (156081253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c4c2836ef9b52981af34c11d65eccc77018a2c40dad9c8bc696ee34faf28da`  
		Last Modified: Tue, 26 Aug 2025 17:48:34 GMT  
		Size: 69.5 MB (69549460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf06219a6f05ae84a8a8a7f7840eeed8cceb5ada0bc6e16dd01ad1016d386aa`  
		Last Modified: Tue, 26 Aug 2025 17:48:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1509569a08fd6fa13b26d5bb128d1de6ea7a482ed7b966773136816cd2b1ee1d`  
		Last Modified: Tue, 26 Aug 2025 17:48:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:541430df0486c295ce1e8e8a2f135a067095af52f0235e7707a7b1cb5478a244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2c6b277f3f98866e145f82a268e1e7682c793964114c055766b23deddd6872`

```dockerfile
```

-	Layers:
	-	`sha256:74307c93ed0102f47d33dfcc74bfd1adc55499acb3001de23fd041f3e6017662`  
		Last Modified: Tue, 26 Aug 2025 18:40:01 GMT  
		Size: 5.1 MB (5120856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410ee0024ab2796f34b3b38687b5a7ce55e6374fa17d061273d6f71e1e873f2f`  
		Last Modified: Tue, 26 Aug 2025 18:40:02 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f369a5dbba6d8d25fd3e4ac64a2221bdbdb4f8003ef2db21c0860e6e6d84053f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265541888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6284d3ffc589c6d54cf5cf55431df0176b2df531de7d7de2d2d395dded9596`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f159f526f8a9c3649fee57d0df8248d04aeb1f957c2fcd7d35d584b2f74bdf`  
		Last Modified: Tue, 19 Aug 2025 18:06:25 GMT  
		Size: 158.0 MB (157963439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9005274ced95b932f6d7ffa914f0435f4e253e50a12f893dfb55be7f62c82aa`  
		Last Modified: Tue, 26 Aug 2025 18:07:02 GMT  
		Size: 75.5 MB (75503983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2e979f93d3d9b4a6052782b32e12f8c66d2486afcdb393f03ac98cdc64d38f`  
		Last Modified: Tue, 26 Aug 2025 18:06:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2e293b9967a2b5cbe323ab28c2299f33c6894ed0a32c2f930d4bc77b43373a`  
		Last Modified: Tue, 26 Aug 2025 18:06:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a56ffbca69b0c10b8d5a2d10f7b402c0a77af7d71f602dc593ad35fcc82f47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad7379e0220e72daddbdee06f83a46e0dce6474378c23c28f7aae7b6023a26a`

```dockerfile
```

-	Layers:
	-	`sha256:9e4fc38b6b2c3a9258c556a6c3710f956563d25f116a54ba2bb757e8425d1c2a`  
		Last Modified: Tue, 26 Aug 2025 21:36:47 GMT  
		Size: 5.1 MB (5120241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4779337b51fbe97b98e13274c77ee1942aa9c4f0be62f12653b31485cca50d34`  
		Last Modified: Tue, 26 Aug 2025 21:36:48 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:cf8f05eb1a815ebe4563169b9698b70fe0975233eb3b384b7ec37a04989fe9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242400188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014be84f8f7b69f285f6aa08d51ca083e4ae3f04784edacb4ea07580bcbc0c4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2dbf27160a1e80e0b20c8615d5458b6251a8507eb46a0bd9f24c7493aacd91`  
		Last Modified: Tue, 02 Sep 2025 02:09:55 GMT  
		Size: 147.0 MB (147026942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1153243e0dbdc3db0d530b81b61548e0ff6df05fe17d427174516fcb81500270`  
		Last Modified: Tue, 02 Sep 2025 02:16:07 GMT  
		Size: 68.5 MB (68484365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44457773250f61ab92a6c87e6c06859a9821a0c66e944de73e6cbd308fb07f4a`  
		Last Modified: Tue, 02 Sep 2025 02:16:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2062c63065cc4b971f70de6d5e039f6929981ce2d7f29a73bf7056d56f0ab7`  
		Last Modified: Tue, 02 Sep 2025 02:16:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90617ae32b4dff397af8199cec0256f00720c3d66e977f181bfbf8cc16195b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cf3bd4ec438d5e12c6fa8ee0edd28f48e07c7f0bf43d46ec15138155834209`

```dockerfile
```

-	Layers:
	-	`sha256:8bfedd8e7288a802edff371732312e3046a452378deb7d9f240df5dfbaa3ec42`  
		Last Modified: Tue, 02 Sep 2025 03:41:13 GMT  
		Size: 5.1 MB (5106392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3849db76d73915c2c9cbabda09f908abb7eb706971d3aa722fdf7c3b7b3860c5`  
		Last Modified: Tue, 02 Sep 2025 03:41:14 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json
