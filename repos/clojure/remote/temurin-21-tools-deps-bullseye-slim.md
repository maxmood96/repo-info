## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:4c8440a49f79f7c531dccce9a6a64842387815694a971f91e0bc087e460d077d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0d2f75d30fb914dc8f06c6c0f2c875ad36ea3b7b67d8f1afe09f80a4aba91777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247253006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a1139035b6e8491588c9101270acc0419224307c4e940de9676ed1984a294`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:44:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:40 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:40 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:44:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:44:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7e2e45856109bf404c7e7fee1b9ad29c01af63c34ac8fe47b7a985d51e9968`  
		Last Modified: Tue, 17 Feb 2026 21:45:18 GMT  
		Size: 157.9 MB (157857101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa6757abc323fbb39dd7cae64968635fcce7060a4fb20ab5fafa8630a94d10b`  
		Last Modified: Tue, 17 Feb 2026 21:45:16 GMT  
		Size: 59.1 MB (59136578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e075caba10e3c71eaf23f6836adca2c19ba2b433af27b0b94842b8d6a12cfa2`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fd5b6dbe6abbc53e9eb031d8b2b5591d094d834177828a742ec574942e582a`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:265be8ce3bdc4bc840dc9860ee88a402dd1bf3e6364f539aac3fd825119f0928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42819707a125670fcbea2d346f89ced89b787782e1be3c4c31a6a139b4de2916`

```dockerfile
```

-	Layers:
	-	`sha256:95a4d8e0856dd0397831403247fb7011f99bc88f78323b64e918be38f7905d7f`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 5.3 MB (5311972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e03204b44e0d99afed2c2db29913a95316ab46a3eb4cb604294471ca0efc2e`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc8d91fce6b0e53c8435bb4121440fd9295b713063416f17be35e828d16699a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244166470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5eeffb84fa641e7ff9a944941d161a54f7096bfd2ae4134a6e1606ff1db5458`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:44:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:40 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:40 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:44:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:44:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62956f2eaa59627f43e370a2b4157f821fc3a8a8fa824e2cd0463e3ecebc598`  
		Last Modified: Tue, 17 Feb 2026 21:45:19 GMT  
		Size: 156.1 MB (156133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc0c5ae7b95810562dbf94978004cdfcd0f63209e4e76f2c10a37f7298b86c`  
		Last Modified: Tue, 17 Feb 2026 21:45:17 GMT  
		Size: 59.3 MB (59287910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776b475a7645f288720192e13bf65c8e07724d1d6b81b07146ff3d95b9156310`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ae274a6cb03af16ae18b1a1e49aa831a6bd070253552a4196a0cce9a968a21`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:57645822183935338eee67eb748f287e671fbb00c23b8bbaa0dd3b50d31065e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5333657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1e8f868981c228018de30b53b3602244d9e1e143b32c2bd251506e8382ae7`

```dockerfile
```

-	Layers:
	-	`sha256:05fde28117e2a37aaaa3e6c4c53b40a2d1fe44a22418c90759d1af3acec77e13`  
		Last Modified: Tue, 17 Feb 2026 21:45:15 GMT  
		Size: 5.3 MB (5317704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628bfee753463d79c206bfeca7bcd7410ae1bf95e5b03ee760216f821cea8f0e`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json
