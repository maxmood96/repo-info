## `clojure:temurin-24-bookworm-slim`

```console
$ docker pull clojure@sha256:723127409492ddd17e2982d27787feb3344c9ddaebf545324988a23efc3fd314
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fd9a5aa329b6272dd30aba140aec76211e33f9e3ee9df3d03e94a2494787dc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187705682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955537d29b471453b3d2becd1ff5934cd747863fb3722cedb3e64589714be3bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0be7d4ba871b58c198a66ea044a3318771397121f69ae6bde737ec81f9b150`  
		Last Modified: Tue, 08 Apr 2025 01:36:59 GMT  
		Size: 89.9 MB (89949035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17b24f15db2b1d4b29f27a4138ca73d13b92ef6e903d74f10e60e27d74a2a6a`  
		Last Modified: Tue, 08 Apr 2025 01:36:59 GMT  
		Size: 69.5 MB (69528347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6d4862de01f97c3644c5da906a86159d7b8074ecf6074e91c1495156d5179`  
		Last Modified: Tue, 08 Apr 2025 01:36:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28323bd7b90685f9daf90a23e4fcc0435d19aeba1bfa24ea86d52edd9915ef66`  
		Last Modified: Tue, 08 Apr 2025 01:36:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8eca95e8fc5268f6713dcbfc209644077d86d56310db8231085e390e34952933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083dd07ccff7e36ebf45f37e35b81ae2cf479e31350092ffb1d8a80d4bf90d1e`

```dockerfile
```

-	Layers:
	-	`sha256:1630b018da9cf67288d5e8547f6f1aba9cdc9bbfa01ca1423c6d620deccfea99`  
		Last Modified: Tue, 08 Apr 2025 01:36:57 GMT  
		Size: 4.9 MB (4864597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61369e04e7eb8aa9fbb2a717f1c4a01ab0fbdb634a6884e34c57113a3f7e1bb4`  
		Last Modified: Tue, 08 Apr 2025 01:36:56 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

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
