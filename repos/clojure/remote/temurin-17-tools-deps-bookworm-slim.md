## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:020fe9372e8e71ec1bd1bebf9af85313aad7940ee3303949039c9341094ee5ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0a73b68147c2efe0704e3921a6b3b8d54872e063b90cab0c1c824ecd39bd4940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242399696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655940e0f36cdbd6695c1d9a7f49cc9306dd6bbf6577c6e6b6366a9cf468de95`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb909fa4134e33100cbbabc54d5c2dbd39d05f8b84d7de32f2e362c8c917a3`  
		Last Modified: Tue, 01 Jul 2025 02:39:26 GMT  
		Size: 144.6 MB (144634948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b55807f1a8bab36fb82c869704a9d29d4fbdc430dc660fff105f0af9f66116`  
		Last Modified: Tue, 01 Jul 2025 02:39:39 GMT  
		Size: 69.5 MB (69533565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a189708a48da50700ed9105589e4d6b89b3745c11d9a42f6ff63170b37ddab`  
		Last Modified: Tue, 01 Jul 2025 02:39:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fe95746d0ff83227a491f39aa8f1aa53e094efe18f9e9303a443583ed5c0e1`  
		Last Modified: Tue, 01 Jul 2025 02:39:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99437c46df3a6b82b2208710b62c564b09d323fec411af386e75219fa591e0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5127122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883dbac2b6376101532ef00c912fde15001ee8c90ab42088b76d4d651f8a9dc5`

```dockerfile
```

-	Layers:
	-	`sha256:31e754ff403b7ecee6768247371884b926500f0b3598094b1a3b7b6edd761810`  
		Last Modified: Tue, 01 Jul 2025 06:36:59 GMT  
		Size: 5.1 MB (5111244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a9d065794b4dbeb327b7db550ad267039cb067f58523f41cad4e79fb20c547`  
		Last Modified: Tue, 01 Jul 2025 06:37:00 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3685334ae81edba74f08e6878605dcb5dd452298d7b56c70eca9632fa99078e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240982191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27045a012d1920f9fd323dc683a097e5583a0e7092ece0dcc37550951a00755`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d445f89a86a5a0de06289041c3386131f0f843fb9af5e73aae74d3971e03f1`  
		Last Modified: Wed, 11 Jun 2025 19:40:48 GMT  
		Size: 143.5 MB (143512629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7372b8451ed56fe82ad07c018cfaf78c7e4992e922ca07e3d16214f475781ef7`  
		Last Modified: Wed, 11 Jun 2025 19:40:47 GMT  
		Size: 69.4 MB (69390848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682c404a7a8318528106cfd5295a2a2a8cf0a9393d9640733dfa7f4fd63f0667`  
		Last Modified: Wed, 11 Jun 2025 19:40:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed3f95111b2a31eadbe7b7afc288ed5fd926a5cccf7c366b82c26538eabec7b`  
		Last Modified: Wed, 11 Jun 2025 19:40:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a20736466d332fed69c65637b2c8ba1a6902809f9ca7803b558b957e39a09d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e2ca100c5f3b7165517a07128cb1bc87a743c25c88ac3815c953c62bf8f485`

```dockerfile
```

-	Layers:
	-	`sha256:fbc84032ae2d54d6b00b998369b24fc7c8c41fb77cd2ec8d426f9b05ea781a19`  
		Last Modified: Wed, 11 Jun 2025 09:37:22 GMT  
		Size: 5.1 MB (5115649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3b77cdd37f2bf16be1d296535fd2b34cdf865bb4b0922c9268ca08e4c5f966`  
		Last Modified: Wed, 11 Jun 2025 09:37:23 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1c85a68ce8067b35be56de1e6fe379e91db647c3f0c45d3ae699610669cfe436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251712367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad9bdc51155f7f9dcbbb47fb07cdf82a5f32cb74765beeb2c241b8161e21bf2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f944723882769f71d0bd2e9c000bc9d3cd710ee213264d168a19113327c3d81`  
		Last Modified: Tue, 01 Jul 2025 08:44:09 GMT  
		Size: 144.3 MB (144280553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295d4231e9d7649d5391230d0971f01cc43c4c0d56757ae6037d07bbf3a275bc`  
		Last Modified: Tue, 01 Jul 2025 08:50:59 GMT  
		Size: 75.4 MB (75357954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccf4f42b83ff98dc9432aa8159247189e73858f71117ddc6ee78504161b1910`  
		Last Modified: Tue, 01 Jul 2025 08:50:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28270b26781ce3045725b934d95ec60aee14aff42381aafb4fcdf6683b6f9969`  
		Last Modified: Tue, 01 Jul 2025 08:50:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2ef23242548ddfca037b229a5220a1733f5ba572de0f27ae5acf48846fcfebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a450016e91f260c6f8fb67cf5e11045eaad4eeb665a06d37451d6fe60fc4583`

```dockerfile
```

-	Layers:
	-	`sha256:de1f8362084a7560b82c6edaedc3b909b4ae2ca47ded73fe6fffdb6d341c0ea0`  
		Last Modified: Tue, 01 Jul 2025 09:37:20 GMT  
		Size: 5.1 MB (5116402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f8e3ae97a14273801be7bd760e587900dfed91898f7bd0e15f9a5093cba95a`  
		Last Modified: Tue, 01 Jul 2025 09:37:20 GMT  
		Size: 15.9 KB (15926 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6eb2082abe864e4bf8c2c655f07c1f7c1d06009ab2777e7eee7eb3ca93327219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229900701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60e42802ecace4fd575eed0e4e1779a1cff89ff3175452343c46c2fd09b6d39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7853e8c0aa9e0045ffb780b6a0ed5f930dae459195b522c489be21aac2ba66f9`  
		Last Modified: Tue, 01 Jul 2025 08:10:41 GMT  
		Size: 134.7 MB (134673542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913c6a9e0b7b23865c514e41104bf33bbcffbebe83d9388e9d7365e9c337a13c`  
		Last Modified: Tue, 01 Jul 2025 08:14:45 GMT  
		Size: 68.3 MB (68338307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14718acb05f766dd1d85d6f2240143364178166ffa7e499150d662adeb6fc125`  
		Last Modified: Tue, 01 Jul 2025 08:14:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55c458dc1016d9b8c099060a5b7aed306c3ab6aad5280fa79584ac00dc9b8d6`  
		Last Modified: Tue, 01 Jul 2025 08:14:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12e9be236d6169ffa5f06d95c4ab8559807414b2b1611711715c5dffaf34c5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5118444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c0d527117830da244ba24686261225aee423cbc5084f0216182dff6d9f43dd`

```dockerfile
```

-	Layers:
	-	`sha256:33aa07203b48ecdc32ddfc2aa3622cf59cda6a95560df85e9221c7120f9b0dc2`  
		Last Modified: Tue, 01 Jul 2025 09:37:25 GMT  
		Size: 5.1 MB (5102565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ef36d78191d9c19d4c77ba167529611807fd0e50fd33970fe9d9e4235902c8`  
		Last Modified: Tue, 01 Jul 2025 09:37:25 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
