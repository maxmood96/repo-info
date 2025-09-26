## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ecd56952babd94e2ae17dbce4895c4926567625b7c3bcb3d284fe38a51ea2239
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1e5be3b553631f95086c244caf96e0462a1025d678c4216b7e3121314cbc7b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247213427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4818213275b0befeed9181cb80b4b05193e3e9d9a6ff62fecdad9f5a81ef7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4783e427914fcc189b6a01155fa69f26f0721829649e65ec58648cbc9086838`  
		Last Modified: Fri, 26 Sep 2025 20:01:53 GMT  
		Size: 157.8 MB (157804740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b626251e6b237c74ddd206c678b77448c5866aa5fe7fab2f438c18a695767a`  
		Last Modified: Fri, 26 Sep 2025 17:58:12 GMT  
		Size: 59.2 MB (59151578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb19ad038199c0c5788aefd66b6d12032866d8b5b0d6454c7c294a587a24a826`  
		Last Modified: Fri, 26 Sep 2025 17:58:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484dca1d89fe8672c85c75ea5b54a601d136e8f6c71a39e45abf34201e48bee`  
		Last Modified: Fri, 26 Sep 2025 17:58:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a9301d34b51c01f4b7e14f92903d5552409bc9b6417820eadfa15617adc9400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885c03e8f1aa3bcc87390e19f3191a68ea22797651e219e708bc01ad37184aee`

```dockerfile
```

-	Layers:
	-	`sha256:5be56a017760b51176957f9fdcc24209ae1308a8eaae52399bde0d9a5b3eed0b`  
		Last Modified: Fri, 26 Sep 2025 18:41:38 GMT  
		Size: 5.3 MB (5311169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c4c2d065ea05c1ca7ad131f2c3458e689ffb0e127fdb9cded62c51e610ab93a`  
		Last Modified: Fri, 26 Sep 2025 18:41:38 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e6a4415399604c8ff84d18ddc259458968af6a531bc5adbf4e6a395c6b9b0e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244119004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb195de6240893793b158583fda2da7ec132f39c3074e07cd8e379b9fd195aff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0fe1823193cb3e358e4db43f41fb28d718a20b91e91bcedb9093cc941b53c`  
		Last Modified: Fri, 26 Sep 2025 20:01:50 GMT  
		Size: 156.1 MB (156081186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d72435e217559e650ff2b287c6b1f980655bbe25c116d2d51dc65a9f4a03521`  
		Last Modified: Fri, 26 Sep 2025 20:02:11 GMT  
		Size: 59.3 MB (59286319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d5dc9982e032731e71bbbf974af9975ac6b5ea8772ed53ea6685ed9c3a3e06`  
		Last Modified: Fri, 26 Sep 2025 20:02:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d718182cc82675f48b6d42d1104fbcfcfe684f18beaa97d58f8f458d821f656`  
		Last Modified: Fri, 26 Sep 2025 20:02:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e2600de637d77ad0c40d320d1b97f084cdcc8c78ad0b4c02f3041833c19ef4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca91bc27c0fec095971002125537fe99c2bcc34983408bc6d5dbb7bfb1d8b0c`

```dockerfile
```

-	Layers:
	-	`sha256:5d5c5e36cc15a7cdf26e36d1828eceea2225f8bd455963333b6d868f018a3619`  
		Last Modified: Fri, 26 Sep 2025 18:41:43 GMT  
		Size: 5.3 MB (5316901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e356b76baa5529472e3d67dd323974f1215bfea5d47405f5294613242fc58db8`  
		Last Modified: Fri, 26 Sep 2025 18:41:44 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
