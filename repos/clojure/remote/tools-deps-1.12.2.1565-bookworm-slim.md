## `clojure:tools-deps-1.12.2.1565-bookworm-slim`

```console
$ docker pull clojure@sha256:223e90afe8f01c01b8de4a34d6a10027dd26f6f7586b78d136e689d3a2aa0e16
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
$ docker pull clojure@sha256:173f9ebc91cf94eb9f61f8b33a8ad441ed331cc894bdcf1e97b6ceba04f0a072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253713707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ff8ba9840cdeef586153ea580c5031db79da4817ff9f188257c58f20510f75`
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
	-	`sha256:c7cb6f08fc12b236ede5adade93b3f9ffe36915f17b9fb3fdb6b34343457dc11`  
		Last Modified: Tue, 02 Sep 2025 08:09:57 GMT  
		Size: 156.1 MB (156081264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec41caece9878e40417268935eba0514bdf8dad8b3fc6a742d512c9ae5a7c69c`  
		Last Modified: Tue, 02 Sep 2025 08:16:40 GMT  
		Size: 69.5 MB (69549398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410ba774294d29112c87208b695529b2e7fc0ae49c48192505fcf04c909a2215`  
		Last Modified: Tue, 02 Sep 2025 08:16:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d3fffdfa8a8fb825c906690f317b6190e338ea9d03e864ed24d93a3edbd9c3`  
		Last Modified: Tue, 02 Sep 2025 08:16:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:730b74363f6d374e1d3a9b99f8cb17ca89d8582b1720a093f5d0f5424008065c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8e7cac53879ceaec7ea57386175394e87fad667944d62a5965f0cab436d569`

```dockerfile
```

-	Layers:
	-	`sha256:d25aff314569b19f0b848391c5583dd58ad5c38de6fb83332b93d43e3f40fdac`  
		Last Modified: Tue, 02 Sep 2025 09:40:36 GMT  
		Size: 5.1 MB (5120856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818b43ae18747abdd9f47878c755dde98b086d6219249b03896a8c531c8e1287`  
		Last Modified: Tue, 02 Sep 2025 09:40:37 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:93c6689d9973ae3946f4bf96e7145cdaf936a988ffd3b8e18bd7375aac189a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265541929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0915e7d375bd9f5c1192126a1465815be2405e9ac5aa3dbb23172e0fd8851dfd`
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
	-	`sha256:19ffd328672fd40878f149855d02f5c91f57260d057b8ee8febb0d0879fefa3b`  
		Last Modified: Tue, 02 Sep 2025 08:52:31 GMT  
		Size: 158.0 MB (157963469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd60fcaf424ed5149916c0da05432fdf9416f6a5e26ec835ce5e42c21f5d742`  
		Last Modified: Tue, 02 Sep 2025 09:04:11 GMT  
		Size: 75.5 MB (75503995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c29a81ea10f3bbbb0bbb623c188e62fcf76e2131307afeabd5d1b51d17186e`  
		Last Modified: Tue, 02 Sep 2025 09:04:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f260de2b2cfc0d67af70b6a3e2f1471939e44efcb65932c2ea6f92452fa6a`  
		Last Modified: Tue, 02 Sep 2025 09:04:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a56ee55f817d7c077a3804ec7cef70460d8b8a98d1b1b17e6e94b007fff895f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393678ec8d956bc8348135eae3d2b21749119be9dac988471d965928278f4338`

```dockerfile
```

-	Layers:
	-	`sha256:5af1752f5ba4734d4a9988a8e2513fe149901ea5a9caa09bb8041da9369c6c13`  
		Last Modified: Tue, 02 Sep 2025 09:40:42 GMT  
		Size: 5.1 MB (5120241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583427c53ed8f2f20b0494a6219ca0a03d912c9bdfeb562484ed3343ee675663`  
		Last Modified: Tue, 02 Sep 2025 09:40:43 GMT  
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
