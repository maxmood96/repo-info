## `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye`

```console
$ docker pull clojure@sha256:11e0f50974170bb9bb90de8267b93d85ca1e89fca7bf6077d87542883e513ef6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c548e0a1ecbe97d3e359136d2c27fd41c4c905d9a77c99540c85e1c4beb7bbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266192202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5e4913b7336b9833bb4422890a63b7868ec715d5adfed36d51d8ebe0edee97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:17:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:58 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:17:58 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:18:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:18:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72b69b48c3e2b02e513d49b920e9daa422e808f0da9ae230fc68da682f28646`  
		Last Modified: Wed, 24 Jun 2026 02:18:35 GMT  
		Size: 145.9 MB (145905407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af6b6ecdb1d1c29390238960afeb8a03f8126f57f8bbebd413fe84f6817bfd1`  
		Last Modified: Wed, 24 Jun 2026 02:18:33 GMT  
		Size: 66.5 MB (66512746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe69d6c277c1b0bbc9833eb4c714bda74fbe11eb8457ab18cb0025b9c6eb729`  
		Last Modified: Wed, 24 Jun 2026 02:18:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0008c42700dfdda2eed2797a59b773ab01af21225fa6a4356f72701f2e5d3bfb`  
		Last Modified: Wed, 24 Jun 2026 02:18:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e54fce813cfa190c6608e9a18f36102d3b5b7a5f9d56e1edd791c87d0e42610e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b702056150729c11bfa30f96aec6b2b86aba78e3b4a851b47b2356616d57bb81`

```dockerfile
```

-	Layers:
	-	`sha256:5614b68be12d328c21f70342a530c5bec68a5620e691a414c1fe073d97c74cef`  
		Last Modified: Wed, 24 Jun 2026 02:18:30 GMT  
		Size: 7.4 MB (7405449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b18f036e5ee1de0d192a3a153765b3bb5f92e7ec1dc6364a642793b000e6d9d`  
		Last Modified: Wed, 24 Jun 2026 02:18:30 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fda8386116d0fdd69fa545318cfa2ed1400d857cf47e0dda87039f81f6bceebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263660600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823c5f82eb457a1da5bd3cd8ba0309d280e86d514c3ab090ef6fe5ff75f55556`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:24:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:24:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:24:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:24:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:24:41 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:24:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:24:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:24:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:24:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:24:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470eb6af4d8962b160ca70d74332f99e19b8dcd7a10ffdd8321b0a6e98d7a9cc`  
		Last Modified: Wed, 24 Jun 2026 02:25:19 GMT  
		Size: 144.7 MB (144724352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efed9961acbaddc40ba3dfd40472ab357e1877017000fc1b29c151fb2140ceed`  
		Last Modified: Wed, 24 Jun 2026 02:25:17 GMT  
		Size: 66.7 MB (66677989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27985b0fc6f33b6db22607c30dfd2b8efda972052ccc0d1b7ffe5e939bf56e6`  
		Last Modified: Wed, 24 Jun 2026 02:25:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a624ed98a305dc9f46bfec23a80e2c0626c6d51823d54b3ec6a6af1f7af00`  
		Last Modified: Wed, 24 Jun 2026 02:25:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b30ea6cc0c7c7d5d9065e060c79305b846a4da970b32ede304a0833409d34b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16487d652930edaf38ba9cb940e1e92db3572b9e21369cad454b9ef37a12fcd7`

```dockerfile
```

-	Layers:
	-	`sha256:bd0dc7731ff8a991c2e8e977e6d882a92285f268a46c73caea94928aa02da14e`  
		Last Modified: Wed, 24 Jun 2026 02:25:15 GMT  
		Size: 7.4 MB (7410548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c5fcddeca505e82f15469a654537812f014107913b19ea2bf465a999b1e1a62`  
		Last Modified: Wed, 24 Jun 2026 02:25:14 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
