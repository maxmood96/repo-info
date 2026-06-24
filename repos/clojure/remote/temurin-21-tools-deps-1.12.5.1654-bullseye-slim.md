## `clojure:temurin-21-tools-deps-1.12.5.1654-bullseye-slim`

```console
$ docker pull clojure@sha256:992f44544c7658681e356eb26816c298e4879c795c04102489938657ecdc478a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.5.1654-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f9081600af318a7118cd59ae1b65894b6ceaf670694cb0a8b0887abd4fb42e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244527775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accf994a0c5a63d03f8e87425a94c739c22eecee299d04d00f2c270e8af2edd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:19:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:19:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:19:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:19:57 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:19:57 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:20:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:20:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a57cebb8a87d3a6801dac7afb55de96328222c73d963b4e64b15eff62d73afd`  
		Last Modified: Wed, 24 Jun 2026 02:20:32 GMT  
		Size: 158.2 MB (158166941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358fb268be20d565b769072aebd080232fa178e4019ff64878ad7089e46b8a`  
		Last Modified: Wed, 24 Jun 2026 02:20:30 GMT  
		Size: 56.1 MB (56100345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9aba6c140bf2763f9075966ea19649162901af123d34e6be6c460114d784b5`  
		Last Modified: Wed, 24 Jun 2026 02:20:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7e32750c3865230404690e0b7ebc7755e0b388d2f458c03cd9fee3078378f9`  
		Last Modified: Wed, 24 Jun 2026 02:20:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40d34d3ab5d55db72c6bde5d13e2b0e53a05c2d1fd95057f89a37edd83a98108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d8a5453eadc7ecf69c1e0b0310f814e36628f02a209b19b937044210041e76`

```dockerfile
```

-	Layers:
	-	`sha256:fd143152ebc24482770c7ff0c74b730b2366c04ca7038835c6a4cc75204ef5e8`  
		Last Modified: Wed, 24 Jun 2026 02:20:28 GMT  
		Size: 5.3 MB (5319701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a216d6c1410daa0a69c59d39436cf6554618369111102fbfe7d1aefba16370df`  
		Last Modified: Wed, 24 Jun 2026 02:20:28 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d9a10e11416f1e2ec973db8d3a950c846e9a0d7ca9730a927463e8db17e86e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241476028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f857bfacf6169ca15f3994239f9d533d6a11dfbb1015f31dcad2e55f935d4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:26:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:26:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:26:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:26:19 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:26:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:26:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:26:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:26:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86371c72599e6acab4e07821a5e67fef2b85ae2e185a011bb5b15222edb8e19`  
		Last Modified: Wed, 24 Jun 2026 02:26:56 GMT  
		Size: 156.5 MB (156461246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fc8341488264b86aae4ddaefd78d718efd27e429875910dfd71260f0d82ab2`  
		Last Modified: Wed, 24 Jun 2026 02:26:54 GMT  
		Size: 56.3 MB (56266816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a2ac8fb2876579e7a9055bf9402cb2c37fff1547bd21f71563ddae1bab9e9`  
		Last Modified: Wed, 24 Jun 2026 02:26:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b30cec959d7b380dad546f2f465401d86762437226ab2b5d3f3dfb7d47d3289`  
		Last Modified: Wed, 24 Jun 2026 02:26:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:540b8defee8b7fc15ef5deb6e9833e0ad22f70bf196aa0f25a8be49149ba4383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f8c1208a58a1f4f1262f9376a78a755903116fd35d5658c5ae825b46923e5f`

```dockerfile
```

-	Layers:
	-	`sha256:0f44b70fb79834f5ea2606e927dc3df1b46598205b6cf01b619a8f32d5042d8b`  
		Last Modified: Wed, 24 Jun 2026 02:26:52 GMT  
		Size: 5.3 MB (5325433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a829d5f80ca2e1353b08fccfb14c591e129d61f32d4ad666da5faee60def439`  
		Last Modified: Wed, 24 Jun 2026 02:26:52 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
