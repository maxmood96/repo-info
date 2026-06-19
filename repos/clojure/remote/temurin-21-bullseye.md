## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:290a891e6f4d715ee3e15a31336ced73b06b48a086e48b8561acf6aae0232027
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6e4b00147663b3ccbe9044f0dff25a243964532a156a15594c3ad0bab1d7a6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278452486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce11e4b7395f518b64b213231cb75eb1a44f14beeec3538c52fca74a697bc79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:18:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:18:49 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a22fa2fcd99d1ac959f45fc21a8217c772f4558f2639dd1b7027b0254c4616`  
		Last Modified: Fri, 19 Jun 2026 02:19:23 GMT  
		Size: 158.2 MB (158166925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070ababfb73620f02eae570199f3102cc448206cd0ae12f6e6f282624c9e8df2`  
		Last Modified: Fri, 19 Jun 2026 02:19:21 GMT  
		Size: 66.5 MB (66512754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c64e5288e92b42d0e09e5cb2b37017328dc1af8cc9a88d84d17827fa319a90d`  
		Last Modified: Fri, 19 Jun 2026 02:19:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a64a39554a1e679987cccc519630664ed143cc516c15480effd1fe69df322c`  
		Last Modified: Fri, 19 Jun 2026 02:19:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:adfa5d80610fbc70ae82296bb344abe5a9d28ad5100f9988f8dd6d74c7159ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc3c9e5bdfb1671d0169e061762485eea3d073eb87fb909db1a4d3ca87ca44e`

```dockerfile
```

-	Layers:
	-	`sha256:89c844605fc037e5c3d81ebed753f525c97f5d4d46c1593a375f15e08d71d5cb`  
		Last Modified: Fri, 19 Jun 2026 02:19:18 GMT  
		Size: 7.4 MB (7408925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9a7a063a918d7718480623b902ce738e22962040fd2a4521d3e3e032eadd0e`  
		Last Modified: Fri, 19 Jun 2026 02:19:18 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1f21f48b2799e2f8f07742e9ece63a68df3a2316d32c0e1920b0b5de3f10edc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275403895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035dd5fd7fb64b9e4f3431a8f62f21152950beecfe80536d07b4383fb7022037`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:19:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:12 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:19:12 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebd1586a1969a9ff83828981da6ef955a6b565efe6ba9271a940548218f72ed`  
		Last Modified: Fri, 19 Jun 2026 02:19:51 GMT  
		Size: 156.5 MB (156461268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbdf6591fa47cd864a2204e9c800aede020474544dac0eba8edbe03791af4bf`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 66.7 MB (66677470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e6ab84da200bf961e9f93a794ca24c34a7f87aa4239fcdf5f0c63b8244d18`  
		Last Modified: Fri, 19 Jun 2026 02:19:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67400fe9c1037a4a14b132b90e9601efb789d2756694f83cc25c3a3ea440cf0`  
		Last Modified: Fri, 19 Jun 2026 02:19:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c66882df6a9396922e01ebf243892b7e98ce17574c2621ac51ca9295e444be44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a534d70663be2bce53643fe2d12514e21af622897dca3e6d899fe92679f4830d`

```dockerfile
```

-	Layers:
	-	`sha256:1008cafce1e7351f6a734703810597aeb0dc05c81c2f3e232c15495d24271d85`  
		Last Modified: Fri, 19 Jun 2026 02:19:46 GMT  
		Size: 7.4 MB (7414024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fdc372eff95d9df71227ffff0464940f1ed8a51bdf8d16514e3168d19cc157`  
		Last Modified: Fri, 19 Jun 2026 02:19:46 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
