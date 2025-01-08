## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:bfbb7d0dd923ba2be323348193eebb05195be014391c9ac686c34bd0d4585884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:81bd115be8c64d9908ca53b7e20b83fcfa8612d3c0ac9d8539d2fbce258915d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273810917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349383526cc3299a0291ab9d97ecc419e34afefcb2d26eea92de93dd4b4c5c80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603fefbdd17997413977a84544da923cb691f54422f3210e600a92acf7b38b05`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 144.5 MB (144536674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f23e744e94c9743092ef41f951fb72011bf2c77037b21fc9cc3ecf8c883ce7`  
		Last Modified: Wed, 08 Jan 2025 06:29:42 GMT  
		Size: 80.8 MB (80776140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f0a604f3e745b00ddcaed5724bd463d5e573eb79008718bcbe736b5985f9b1`  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e606d06a03e7c2c280263ff7153138f120bdffd5ffa8fd573155ab69b1a9f8`  
		Last Modified: Tue, 07 Jan 2025 02:29:25 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:85ccf1c04c833056f897bf3c594ddef177c655f5c7b183a92a9ab1dedcaa3706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5416ec5ffa59870a1b95508bfad6d2bf2d32d1a41657da765cb980eb3b7dcd1`

```dockerfile
```

-	Layers:
	-	`sha256:6564d4b872b2a493e12ea35660854a2ad2c6400fc3c8a113142831aa0bd8c77d`  
		Last Modified: Tue, 07 Jan 2025 02:29:25 GMT  
		Size: 7.2 MB (7171080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ac269d9e5ef6a146fc18156b03f99ddf68a401ba69a1c5e0da03edeb8f6916`  
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
		Size: 80.6 MB (80624403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62e42848e45479c20f3b810fb60d8fe8c796ffc57ea3a56537411fc9f1297fb`  
		Last Modified: Tue, 07 Jan 2025 03:26:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70155cf50aaf627270a5c2f0f6482bbace8dda3ee16679458a0933fe9959743`  
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
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
