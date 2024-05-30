## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:554dbdc94494889f2b55189cacc5526607af1af003a17cd25586bbdcb52950ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f0795f2b0310c7158df07334d4ecdfd764e059c54d3b77eaeeffe9808d84515a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243114585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f7d2353ca7423e992dc840365729c74a16430590441cc756513c5e03e1d08f`
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
	-	`sha256:084cd2598fcf7a9e095da3754e9b2795b89caa5de0b755d30dc04395a6ded66d`  
		Last Modified: Wed, 29 May 2024 19:57:16 GMT  
		Size: 145.1 MB (145095011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2dab6d1be25ed6dac9996bc7fc665b53b249facf5a5a9cc728209e03d6767`  
		Last Modified: Wed, 29 May 2024 19:57:14 GMT  
		Size: 68.9 MB (68868118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fceec9a83a01064f0e73e78ae5ac6f97009cc18da8f07a6e9731772a00d2fc2e`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240afa2a991362756f073b6b4787cf67c2af3c7faec49d1eb992a5b70ee9f797`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb13ac023a07e39c1308fbba6ded7689746b6a4dc4af6be1415d9cea156a5906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8315bba1988885f239ae7ed08aa1cd0d27373bf7880c2d409a510298cf6224a9`

```dockerfile
```

-	Layers:
	-	`sha256:9340e563b72bf44dc97776d8421aa6df90bee55166ff1c32faf496012c52d213`  
		Last Modified: Wed, 29 May 2024 19:57:14 GMT  
		Size: 4.7 MB (4704939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78815be805a4cd3a0ea48ca8bee8b646041f0fe1451778df9e276e19f0aae4ba`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

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
