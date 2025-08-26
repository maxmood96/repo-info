## `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim`

```console
$ docker pull clojure@sha256:e4a3c34c28a9a440053b8c3eab5fc858a5f5a6e4779b530c4648579aa165873b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ea3362d258be2dd11d3b83287b3e8ded3b17e6e1087f62b5d8cf4f50c186d487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187882741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b4c67063d7978136f90a3bc263e9a5a13961e48d1b073fbdc395c0c622b505`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322222ab55417e41b3bb9dd10ea48d266a1611d944d7787e075aa3866992642e`  
		Last Modified: Tue, 26 Aug 2025 17:27:33 GMT  
		Size: 90.0 MB (89975158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c441fca0726af8e2c5804d3f2e55618bd386a97b0e1ce37f9b9459e31220b44c`  
		Last Modified: Tue, 26 Aug 2025 17:27:33 GMT  
		Size: 69.7 MB (69676288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e81cdc113ec3de5e2c3cce89ab9b1cae9ea62cfe279dcd1ddeb219ebf5839bf`  
		Last Modified: Tue, 26 Aug 2025 17:27:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01269b70db0f67627da9a2d72d771519948366df98d54ec88793828a2f81851`  
		Last Modified: Tue, 26 Aug 2025 17:27:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ad324a3d7961c3618852c279062c1b4ab0297e3c6b4b78f408d414add61bc17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5f23dd670a07ee2b5fd058f2756a79e6c19455263505c7922aa763da28e1a3`

```dockerfile
```

-	Layers:
	-	`sha256:0d64e0f8ea97f7ecb323ef95bb6572f72010c5d891fd0b7dd872e058a02783b2`  
		Last Modified: Tue, 26 Aug 2025 18:41:58 GMT  
		Size: 5.1 MB (5061921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c9fb9e3e06630e7ce180ec15f58920001e5fac44dc8cc0361ea829054f6bd9`  
		Last Modified: Tue, 26 Aug 2025 18:41:59 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b550d3df6bf18e0a824b241aa3a231114ded00621082a7bc378625f5b6bb625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186725040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef11cff56acd88b2a8f84079fb12e251f89c2c4634977013b0f138fe323cf4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e6bfd40fe1f401c5b893a66ab4775a180924c4ca26ac82e4428bc83ebf62e`  
		Last Modified: Mon, 18 Aug 2025 17:21:15 GMT  
		Size: 89.1 MB (89092530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f7975630abfe129c003e6161941bf52aa7975c07d762c097b2a02847dc605e`  
		Last Modified: Tue, 26 Aug 2025 17:55:30 GMT  
		Size: 69.5 MB (69549465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a760f22733f743d3feb36473008c7db3808d576f4cfb179090fcdeae8443f55`  
		Last Modified: Tue, 26 Aug 2025 17:55:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0013c0b9c120b51edcdaf70952bb17792dfe4d8af53a7059fa91dd9e0cff4b84`  
		Last Modified: Tue, 26 Aug 2025 17:55:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93c25a85aea89169cc70d109029e833fceb902cf44e7fceb8719c4da47737dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41d9f57562b47f9538124452d46a8d601404e08ee39cfef27919a1d781ef3aa`

```dockerfile
```

-	Layers:
	-	`sha256:91a759407031bd9dd5fdf66f1993a3d9ef5e3a46c58ceb60b213e499e5421bf2`  
		Last Modified: Tue, 26 Aug 2025 18:42:04 GMT  
		Size: 5.1 MB (5067679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ea083b9c594907ed7e2bd97449fce318a10e329e683dd41e95fec693f38924`  
		Last Modified: Tue, 26 Aug 2025 18:42:05 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
