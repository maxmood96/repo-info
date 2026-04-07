## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:901fa20a7954cba5b92afd2d544a6f68e3fe8fb45c4f80b6049f81420ea7627e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a5fb9d5d5bef16f2d7ae9adb83fbcbed0a6ed33a73cb9ffbe65e8237005169ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281208445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7969929d741458dc782d9818e92d0faa91888cfe2aaeaae1ce0578ac63b746`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:16:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:16:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:16:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:16:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:16:03 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:16:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:16:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:16:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:16:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:16:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1286b944f505bc80fbc4aeecc5f849290371552af75c16e88f5c6eafa9e7467b`  
		Last Modified: Tue, 07 Apr 2026 03:16:47 GMT  
		Size: 157.9 MB (157857076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d99bc069d7b1c962589e910a0ee024c48e22b05f13c5355663d1b08815794f`  
		Last Modified: Tue, 07 Apr 2026 03:16:45 GMT  
		Size: 69.6 MB (69587532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d9c3d44c01c119a43cecbd57ca1c83d4e47f98a586220ba3282da3a640e8f2`  
		Last Modified: Tue, 07 Apr 2026 03:16:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65fc5f1259efad1acebc2e8fcf9cf99bf7c7ff2aa673b589c43bcc29cbcd724`  
		Last Modified: Tue, 07 Apr 2026 03:16:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:38d0400dc85ff3ba0e569fcb72cf2a90f774e89162b15178ccb9e366045af7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23cd95788da7c865a5ce41117c0bb5b462b3aea1a8d0888cb04c7fabb19d19d`

```dockerfile
```

-	Layers:
	-	`sha256:38f1099f38e5662cdec59df8e255b2332b7e530d834f96890c8871bff1e59390`  
		Last Modified: Tue, 07 Apr 2026 03:16:43 GMT  
		Size: 7.4 MB (7409505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c749f047510027d510a4b153d4f6824329f9669d980e5d84cd72fa9d664d760`  
		Last Modified: Tue, 07 Apr 2026 03:16:42 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9cbdc61b5960512575feacb4039fe95a5f11c86b23eb8b31b407d8c62d7c8803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278110556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb1fa9d9531b04bffa5a27ae47a3d4ff809cc25d52306f5ceff5164f65ee199`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:26:50 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:27:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d17a15d9e5d8eb7f17ad5f3434c8bec5ecaec69d8b22e8f65d7eb81a025e98`  
		Last Modified: Tue, 07 Apr 2026 03:27:28 GMT  
		Size: 156.1 MB (156133057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafc4dbaf365d03919a7720458a3dac9a06ac427c52e53b3c93d5922b931f2fd`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 69.7 MB (69728845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04633f1680312b2fc53293b8302f060708c0d2d254a80e694ad58e5f0f513855`  
		Last Modified: Tue, 07 Apr 2026 03:27:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5e6b35e37674193aea21a4f0db1f6f027b07c61fa8e320976dc84a414a0e2`  
		Last Modified: Tue, 07 Apr 2026 03:27:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dfe5cf76e8d1fb17f94424c126c98253c0b8b36472109104c8438bcc4036d774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf1c06458401d4a1515428c290618058efa6ee9a4376c8d1df64818679827fa`

```dockerfile
```

-	Layers:
	-	`sha256:9f02aecf16a25b0d09c56cb8cbe4333f81f2a74d37a978f54db5ef2f61e6b3d0`  
		Last Modified: Tue, 07 Apr 2026 03:27:24 GMT  
		Size: 7.4 MB (7414604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64418c90dc99ad45a5e59e0cbb2237555cd97154cd53fc1cf72393aaf9b24eae`  
		Last Modified: Tue, 07 Apr 2026 03:27:24 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
