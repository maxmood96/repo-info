## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:7f2ea85f3dc906b37d08417f1d16e5c2702427e6cf4b2f7e88567d0951a6bf70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9ae9fa8dba39f5bfc8a218a5c3bfad5e540d56e64c6675a7528e5d217ad83cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269293836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7c883ec75b6e95a1a8fbdcd022f10de54a0e68ed1f9cd79e7e9c54c4ace8e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:35:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:06 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:06 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e4b07698f1229bf43c5188d8329829ee0524d7f1b1578a2c1a23bd97462f0`  
		Last Modified: Thu, 14 May 2026 23:35:41 GMT  
		Size: 145.9 MB (145905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851391d12631d554326b1bcf01d3c6c584f004ad42ab3603cde12c2952ffe432`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 69.6 MB (69623969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb6e4e70381f4925beddb0fbd067098c33c2a635a6a205f5adc2f19a5a76261`  
		Last Modified: Thu, 14 May 2026 23:35:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ace9096cd784724701c0e7078407da60d28a5d70b87f305492ded433aeff24`  
		Last Modified: Thu, 14 May 2026 23:35:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:31af49099fcd65dcfd82ff5ec6a5801391ba64671e2d47980f9583510dbfe416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af32e9c006c564d72f1e468aebeba074ab19909c3d5c1b00d40767332882e14a`

```dockerfile
```

-	Layers:
	-	`sha256:b279ba03ddb2774f8a287d055716dea807243eb2a887cf3d3b2fd948ffe9373c`  
		Last Modified: Thu, 14 May 2026 23:35:36 GMT  
		Size: 7.4 MB (7408278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a80eff0819863b1c00d3b80ec12695d4f26874f0a6833b446160a7a391fd30b`  
		Last Modified: Thu, 14 May 2026 23:35:35 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:35641d1419dc3f7ca79c066077583fdf357598d4fc3cdae5d4cbd75422d5a217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266742787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18960507cbdc44caaf85abbd9c530a05eb44e09072b27f054c3d000deb38fc3f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:35:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:06 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:06 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b350062e65ad40008d3d61b2a5d5b7e893c1d6492bc205afffa9f83d1bec394`  
		Last Modified: Thu, 14 May 2026 23:35:44 GMT  
		Size: 144.7 MB (144724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2caf5bcad72aa76788a444229696042c15ccc96399695af0121e71c09b1788b`  
		Last Modified: Thu, 14 May 2026 23:35:42 GMT  
		Size: 69.8 MB (69764196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3da2e559d16bfb46a0893047971d859cc8baf8fb802cc7b85828b62bd312375`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850bad6ec9b4ab7e665d654ec0b3f3a715dbef2723b479f9442afb7fdf7ebf9`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:224f6dc3b99c27957ca405f9bc1b77a93dcb755758bfb2f52aaa73c0f966a349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c9bf129f1c8ecef807c4707d0621db5c71a29f6d6ee75c9a9ea2a991d3116d`

```dockerfile
```

-	Layers:
	-	`sha256:675d2460f089f2fa71dcffc2bfa65d194f463d14fe69c4ce5be9203a83676ea5`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 7.4 MB (7413377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ba122b1bd3ac2e015a480329e2bc721d8433d9e7ca6a7f249f58f954a8352bd`  
		Last Modified: Thu, 14 May 2026 23:35:38 GMT  
		Size: 16.0 KB (16049 bytes)  
		MIME: application/vnd.in-toto+json
