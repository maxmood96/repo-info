## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:1a51108a7dbad5d69b29a7bd22c08261218f956a30bb6b69dc8ab6d6b556744b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:786b9ddcb0a42e9349cb79e338693920e844f48428c079c637df2d3e6ce9807e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243115176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cd3ae1bcd85a6aece8b6458a39fc933c93800895ed42e1e0e11a6c26587de5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c27c506ae9a92327a0e91feb06bdbf6ca47bf557a5163145f38a18de3c89aed`  
		Last Modified: Wed, 05 Jun 2024 06:10:24 GMT  
		Size: 145.1 MB (145095123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5933d949c8c76661296c769f95e0e7ca840be06f46e5836eef103d036c8c8a6`  
		Last Modified: Wed, 05 Jun 2024 06:10:23 GMT  
		Size: 68.9 MB (68868597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d4c957b7c81ff71f11bb7a2262570ccea04926d94967b41ce82c6faa40918f`  
		Last Modified: Wed, 05 Jun 2024 06:10:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f82c78e0c91236dd3e9576ae6f1f7fa8306071da7e537dd202759be6772bf1f`  
		Last Modified: Wed, 05 Jun 2024 06:10:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ac9b6fbf2b90f5bee9cdd5848f336c6e644b38584afe7ab82ef17d64000571d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def88153592a42a4a288bdc17e7b37ff41d2dc7357f70c9b847724b5c115e890`

```dockerfile
```

-	Layers:
	-	`sha256:b4d6ca06769d341957ede537b773b82c9e45cdafb5aa3646aa89afb3fffbbe31`  
		Last Modified: Wed, 05 Jun 2024 06:10:22 GMT  
		Size: 4.7 MB (4704938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbc6a005c36e91e4ace0ba6166ce12857d648f2d9cfaf36be0bf97dfbb4e632`  
		Last Modified: Wed, 05 Jun 2024 06:10:22 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f68b68e68b9be82966bf1697d3e4c52ad0118010b5a1c6650610683552c3c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241694196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1345493d508cf2250bd0d2dea73cbe538d2d694394873ecc1b7b2576d61741a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4858d30acd04ed0bbb40355f5256ecb992b85301a5533550610d7267de1552f1`  
		Last Modified: Wed, 29 May 2024 21:39:33 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be33bd428e96803beb97e65d828137c900c4e546f37d7a23cec90caa575ada8`  
		Last Modified: Wed, 29 May 2024 21:44:34 GMT  
		Size: 68.6 MB (68620871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e721eacadca052c6714f18cb94e60f753c8f635a81559c79d58256bcebe3a78`  
		Last Modified: Wed, 29 May 2024 21:44:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327f6525ee2911cd6a6496c868e4aed95a3c1fad58c307fe4c537b0669744471`  
		Last Modified: Wed, 29 May 2024 21:44:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dbc0b213cb276d7b23dc839abb8933a06a235cbe46526fa0eace701dda56d883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7af74b2cee484f20eb86799e34492751ba435fe9aa37b33f5f956ef1627c62`

```dockerfile
```

-	Layers:
	-	`sha256:abbdc13acb514c6fa94ff73aeda55a54449012e9199d0703b5edcc3278c16007`  
		Last Modified: Wed, 29 May 2024 21:44:33 GMT  
		Size: 4.7 MB (4711324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336d5d55ca57c4c610f5fd690516435a9f0ce9b887e050075251257e582899ad`  
		Last Modified: Wed, 29 May 2024 21:44:32 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json
