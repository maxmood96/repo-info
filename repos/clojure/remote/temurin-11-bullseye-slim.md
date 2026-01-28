## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:30b3825b078342211da7be461982d9ac48af64753daf96adff8f002a8951a8bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:544bdbd533e68a01017658ee55b394c375b31db54e3e5671cbf8e171724f5d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234362546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502896d1977d321828b4c8d0d54d8e41396818a8148cece068dad8074d3e7a86`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:04:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:07 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58578195f51c5df2a28acb762fb062a3e171341ab1f465ed40309d04062e11`  
		Last Modified: Wed, 28 Jan 2026 18:04:48 GMT  
		Size: 145.0 MB (144966605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb4b13004d789c0e84a28ea08c0034e2514142ed5249e47b4ca19fb23311dc8`  
		Last Modified: Wed, 28 Jan 2026 18:04:46 GMT  
		Size: 59.1 MB (59136800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77031cd3890a5e470544224def29fe0308b753c0a66019c08a2528c195e9d50`  
		Last Modified: Wed, 28 Jan 2026 18:04:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:827d1fba9fe0307f67dc99dabf9d72d8355d5f8bb4abf7d4e1ba44a08cd0b62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad31f96026613f656c4d31d3f32897ea67fe93eafaec6544256ff12cdecd82c`

```dockerfile
```

-	Layers:
	-	`sha256:585de435b21e7884a751a00237ffbb530ebd257cbff34db26c6e401a11b12950`  
		Last Modified: Wed, 28 Jan 2026 18:04:44 GMT  
		Size: 5.3 MB (5329007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b7c54adc18f18a9b5394d14a6d7adc26804874d67b06c58e4c6bbcb8e78bb7`  
		Last Modified: Wed, 28 Jan 2026 18:04:43 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e5b3dd408838556af8e7c80e3e796758c1a83ac71deba29d07bc0453a0b7526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229767302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe2bfe26de59d739405e068cdf07631dd85462796ac046eb66fecb6a6577893`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:03:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:14 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:14 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b008161c062441dfffa84e2849df23efcaa7b816f12d590ef152f2fd16fe74`  
		Last Modified: Wed, 28 Jan 2026 18:03:50 GMT  
		Size: 141.7 MB (141729962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a331b31f28bdcf5e86d933ca80b34f186d04c34c1e43bd95165a3cf16a01896`  
		Last Modified: Wed, 28 Jan 2026 18:03:48 GMT  
		Size: 59.3 MB (59288178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590acb0aa977ffa14bc0f9b5628f52430200e8c91134345def2ba1886a834897`  
		Last Modified: Wed, 28 Jan 2026 18:03:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2034935eaa7fb8502ec55dd349379e840929505f4db8deb18cccfa5df9c93c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf885675973f90e55f72c115f7e4943878b29447ee1e82ad0cee14a70621c75`

```dockerfile
```

-	Layers:
	-	`sha256:6696fc6224f8b2383aeddd09c85becacfaa74eb8171608a9c9ab74b549ac8f97`  
		Last Modified: Wed, 28 Jan 2026 18:03:46 GMT  
		Size: 5.3 MB (5335357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8882ad4f0498625627ff07db5bd384c9d59c8038be23bde16d8ac69e18cf4fa`  
		Last Modified: Wed, 28 Jan 2026 18:03:45 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
