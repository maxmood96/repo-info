## `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:a719921edf95de4f867542e0dcecc5ae508931ac696c7f3e0716b455c3dbc56e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:383e878a6f3d916d0ac2ef3a76c1a04f34b7d55fe6a9d2484afbf1df29c948c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259645648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad2e2e3ecb6e29cceff5b8929bd73ba14a930a84b755f2431af5d3d3e400ac7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:16:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:16:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:16:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:16:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:16:22 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:16:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:16:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:16:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:16:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:16:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9e50013f4b0512cf7a2bccefa28d6f43fdc06ebe29bab1470083915cbbfaef`  
		Last Modified: Tue, 07 Apr 2026 03:17:03 GMT  
		Size: 157.9 MB (157857047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2585cf4307b900f5eacbafc3de35b863e7618e5ae5fd23ef3caeaf1ac11c22`  
		Last Modified: Tue, 07 Apr 2026 03:17:01 GMT  
		Size: 72.0 MB (72011919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4f2e6feaa19010565f1ee04c4a89d525a5fb2c5da6d37b2c0258f4042467e9`  
		Last Modified: Tue, 07 Apr 2026 03:16:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2cc3c2ae7ad172783247a5d865185a51ee0d0d0fe4059c9417302b558f60be`  
		Last Modified: Tue, 07 Apr 2026 03:16:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:263ed4a3be155e9f3e687dbc6520f0edfb398ef999711682bafcd09ab1b7adf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad04f4832022fd87310e1c99be31bf90d695783b4966d841540054d552cfcb7`

```dockerfile
```

-	Layers:
	-	`sha256:001253aa324ddcb35751140b261878fb055cd16006da8db5b91c966045af5649`  
		Last Modified: Tue, 07 Apr 2026 03:16:59 GMT  
		Size: 5.3 MB (5260990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7e28f28e6b94281b31bf033f79797f32ed2a70f0b1e7ddd661214c0875c0026`  
		Last Modified: Tue, 07 Apr 2026 03:16:58 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5ac03d6c7c10bc648cc15705b0acea97adb963fd04dc4aa1b7b13c5028ca205b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258104369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f503d46fdaaa0155e41e6b66b184635a46a24fb7ff26ba19d4c6b59300bcb7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:26:33 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:27:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c1c3a34ef57280cf5c0e533c81d90c0e60f26075860ec24985d325b0935a93`  
		Last Modified: Tue, 07 Apr 2026 03:27:14 GMT  
		Size: 156.1 MB (156133064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edce20d072a55d0da79d1af7d9151a4e4ebdc464a4540215919526619f9d6307`  
		Last Modified: Tue, 07 Apr 2026 03:28:05 GMT  
		Size: 71.8 MB (71831713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836a84aa1a28b3e7f099e18382a3d190c72107f5098a479ac3ed611b1121ba53`  
		Last Modified: Tue, 07 Apr 2026 03:28:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5216e9d3d6c71f610b831a2f8f63e01adbdf560405924c119a92ed3ccbd8cea6`  
		Last Modified: Tue, 07 Apr 2026 03:28:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:943db2f75c3b85d655e5be53e9b17e44654c76eaa40fbbbce3d6b1e0c8fbe8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7735fb1a1e95dd825ae46a9afdb845ce8356c38abf603e6095421c878ba3c3fc`

```dockerfile
```

-	Layers:
	-	`sha256:da0add43b028712a2032551c57473f3205d7acc36fca81890852b927d37673e9`  
		Last Modified: Tue, 07 Apr 2026 03:28:04 GMT  
		Size: 5.3 MB (5266759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48d4ba7ff55f2b6782cfc037ce5bf28662ca67e0d51f1172c011e5916eeaa2da`  
		Last Modified: Tue, 07 Apr 2026 03:28:03 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:793e7368612b44f8db8dd42cd3fe6a1c120bab3259c86579f51be70fb18a5230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269000902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22ddd49ff8594ca04896a235bcac404d1ef6c0cfc19453f0079ceca2e37a668`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:37:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:37:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:37:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:37:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:37:33 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:43:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:43:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:43:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:43:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:43:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3ec6fdaa48a78814b25d06b8958fec2609466001981f561b8114f6360e796`  
		Last Modified: Tue, 17 Mar 2026 18:39:04 GMT  
		Size: 158.0 MB (157977471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d91eb187d8917ace2dc97d414b07a5d6c7202303e23958d567f71b2bbcbcee`  
		Last Modified: Tue, 17 Mar 2026 18:44:06 GMT  
		Size: 77.4 MB (77429555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fb8b0246ac2030f984b095328c08da0c3407fc7789e5ed3e4e77884c282d87`  
		Last Modified: Tue, 17 Mar 2026 18:44:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3515028beaaafa57b08caab68e3222ab62f377d358557810c1a1d27b92f0b59`  
		Last Modified: Tue, 17 Mar 2026 18:44:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:890cdd56beb3f7bc2a1b8867a63cde085b909bc27f00c144bcc716e18d36e561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91ee67588db7298d47cfba18ff5778a16329aab4ca383963e865b03ad857c66`

```dockerfile
```

-	Layers:
	-	`sha256:4f93896a4e3f5de116f867276756f9c4894db80c40ceb6f6a1895474890340af`  
		Last Modified: Tue, 17 Mar 2026 18:44:04 GMT  
		Size: 5.3 MB (5265361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc70129aaa174882bccc33a61ef0a5823b3ac1d8b6f69d070810dda346e684ae`  
		Last Modified: Tue, 17 Mar 2026 18:44:04 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:3241f90b07f1e3aa49c2a45db2e29458c1533deeb08bc152c76ccb07fa0bc260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256394110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40f477cdf13538206759c8606ce5d3ed963712f79ebe57a0f9f83e338131aeb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 18:55:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 18:55:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 18:55:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 18:55:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 18:55:45 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:19:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 22 Mar 2026 19:19:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 19:19:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:19:29 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:19:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ee54184b00a8250bd83765fa0f3fb43da949588b64be8499761fc35178cc57`  
		Last Modified: Sun, 22 Mar 2026 19:01:53 GMT  
		Size: 157.2 MB (157216875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0c277426f33dc41fd1063ee8d3c491a07a0d7f74195afed69556c7031a9f3`  
		Last Modified: Sun, 22 Mar 2026 19:23:16 GMT  
		Size: 70.9 MB (70900558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ce403ca8325a553ec044e921106dd5d8cf309c1cfae23716754a1ea0e9ff62`  
		Last Modified: Sun, 22 Mar 2026 19:23:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afa626657b02b03ad67ab9c68e487afa0d3e226cb66453a12957d55b68962de`  
		Last Modified: Sun, 22 Mar 2026 19:23:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1afdc82a339b0b42f48e48f181dd93eaab80c6ee1deeda326bb55cad329f8bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a243b923713b2e95a6f29446851d63338f7321dd71a06a5f94a964b451ddb64`

```dockerfile
```

-	Layers:
	-	`sha256:f7589bc3e469a59f145fc293cab0ef1c141433c11aabb3f7c44fdf13c780bf3d`  
		Last Modified: Sun, 22 Mar 2026 19:23:06 GMT  
		Size: 5.3 MB (5250454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e18b86e6721685a1071adc6478cfa80b8ba751ad0eb95d1ac29f4849811619a9`  
		Last Modified: Sun, 22 Mar 2026 19:23:05 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:10aebca408a5add621327f424ead0918cce9c45ef180115973197549da07064e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249928731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a9779daee88a35a6b66086f9a3fb4be80a573b9cb90f18f9153d5a70dc81cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:46:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:46:26 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:46:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:46:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:46:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:46:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:46:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc4ccf718b91e6d661df12976987fde0beff316e149a5b77a4424557d38ee9`  
		Last Modified: Tue, 07 Apr 2026 05:47:13 GMT  
		Size: 147.1 MB (147105211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d582f7becf81eda9951c35ed284b91860a9627e639a0d54d079165824ad6e9`  
		Last Modified: Tue, 07 Apr 2026 05:47:12 GMT  
		Size: 73.0 MB (72987061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7b4a14c675c6afa039233a00779cf69b5f9a4fcc863dd392a9f690c9849202`  
		Last Modified: Tue, 07 Apr 2026 05:47:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca9c429f539c03b5bda01ddc7ab7707fa44fce5af09a4cf45e738b81ce84ce4`  
		Last Modified: Tue, 07 Apr 2026 05:47:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f428b13108c44a212c2aedf63a31a856d7030d4ba75458afcf44f3cbdff5441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c59ad1df71fbf40e4472ce65785d7571e2a7316bc9111a11a73d84ee8e0888`

```dockerfile
```

-	Layers:
	-	`sha256:648f6325b11d9021374597249a6b23b77f66feb3a493af7ce817c85555398663`  
		Last Modified: Tue, 07 Apr 2026 05:47:10 GMT  
		Size: 5.3 MB (5256914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f0fd9b70f4972232a6fcccf9c5e2c023bb2084df3a0155956aca32549d1919`  
		Last Modified: Tue, 07 Apr 2026 05:47:10 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
