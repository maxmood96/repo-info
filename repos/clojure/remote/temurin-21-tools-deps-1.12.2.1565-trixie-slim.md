## `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:745a3e73c7b9c73e64bf91a20a754a5e1ba013fd4a4f401a3df9e0be99a17c9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b0f8bf5e42c2a265b8af0120a72e8d06acd1840b69481f17625ffbfa968f3275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259561988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f06c3c4146e787c7771e847316920bf2e644435ca15a7cbb0d40238dcdbba4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6064f4f5254f6a00caf4b34e2df8daf0a6a5bff71afab72002ae2d53e3e625b9`  
		Last Modified: Tue, 26 Aug 2025 19:07:21 GMT  
		Size: 157.8 MB (157804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1cb4f5133c3354e4e3454f3ac40e7dd4b96c56c8dadae4472da978eaf2f5ec`  
		Last Modified: Tue, 26 Aug 2025 17:28:29 GMT  
		Size: 72.0 MB (71982888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7cded1d74692f085fd6cff91fb4c5b73a709b4abf7da8ae8b3ef90456e101d`  
		Last Modified: Tue, 26 Aug 2025 17:28:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0b5a698da972e02dd76687246af201df6c7850f296d9e1126252043fbfcc1d`  
		Last Modified: Tue, 26 Aug 2025 17:28:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd4c708f8b960c1ee41cd2ea10057ad24b759b3ace4e494bb77a0fd99537d7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae229c11176820f6aa85bfd94f3eb539216a8530021439862f76aeff28f83ae6`

```dockerfile
```

-	Layers:
	-	`sha256:b191486db5463c714432bdc4c303305bc39946059880f3f5e2108af2bf6b442a`  
		Last Modified: Tue, 26 Aug 2025 18:41:13 GMT  
		Size: 5.3 MB (5259027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53ca477c98c6a1e6dcf56e2f56f560c31026c484a5a48b8b2d828bb6d8067c36`  
		Last Modified: Tue, 26 Aug 2025 18:41:15 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5f1313ef42649cd840de664e0bd7d102080393cf94ed0d575a36c8f3c3ecc1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258022084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c43617bf712fe9a3033c5d83057a3feb001dd6a593c2c16c14ba70f4c68f19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a56322ce1b94f29786d8f76971f53596ba74b5abd690c1219b73a7ffedee07`  
		Last Modified: Tue, 19 Aug 2025 01:33:36 GMT  
		Size: 156.1 MB (156081245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96714c8480f45f0a7caf3f9e4ca5b41099b96e7a6e1495cec71886a2af508f7c`  
		Last Modified: Tue, 26 Aug 2025 17:53:19 GMT  
		Size: 71.8 MB (71803752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11abcd13d4dae1aa6e6dd6e760c06ee1b24571966266ab0eaf68cb57a271fa0b`  
		Last Modified: Tue, 26 Aug 2025 17:53:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0d55206ace0c0a52c3f7f272db1bf330e9c26fd96e5fec1578e79d04ae92b8`  
		Last Modified: Tue, 26 Aug 2025 17:53:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6543a7875c2a07fdfe947b8de151a36c70b84d78e30b03081655bce0d3ad49b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00d5d073ba18bf9bfa39c172505151d530a0bd393a98ce78da1a680b5859e19`

```dockerfile
```

-	Layers:
	-	`sha256:a61de1383119def08b0016b6f6bcf931f223b0c65a72f38e6481e25b631539e5`  
		Last Modified: Tue, 26 Aug 2025 18:41:19 GMT  
		Size: 5.3 MB (5264820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bafd101508611c7b0590d66866a8937e87a88e3bc75b9441a2091fcba46f1d6`  
		Last Modified: Tue, 26 Aug 2025 18:41:20 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json
