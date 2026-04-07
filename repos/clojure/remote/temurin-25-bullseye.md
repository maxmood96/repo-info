## `clojure:temurin-25-bullseye`

```console
$ docker pull clojure@sha256:6957a77c2993cc84bfa3be728eda65b909b3aaab484bc615a93d385f87808751
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:898ff486d89fac440730cd496244ca346595a78c2385a056a994a8ba1f141fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215607708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce83d20ebd8e58a0df6cd865f78ec3e760c143a70171930d1a41a47dd352aa5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:17:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:17:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:17:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:17:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:17:14 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:17:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:17:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:17:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:17:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:17:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5410d930d4456ae13af316713e237da39ab63bd37407f3f315336bd80c6e1dd8`  
		Last Modified: Tue, 07 Apr 2026 03:17:47 GMT  
		Size: 92.3 MB (92256301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2a8a63030cfc7afa836e78b79f7e98df1438c31aff9742616acc76153750d5`  
		Last Modified: Tue, 07 Apr 2026 03:17:51 GMT  
		Size: 69.6 MB (69587570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318594da2c04c5ad513f057ef274bf8b80b2499c819073b07a21e103880a2562`  
		Last Modified: Tue, 07 Apr 2026 03:17:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f485ad38a2533f2f0f614c251cf9d069f248475fe528659f6a0037d407dd8ba`  
		Last Modified: Tue, 07 Apr 2026 03:17:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f8ac54b12dddebf1e22ec0e44eabb0f75b7733561d5ca07e68e7c2c9b7d84d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee07869a03a5e38323dfedc61aaced95dafc448e228d3dd38a6adab73a3c97`

```dockerfile
```

-	Layers:
	-	`sha256:04fe93774d8e6096ca3ed09c0466b25dc7e03c21ef7ba69111d054da4873e7c8`  
		Last Modified: Tue, 07 Apr 2026 03:17:49 GMT  
		Size: 7.4 MB (7375727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba3ae4d52fc798f0e3ebd1da84cb57f4b43796481fa18fa74062ba70bef151ec`  
		Last Modified: Tue, 07 Apr 2026 03:17:48 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77db137b5067a6555ff5a853c3b9c7e45b07f56f1c43c1fdad496a2ee1e9df42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213265533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d156301e31f24f95fba7af00d9fb6f64aa0764f4173c64eed6db11b7b26a7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:28:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:28:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:28:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:28:10 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:28:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:28:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:28:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:28:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:28:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd411d6fc473f42818113b56a5c06de8532fff18371f1b5ab4ffbcf7d16db5cb`  
		Last Modified: Tue, 07 Apr 2026 03:28:51 GMT  
		Size: 91.3 MB (91288270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb2d2ab4a76ff51c061fbf2b5b3e1193dd54547649b2ab587b9475d7b577679`  
		Last Modified: Tue, 07 Apr 2026 03:28:51 GMT  
		Size: 69.7 MB (69728606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c640124b358af5daf7047730c761248a8ee22c1bc2a87bcdba79780933c756`  
		Last Modified: Tue, 07 Apr 2026 03:28:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d569c6f725dda5e6083f22a3de17b8b4ee79d26553618fdb47c3f58881ae0`  
		Last Modified: Tue, 07 Apr 2026 03:28:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9db83d6a52df28bab67cad34a8b188e3c712022f1d6f2b3f2ea3f626c9a52d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdff21d2dec346a1bde0166a635778cb520c459bf6b9a0beb02190327c8199c9`

```dockerfile
```

-	Layers:
	-	`sha256:476d300dc5f6e85bb05e584ad312a21ce26e277b1070c1a58d3b3a0b2220f94a`  
		Last Modified: Tue, 07 Apr 2026 03:28:48 GMT  
		Size: 7.4 MB (7380847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecf2486d3fcfa83c39eeab79c476d7efc8a1dbba0cc1e4d611853a5428985fc3`  
		Last Modified: Tue, 07 Apr 2026 03:28:48 GMT  
		Size: 16.6 KB (16588 bytes)  
		MIME: application/vnd.in-toto+json
