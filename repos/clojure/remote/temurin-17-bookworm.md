## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:70ea50a93bf1c1a94fceff9cc46d23315bf4d9fa6168621d509d5ab1caebae0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5ec6bc5f02b27bd031b6fa7470f809c67b9110973b7ba3a5d31ed02de4666908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273995690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88173ab4edeeb1340798355bc6177fa1fcb0aa43a1c67a5890d765d05d56fa39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296772f0b6d96791d34691ccd1c76aee4c0d58346057b00272b2ff1194840308`  
		Last Modified: Tue, 14 Jan 2025 02:44:37 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d69c1c1ebd444f0ff63467027a7ca459fd43799bc37c493d83fd71c05997ae9`  
		Last Modified: Tue, 14 Jan 2025 02:44:35 GMT  
		Size: 81.0 MB (80977972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239d64bd0b8de1f94c6af25b793e4eb372473a9a70bcb39f1bd662f2bfc7c49`  
		Last Modified: Tue, 14 Jan 2025 02:44:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00970dcf6aa9f2124ba93cc80b9b8c2fefd6ae98c16aebe6d77ba5eab44f8ea8`  
		Last Modified: Tue, 14 Jan 2025 02:44:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2181b55c959c1f53b70a6b571cea073dead65f019cc5517e6d9a25668c82d7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fd3953cffca0359b3de85f12da2240f6fc43eb663f9da033f8a4731e6933ea`

```dockerfile
```

-	Layers:
	-	`sha256:0993f9e87cf6d49625b95f9911335d9fa40cf71d67e875ffd74c3b2012a0efb3`  
		Last Modified: Tue, 14 Jan 2025 02:44:33 GMT  
		Size: 7.2 MB (7171080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51df6d2daf7d640fea148b6e898c5f967de3e90b0d66796c7485bc6c5571258e`  
		Last Modified: Tue, 14 Jan 2025 02:44:33 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9909b545be991ec022fd0cd0fa711971fb1d464785261c0d8831cd5b4fd2c040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272311927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2730e52a4b755ae76b58cbe0e55d2f798fdcd0ef7d6b4015375a655ecc93298b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a64b07cf9d984ea02cce7f64d487e4828a776c450c76db8a089be6707a179c3`  
		Last Modified: Wed, 25 Dec 2024 07:24:40 GMT  
		Size: 143.4 MB (143361002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2853fae40e3279d2d8713dd822c8f3f7c60a160efb433763f41aee785e5c8bd`  
		Last Modified: Tue, 07 Jan 2025 03:26:54 GMT  
		Size: 80.6 MB (80624403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62e42848e45479c20f3b810fb60d8fe8c796ffc57ea3a56537411fc9f1297fb`  
		Last Modified: Tue, 07 Jan 2025 03:26:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70155cf50aaf627270a5c2f0f6482bbace8dda3ee16679458a0933fe9959743`  
		Last Modified: Tue, 07 Jan 2025 03:26:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c3f51130bec85d4f9b6dd975cd2f9e8904bee7b72f234bd9b3bd6aa1c4d5578b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e7ca5bc916fccd8c9368a07691877a5803ad79f8290b4f8efa33f04225c422`

```dockerfile
```

-	Layers:
	-	`sha256:0a8d9b17d3a89845fa312a66b4bca07f54e6839d125a7e7306bf742080b3573b`  
		Last Modified: Tue, 07 Jan 2025 03:26:52 GMT  
		Size: 7.2 MB (7176843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a20fa9fdc2d3c96c32905830ead932463b02f63f1edca2a748c0d634a26d06`  
		Last Modified: Tue, 07 Jan 2025 03:26:51 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
