## `clojure:temurin-26-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b10ef1c850bbd2bac746d85954f43ca032c4e7081cc453d1aa1f08ef966df755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8c03afe946539f73d8e2946ac4f3d702349e5348f80300f687911a1a2ee3c4b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217807049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa6bed66f8ea2b9db12737a6adb82a8c08e18f6047b2fe81b4bd101c9ab9dc7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Thu, 09 Apr 2026 23:37:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:37:12 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98806c81404e73a3b185eb16b6ed6b61adeb2eaaa3d859b26d6bcc5441705f1`  
		Last Modified: Thu, 09 Apr 2026 23:37:49 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da71e9a7d5cfa86626f492e57c25bf867b529c299a654ab1ef618591c47fc89`  
		Last Modified: Thu, 09 Apr 2026 23:37:48 GMT  
		Size: 69.6 MB (69587521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65424a2d03d37197f486a18cd2fe5d357f2dd9118352387a72f192093858127b`  
		Last Modified: Thu, 09 Apr 2026 23:37:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1b88913f3605026fab80b533561e72354cb51c29c41568953e8ae3bd379f74`  
		Last Modified: Thu, 09 Apr 2026 23:37:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6af8434e4873ecbf6ea787187559aec564401726e6ad8446a7d0d1262524babf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393958fee9edbc7392c71e1d1ea651c08c3386c00b211bce191bed5ea46cdef2`

```dockerfile
```

-	Layers:
	-	`sha256:0ff3b47c6ec4507f7b3ccbe338312050c978bbc6381648a25654f1c4dff0df28`  
		Last Modified: Thu, 09 Apr 2026 23:37:46 GMT  
		Size: 7.4 MB (7373157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bd2bd8027010babd2df34ddabb6113d6aa52627f5e3136e4889d7b8c70cc597`  
		Last Modified: Thu, 09 Apr 2026 23:37:45 GMT  
		Size: 15.8 KB (15770 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5bf7847b434a2276080c4100f6a9789a159a1f7c28ba2ff2badb3e560da184c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215372378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11d8b7d24a1bc3df74183c0e630175c06d329b903636692f4fecad548e3f21f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Thu, 09 Apr 2026 23:36:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:36:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:36:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:36:57 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f9ef63687cdd1afbb2cb3db99b44a750832b949f7f5ae115b6905380c3e240`  
		Last Modified: Thu, 09 Apr 2026 23:37:34 GMT  
		Size: 93.4 MB (93395164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b94857667fbe237a25bfd9915f7e939dfb0bae05b24d346cf71ffa469dc72`  
		Last Modified: Thu, 09 Apr 2026 23:37:33 GMT  
		Size: 69.7 MB (69728555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76025c2a834d9f19caa92ba4cba5ac755e4691d36ef2df9d739c31cff7415913`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664159c4f21b3c629693818842e9ae46286ed77810e8e3f583aa94502d5e7fc`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d0d8be824316c0a14abbccb5601db8f8eea76d8ab4275e0fa435c372f9ce226e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa3d7ddf38c1336f29fed6ee80da14c90cdb7806c31cc9fdd3f6199b56cd161`

```dockerfile
```

-	Layers:
	-	`sha256:e08b06ebace33a0d73e5f78c1e93f36762c4f8fcfafc8409bd465240f8d50f1e`  
		Last Modified: Thu, 09 Apr 2026 23:37:30 GMT  
		Size: 7.4 MB (7378253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e9d3a0df83ab135733f38fd3c32f3ce8ff713d46039169157243227768d705`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json
