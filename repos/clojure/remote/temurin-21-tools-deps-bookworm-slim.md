## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:418805077277aa55848030c84a8023ed6f95b9d50fade0bc5d2829bc0c3c47d3
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:664016ace08896f1dc14860a74dd58d1fd861667cb33ef0d1c37391908d97f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255704189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e8c23c8c020c6a788aa368db5f08ecaff55b8b7119e48deb6965fa1d06cd58`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4697fcc43aea84bdd08c0bcc20bc06b0d58b7b532f9709b712f79c06f671ec2`  
		Last Modified: Tue, 09 Sep 2025 05:00:54 GMT  
		Size: 157.8 MB (157804821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6d414712eb88191f293ce65f64225e9107e0e4bc51eed75faee1e866740df8`  
		Last Modified: Tue, 09 Sep 2025 05:00:25 GMT  
		Size: 69.7 MB (69669984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc06154aa223c483db8cd7274d5b9650b11c7c12d0e9eadc3a5333ce6fbb92e`  
		Last Modified: Mon, 08 Sep 2025 22:12:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7530f371f7f4a5dffb69b6bd78369b6ee08cac6cee01de79488feb94445a2db9`  
		Last Modified: Mon, 08 Sep 2025 22:12:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2937708c3260814e2d3e975c8aadd0d9a0ffc97b4ca006253c8550857aca7204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be783e7141f0a4869cf2c20ea9b398fbdde2659d422599f7abf2454ff7bf57d`

```dockerfile
```

-	Layers:
	-	`sha256:d36921c5801f7c8e0846f8649f10339ab56b7165a492715675c05ae185291582`  
		Last Modified: Tue, 09 Sep 2025 00:39:48 GMT  
		Size: 5.1 MB (5117186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aaaacce53d027d86d213d86616878b3b8875fe99f7c776e2af38bb7b5cdfcb1`  
		Last Modified: Tue, 09 Sep 2025 00:39:49 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5aca6d179f1a0ba124adbc034a7db958dd4cd29fbc6e1b470dbb46c95b6e9d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253743281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c52a2cf63db92e7100a36e3bafb94b20abf70c62c9a6a6a3f3a39883b0c08d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec05fa0c28eac7c363957f9a78ebd6d62d7b0dd10ae5e9e8ad5c56845d86bce`  
		Last Modified: Tue, 09 Sep 2025 00:41:36 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec848b71dc587a7386347db9ab9681cbb05e27067f0099891472142f8a66023`  
		Last Modified: Tue, 09 Sep 2025 00:41:34 GMT  
		Size: 69.6 MB (69558957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dea242815006ffcad5886ad92cef5cc852ddc19346fb53fe2332e201f5f9c4`  
		Last Modified: Tue, 09 Sep 2025 01:21:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49648be2aa652d6995e443c2a7eec7f47bd159d3f9ae5cf60e12bb4e91b466b9`  
		Last Modified: Tue, 09 Sep 2025 01:21:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04933b918a08ed7ae80c647b5cb1a8b3524f0c733cd8a16f359369ec4319631f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d64de4cd394844c233fe7e112282797837e74c14ed6f12a06b0e52b75638bd7`

```dockerfile
```

-	Layers:
	-	`sha256:147ff0f88ec72132082d34c1d21ebe039e2b96eb6a2749f13f325c93997ac2ea`  
		Last Modified: Tue, 09 Sep 2025 03:39:32 GMT  
		Size: 5.1 MB (5122971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a6ca97d0674c917c4a969af4e2330033acb2f3c53fc71cb47745c0669a31e50`  
		Last Modified: Tue, 09 Sep 2025 03:39:33 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

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

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

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
