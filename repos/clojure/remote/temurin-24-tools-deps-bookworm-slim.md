## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:78b312bf83dfcba57ace46882e2fd367ecc8061861c543b353bc8e63549e1b11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:54e981b97c47696758a848af0603842603e34de5c0f7263b3b7a3d7ddf02d76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187683034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a3057f468e0b3db197c13e02e978315336a741c9493c21404c4b498ba68ec8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9b0c0d24d7638096b6143288c97841386699c5756440e497d54f579213ae7d`  
		Last Modified: Thu, 27 Mar 2025 17:53:45 GMT  
		Size: 89.9 MB (89949052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e90bb82cf972d27990eb23ec29b609c30b253e9c06b615f00a86f08fc10968`  
		Last Modified: Thu, 27 Mar 2025 17:53:44 GMT  
		Size: 69.5 MB (69528076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebec3f65a50117ce286ebf6d1385213b8e93786631796c3768179a883c787483`  
		Last Modified: Thu, 27 Mar 2025 17:53:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7e72d16011ddf726dca1d418225b59e24ecad074314ac151ebb33f3c6de5aa`  
		Last Modified: Thu, 27 Mar 2025 17:53:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:be46e4378bdf349dc06d22a1a8d5b7ec115648812d8c198e0ab7680153f1f3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4879101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1391f826b7a5f33d7ad7fdd7485f3925a6eab18c117b41904562876792d5300`

```dockerfile
```

-	Layers:
	-	`sha256:6982a115481b8f6f863af45c21d4bbcc49b8f1dfa1259d8df006dcaa2b9d8ed6`  
		Last Modified: Thu, 27 Mar 2025 17:53:43 GMT  
		Size: 4.9 MB (4863229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be0fdbed692b1bdc46d6b771bc39217953bd6c179050d6346dea24d0f27bdf1`  
		Last Modified: Thu, 27 Mar 2025 17:53:42 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bb5f0eca29882b692bfbb07bab8e0b3d2dae94011c187790248fb267e832b1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186515884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4461002cc843e0341aabb4a052aec5b0b618b3961c3ce16c642911c502bccc6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ab792ab2fdcccd685a0ff775767fa0fcbf04c694e1e17350177234b03fbe1d`  
		Last Modified: Thu, 27 Mar 2025 17:54:15 GMT  
		Size: 89.1 MB (89092702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bc521b32839aa724b78e9efc0ee71baf30c43b4e8ed61527ee0c4b52dd3f79`  
		Last Modified: Thu, 27 Mar 2025 17:59:31 GMT  
		Size: 69.4 MB (69378105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7c8310271c0c67bbd4a080fa8dcc20dcd0c0db976333cef1277f730f1f4960`  
		Last Modified: Thu, 27 Mar 2025 17:59:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a597e7e4ad100f9d7e94c648186a64e5fe3c7425e6caaf761935417c0b1aaf`  
		Last Modified: Thu, 27 Mar 2025 17:59:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:604e91f9989b84a233513845bd07f8f0f8260a498c3e0a2b92c8a059f91a8a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3021db144d5748d6354ec6b128155e6b767e1fd3ba96fd855a7e44b527bbab4f`

```dockerfile
```

-	Layers:
	-	`sha256:f732aa925d567391ef5b207a171b55d22ab07890c7e463ff00020e3662ce5843`  
		Last Modified: Thu, 27 Mar 2025 17:59:29 GMT  
		Size: 4.9 MB (4868987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddeefb94393affbcdbc106f5bf58dcd046ec109701d4ce1b0d7e3b691534cd75`  
		Last Modified: Thu, 27 Mar 2025 17:59:28 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
