## `clojure:temurin-26-bullseye-slim`

```console
$ docker pull clojure@sha256:b44e8f1a0eac11471d576f9214278d3532be20a8407d51f60130ec332d8f0374
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e884d205367846fc5c5c5007c2b1b549d3cd37e7183200cf5c21f58af8a3f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180883349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cc0435a2d6367430571f74c8d75fed1b2161a4a681a9353f39414e17c29369`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:48:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:48:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:48:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:48:01 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:48:01 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:48:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:48:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17d8d097b3efa5983b3abbffc06be88ed3f4732a6882f94780113438be39fc4`  
		Last Modified: Thu, 04 Jun 2026 17:48:35 GMT  
		Size: 94.5 MB (94524331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873b6ed655a086837d81094f36a8c4514032516d8a6c0e536ff2eee66b5ab495`  
		Last Modified: Thu, 04 Jun 2026 17:48:35 GMT  
		Size: 56.1 MB (56100378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b601e7d555a44eb1225ec1c4febacd734cf642d9d9e6504be8d3eef389703a`  
		Last Modified: Thu, 04 Jun 2026 17:48:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b667116f03481d2ad5afacf3264694e3e196d4b2a3f35bdaf528f63a56b0b1a2`  
		Last Modified: Thu, 04 Jun 2026 17:48:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:96b98875aeb9cb922d75ad619de6a3505cdd8184fcf9e1f1a33e9c091f94db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5298719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6b913a4dfa26c0d6d4d47f376d2a106462f21f0cc5dce75876e686b4b7a92d`

```dockerfile
```

-	Layers:
	-	`sha256:4d91ab4f19ebc33c4e13648634960145363d8e2884857662e3bfbbbae9b8eb6c`  
		Last Modified: Thu, 04 Jun 2026 17:48:32 GMT  
		Size: 5.3 MB (5282736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0204c6350c507d3c1c41e5e2a41ede4c48090a681b6622b926ba2477b96ef855`  
		Last Modified: Thu, 04 Jun 2026 17:48:32 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a8eef12f3ed06f631638df357e6995ad363cc8bc42addcd3a22e660289d1e15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178515990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63cc70cbb9b8eef3f0d72a434196c9d7938ae4a5742f3f18ede271a6ccc18150`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:47:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:51 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:48:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:48:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f134c38b5abf73e616d167df6f0bb12a51051cf67558d1f0d3284e02ec5a2ec7`  
		Last Modified: Thu, 04 Jun 2026 17:48:25 GMT  
		Size: 93.5 MB (93504349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92d81b03070d9d9f499e2f36a8a7e1603c3c24076316b7c0166c4fec42199a1`  
		Last Modified: Thu, 04 Jun 2026 17:48:26 GMT  
		Size: 56.3 MB (56267631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f425ecabc21e27c922f0b25c7af133adbe6b6431cee8122fdb6428e8546984`  
		Last Modified: Thu, 04 Jun 2026 17:48:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4e0957a3db81460f149a390148fb9bf63759157c9653a6a1ad19b86b52c645`  
		Last Modified: Thu, 04 Jun 2026 17:48:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:335e18136eaf5d85ac4ac65dcdcca4fa40eaeef4bf8f8a56487584727a5b89da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0757ec764e31c465cc34cb7fe5ae294901fc5eb6c806203c765fbfe1453c5ea9`

```dockerfile
```

-	Layers:
	-	`sha256:14307d14c62430dfc0d104bd62d4d03a8d10038444439e971dc334373adcbb7f`  
		Last Modified: Thu, 04 Jun 2026 17:48:22 GMT  
		Size: 5.3 MB (5288465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1290075e8f3713692ae80f216b10db644fe90d3bcd9b4d38abec6471bb83e999`  
		Last Modified: Thu, 04 Jun 2026 17:48:22 GMT  
		Size: 16.1 KB (16100 bytes)  
		MIME: application/vnd.in-toto+json
