## `clojure:temurin-24-bullseye`

```console
$ docker pull clojure@sha256:3bcc6ae4f1e53f24155e5ced2734aa9538866e2fb0d9110b4062dc6afd0ae97b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2d2903caea740bc6f6e79f809d28502b3fad04b2b2508cd9401b4d0c5a8850f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213288249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59886576edae0ce0e5f0e24ea4065682257deaa225c73ed226cd2762dd544f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
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
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72718a2495ab224a0e5846873b78748ea1a2be8df66751b0f9105f6e13862e4`  
		Last Modified: Tue, 02 Sep 2025 01:58:01 GMT  
		Size: 90.0 MB (89975141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadc81676acf0683cc66c265fe913bb0c8d1f6839d94dfef5320beb43a72196e`  
		Last Modified: Tue, 02 Sep 2025 01:57:56 GMT  
		Size: 69.6 MB (69556724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a024dc09d245ca2087e74d20a941e116964210c73ddb1872658d088b6211db2`  
		Last Modified: Tue, 02 Sep 2025 01:02:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a5b949b94cee3f3462bd5c6adc83d96a8a75ce4e608a4b22f320d6de874a2`  
		Last Modified: Tue, 02 Sep 2025 01:02:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:735e437f66dddd8e8ca6ed134bc8f9fab8df0e852d596da75f233e2843f55bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba71fcb354f6fb22e50dd25cb586211691288264274c4fd87ebaa4f8717f821`

```dockerfile
```

-	Layers:
	-	`sha256:0dd2674338e6c12aa16311f1655b3df06e21b983e0572cafc15096884e8f5263`  
		Last Modified: Tue, 02 Sep 2025 03:43:12 GMT  
		Size: 7.3 MB (7346315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8139055f62bfc27dfdcbdfca6444db276cf3c375cb1beb35f73c4946319f76f6`  
		Last Modified: Tue, 02 Sep 2025 03:43:13 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83a08bcf1c5fd9564d2bac650fab6f0293ad7941ad7d30680a76926aad6ce6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211025835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8078474321a1a0a2e6ed0aba869dfab953cb79624f401837386f4f50e919fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
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
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60d85f112d5a9f600a471ed0d0ae6ac7f386dc0d9adace00ab46943420b1b4`  
		Last Modified: Tue, 02 Sep 2025 08:24:03 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec011300026fedf1060c1bcf7a65bf10f716f7ae2ab720ce8d9dfd1b9e5532fc`  
		Last Modified: Tue, 02 Sep 2025 08:28:56 GMT  
		Size: 69.7 MB (69683880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a69adc3d02b9531ebe4ce06a80ebc78848e509fed55f7dc4dd8b79c77a59b`  
		Last Modified: Tue, 02 Sep 2025 09:19:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7021c510df81c0d38489576058118308fa015ce21e6f0acbd4be0c99bc4744`  
		Last Modified: Tue, 02 Sep 2025 09:19:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:39678b358d062f3139d17e934e2c7c15f3e0112c6cf265552e98b49556e1f814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de45e97f421535c467b960e29832d30e62ab0e61a25593ee1cbf3b8c7d3bb9d3`

```dockerfile
```

-	Layers:
	-	`sha256:4926eee80bf3b741d22a4ec098ea8f3831d8b8203981023f1819cc2539dac6fb`  
		Last Modified: Tue, 02 Sep 2025 09:42:37 GMT  
		Size: 7.4 MB (7351411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:911cc441995366bcb64e2246850c33680a0832d48033218e19c260d1c51b465c`  
		Last Modified: Tue, 02 Sep 2025 09:42:38 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json
