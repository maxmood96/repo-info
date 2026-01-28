## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:63f1255613ecdf82633c7526f994b0bb665850c791aad4245ee0c233c229507f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:17b5e07075a8d599a40b4955bd06809146e3c990f5c89a533a273cfb06e67fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247222229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af2ec851007cbca3a9fee2a0a7c9f150df1b478d1cc888679761e8eef54d5bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:05:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:45 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:45 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388919fe65bb1c88c6f6fa2757c0816952103420acc7775905483d7d38edc06b`  
		Last Modified: Wed, 28 Jan 2026 18:06:20 GMT  
		Size: 157.8 MB (157826065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae52425091be770e7b291dcd8519414f2a64f347014cc60d7262a683bf7d8052`  
		Last Modified: Wed, 28 Jan 2026 18:06:18 GMT  
		Size: 59.1 MB (59136623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cc2b578e246b1971f023b84f52b14a7f9ef3119dd19bf792f90ea339c9ce27`  
		Last Modified: Wed, 28 Jan 2026 18:06:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951492dca0ce6f4b082c77e619c36dbf0e56b2b867a3f3f8c6e493670465d701`  
		Last Modified: Wed, 28 Jan 2026 18:06:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:971913b7e8654e903941fbcb96a2e1a16564a3e63595646329e82d4c721a15d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029933fdc0146984fc4b1411ae64ba0519512291d3e5c657738e9eba268acefa`

```dockerfile
```

-	Layers:
	-	`sha256:4d06df093d13061f15d2ae8d6aaa40665462192a71776ed5fca906ef2a6c1818`  
		Last Modified: Wed, 28 Jan 2026 18:06:16 GMT  
		Size: 5.3 MB (5311970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038b84ffe6ec3edf2f2f3b1c815a2793c0dab37bc64f32da7d7e9bfff12c39b0`  
		Last Modified: Wed, 28 Jan 2026 18:06:15 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:232faf7425b2c35f976cd2edbd6283362e39316e18c4ef07939b1ceed1332b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244145196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4e26e88032d25cfc24b36bd2d728f426df72caaeecedbaf244edef3e81b5fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:05:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:24 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:05:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:05:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:05:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:05:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:05:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ec37cc57c55a7f3b1fb4f9fb4bee5642ceb221e04b6c12cfbe3856d6173815`  
		Last Modified: Wed, 28 Jan 2026 18:06:01 GMT  
		Size: 156.1 MB (156107578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5659ab696375e8c031d9195fa2c79d86cc31fd4edd5ed473e4e866a2a9a35145`  
		Last Modified: Wed, 28 Jan 2026 18:05:59 GMT  
		Size: 59.3 MB (59288059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ed0b5dd9bc8b83de5992b7d038da6073714fa045c6970e4c3e7e205b260218`  
		Last Modified: Wed, 28 Jan 2026 18:05:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70baf76986c0e432fd1fec11ae782c4ec20b8ac7d388a09d9870c0496ea376b8`  
		Last Modified: Wed, 28 Jan 2026 18:05:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd1837862fdf3f678d819f78de495d7ac9d31e5841225e14523415f81033f1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5333656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a14ba8987ac680a241027872bd86be55420fee16daa578a01de9f59e180a0f`

```dockerfile
```

-	Layers:
	-	`sha256:83f9555e705b28d1b6962c915c4f5e17d1915dada0ffa4aa4d51eb944637e114`  
		Last Modified: Wed, 28 Jan 2026 18:05:57 GMT  
		Size: 5.3 MB (5317702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de8c167a9f71a6c8076664e26d8bc293c2dfae0a5612a8df9c30be2fe3e27da`  
		Last Modified: Wed, 28 Jan 2026 18:05:57 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
