## `clojure:temurin-25-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:9b7c2ab01c155b0505e94a1da7b5a6616f4e2b4db9b16821a9a3810141a9c4bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a2eabcbcc1569fce68c3135c9f8d7a0a37b6c52c68817fe3465d45c5d8ceb79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215621456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a86d6012bbdea7f23d743acd7044504bc857f22f6c0acc0d6dbad92cc133283`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:06:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:06:44 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b47c027ad0f47e2002261dd2e82a36c096ae4f0c969b6056351ca1a23f02e3d`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 92.3 MB (92256319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510e84f309e797c15fdeea4645c9dbbe236e13030271be8d2bbc442644bb7f85`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 69.6 MB (69601299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c5529f4387a1dcc4e15a03201082aa29c27434fd6c8a76f7819ce236f4a151`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76cd141a7d6de05e80fcd5fb50c2e7ba25be79387fe9adb9945c41c3585fa6`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f1d64ddc5312be464b3ab24a2599a9332872f82080be373ddb2d4a68b3ad3c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae28e2343276f766a9fa2265594ea19504cfa643cceb618c039ae0f8cc680d15`

```dockerfile
```

-	Layers:
	-	`sha256:319072fc4709640f3d78e1a37bb91a0980e26e3f42ae9410ba486f0148ba86c6`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 7.4 MB (7375727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a101fd47559ec2be10efaca46807c5c62d3520e52ae1e8b2f23ae286b0d4019a`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

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
