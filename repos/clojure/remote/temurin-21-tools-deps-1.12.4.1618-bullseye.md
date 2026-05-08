## `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:b27a016e77c6e78b32c58f49d7690c1ec9fe86f4c5d5fb2eda6042f078970cf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:bf57c0bc5afa5a960ced82cca69fd3f2cb3e48caa29456725d5c9d0910ed8bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281528810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31609f0d69afede75c28c3c3c83cf7735de9060e771f62e0050a498ca9cd10f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:11 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b9fb0ffc4057c0885c93b84405de9b1e2ab598e9974797d71c2208acd2643`  
		Last Modified: Fri, 08 May 2026 00:28:17 GMT  
		Size: 158.2 MB (158167002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f565596829bba9f6ab413dcbbca05f3659cc1642e72fb8e25368f9dc8d222f67`  
		Last Modified: Fri, 08 May 2026 00:27:56 GMT  
		Size: 69.6 MB (69597618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbfe56a1dd49f935ede9fed3459fc5e27d0ccefe4a4c6a82e0d2b538b59087`  
		Last Modified: Fri, 08 May 2026 00:27:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161d8b46757ede6fd22daedc5b08db396299dc0b489d0e63d0880d24bc8ced95`  
		Last Modified: Fri, 08 May 2026 00:27:47 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6faec8b069b14d00d6ae1b4856a09e8cc46847a30d018e0b4d7cfdb9573a3d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4f032a957d4d63524dfb7c1795906115aa853dbed1ab286d6340f0fd31809`

```dockerfile
```

-	Layers:
	-	`sha256:0fa2c1a631bf035d540dcb52ccea5b8b66590d4452ded4de253c9b5acf8a453e`  
		Last Modified: Fri, 08 May 2026 00:27:48 GMT  
		Size: 7.4 MB (7410132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0f04e70ab0baa2c2d0c004536500e29402bfd2974fe85ddb0b1bc5bd9b3a658`  
		Last Modified: Fri, 08 May 2026 00:27:47 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

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
