## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:d7574f3e7b2c6260b044ca7ab57c4000bf8884381e4ab057b484019cf3545cad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:de7bbd4aeb1e52de7b0acee035c601e2f203877102283c94f6e201df7193ce1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177642584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d01aec42386734102f2e31976c330dd26d9503fd7d658c1b944f408e7ab5b5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ca18aa3ad48ed7c5539a955113449017aa0d8d9f1bd6db609a3255fe34e7da`  
		Last Modified: Wed, 29 Jan 2025 21:08:06 GMT  
		Size: 54.7 MB (54711737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032efded534b11a74f4cf21aa8cde4f26dea52018f7711524ab1680cf952cab7`  
		Last Modified: Wed, 29 Jan 2025 21:08:06 GMT  
		Size: 69.2 MB (69191037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d16b6efe4a40c393934e615b756c2ec72d6cdcaa4e64a97f12a411e6c8f474`  
		Last Modified: Wed, 29 Jan 2025 21:08:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a8a001416802a47cee28c2c3a6efebaf86f510a80f6419724e4978f223934906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4114b64dd035eaca14d8c54008f913154323ee4138058208284fc192e93ea749`

```dockerfile
```

-	Layers:
	-	`sha256:b3a58c12f967d63a3c195bc1f64ff9e3b7a9c8175ab3088a86fc459772aea236`  
		Last Modified: Wed, 29 Jan 2025 21:08:05 GMT  
		Size: 7.3 MB (7326165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa57f8d612f71d36b20fe5e6bcd4acf84d9c5a68c4741c9f2079c7c9fc655cff`  
		Last Modified: Wed, 29 Jan 2025 21:08:05 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a060db5c994d20c22b4584989be5890cf1d9bfea7fbb2490f30b57e9dbbcef37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175374446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032ece9b0b924453ba6960a46855b2dafba63da4876fb611448a790ee7c3c57f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef99793a2d8bdc381daf53998de5bd5712cc60ecc715ece4034ebadad9db1c4`  
		Last Modified: Thu, 23 Jan 2025 02:26:57 GMT  
		Size: 53.8 MB (53816395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bfe74b559f99ab421d2a8be6b9a47c3603436f22187f99d3720f7b8ce411f4`  
		Last Modified: Wed, 29 Jan 2025 20:39:34 GMT  
		Size: 69.3 MB (69311347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851d094bebe042c0b3c0e9e1c0815d55427ac030e8562f851c751a7c32b9bcc`  
		Last Modified: Wed, 29 Jan 2025 20:39:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1f4a779b6eaac6a04eadd853f6dab436a1a36919201c3528da273dc373b2161a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47acac440d4135fec87c4e67b9cbcf49f045d063d30b55e60b7aed8a39566033`

```dockerfile
```

-	Layers:
	-	`sha256:ffde343c572de610eff5cc84b630205f570380445629b93dd59ce65ac3758c09`  
		Last Modified: Wed, 29 Jan 2025 20:39:32 GMT  
		Size: 7.3 MB (7331962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac72a3f40286e530899ac02826ec94724b23c7a4e6fa4584253c6ab25cfd1146`  
		Last Modified: Wed, 29 Jan 2025 20:39:32 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json
