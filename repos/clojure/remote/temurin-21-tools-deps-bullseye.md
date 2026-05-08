## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c35f2ee8a4f84477717fa0f109dfd02d94f9711738e538ffb4763ad04c7d6696
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:80b6da630c4a9527f3670bc3cd72cf585459a5377eb4f7aceb923969a0205af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281218716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65eab06ceca7e0b141a351fe1100247d6472813bfdda365d060bfb0202230330`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:19:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:50 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34c323c49eea6e520615009d1273e4f75fd7212ee7480747195963b25f43736`  
		Last Modified: Wed, 22 Apr 2026 02:20:26 GMT  
		Size: 157.9 MB (157857105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09e952ae7071ea027825de4260e67c0ed3ce3a8941380840371dfae92abc097`  
		Last Modified: Wed, 22 Apr 2026 02:20:25 GMT  
		Size: 69.6 MB (69597417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f044e816b7cd5b9083840de9c3d7aaf93008f45c3f61e56513a81af95bbe110`  
		Last Modified: Wed, 22 Apr 2026 02:20:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a5a55a081694f4faf89eaca429e6fc1df3af075e09242d4aba177efca6ce38`  
		Last Modified: Wed, 22 Apr 2026 02:20:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:38aca49a0b84443d030b0ea1ccfbf0e396a4954dce7d7e09750fd56a7d24c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e02d793ee167e0cd7c710ec4157c29712443e715281628a97632588356b17e`

```dockerfile
```

-	Layers:
	-	`sha256:2d6396b9266069493acceb391fd92c9d445f4ee5d56ad5719b35fb8118eebab4`  
		Last Modified: Wed, 22 Apr 2026 02:20:22 GMT  
		Size: 7.4 MB (7409505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1f37d24c8b199fc0225612f2ad6abb3f2289f5732b00f1f9316bff1188f78ae`  
		Last Modified: Wed, 22 Apr 2026 02:20:21 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9c92a07e9e85791557897f2cc6c9a49840b64901e5ae9f34796002d99e506b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278453890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b141c6d511179e5278bf69b4f85a2cc814c546e89f8db780b65cac7df3ea789`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:25:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:25:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:25:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:25:50 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:26:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:26:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ed538be3440bd13866dfa4333600e40b79f026113b288e7e2ee989ae31389`  
		Last Modified: Fri, 08 May 2026 00:26:28 GMT  
		Size: 156.5 MB (156461247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40a5df77941d34190d60ca68f57ed2989a7266f11e204b665152de4715c8714`  
		Last Modified: Fri, 08 May 2026 00:27:05 GMT  
		Size: 69.7 MB (69738600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa4053dfb5c31f907c484e64244e8fec08df4f8d3947015338597a40ff8007d`  
		Last Modified: Fri, 08 May 2026 00:27:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5032a3ea274bf5a2b6f5fd3b1e15021f3d0b30194bb386859b561e571c500b4`  
		Last Modified: Fri, 08 May 2026 00:27:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7e22841a42c0173eab073aa67437de19e8ac918b0d4b64525340e29afa2a7f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1ec04aa5839e642d39b1f10151e32d9ff9cb2292462f5bf2a67e0369f5f86c`

```dockerfile
```

-	Layers:
	-	`sha256:8f41b3bb877f18b9ef057d151dd880c36948a73f5d81a5555233438e30599860`  
		Last Modified: Fri, 08 May 2026 00:27:04 GMT  
		Size: 7.4 MB (7415231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fbe44f77766f32978cdc0d32dec50033e926f0a8cb955daa0d56b3637f6b23`  
		Last Modified: Fri, 08 May 2026 00:27:03 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
