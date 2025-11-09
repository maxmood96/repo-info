## `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:7c7dd9af88507081f1be7ece156434b3e679a07d3499a23fdba1f10e45d39d50
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:03374e01ac83a2689943b2a1f818c7b0ab370afaa86db8009abba4205e5b2c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242757924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff68f0fb967a733ba83a96d22c5619fea99cb61683809772c2ec416532d183b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:43:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:07 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:22 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0436715264d0b8e21fbe44e8250538bcc9b0ad17d15d959bf5b2cf5bb7979672`  
		Last Modified: Sun, 09 Nov 2025 03:51:04 GMT  
		Size: 144.8 MB (144848051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2340aea45c7ec7f13ebe5f17651c52c9314725f2fb9c7815e5776c3ce5cba7ab`  
		Last Modified: Sat, 08 Nov 2025 18:43:53 GMT  
		Size: 69.7 MB (69680264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fde6c468467ee52639aedc6e1c49e036316ae3616b9aaba9eaa20fd4229a2d`  
		Last Modified: Sat, 08 Nov 2025 18:43:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff5abb36473ae1bdcb0bf185fa514ab0c288c87a90c69ab49998a4ed2ac5a37`  
		Last Modified: Sat, 08 Nov 2025 18:43:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b32e7fc1e6b9968ea27ef01cce02479d566566847e8016e32ee128598db914e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84783e31b744fa7fb041eb00a2d79078eaf6b608d285790db775568c3017747f`

```dockerfile
```

-	Layers:
	-	`sha256:1ba189665190f3b7264940cab64a2d7fbdc2371da2a65403762ac5ae9b1c7b0a`  
		Last Modified: Sat, 08 Nov 2025 22:41:10 GMT  
		Size: 5.1 MB (5113390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea3c68b6719f626e6b24e65dc14a6b52ffa701a165808b6126e10ecd5f22414c`  
		Last Modified: Sat, 08 Nov 2025 22:41:11 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e605c0f7efcb07d3ec86e0195d4d58aa6694acac19951bbdaa7a7df81dca165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241343850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217f9bf6393436972dba8a9d03bcbd7f453f62bd04551bc4cc5dff3e64d46dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:42:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:42:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4a8cf669b443f60fea528c8903ef54f42cc746d80ce9f8604361f417c6429`  
		Last Modified: Sat, 08 Nov 2025 18:43:04 GMT  
		Size: 143.7 MB (143680023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e1846730ff64a1d9b83d4fe5f25d2fc9b6b8d61724b039fa6fabfda7870bda`  
		Last Modified: Sat, 08 Nov 2025 18:43:33 GMT  
		Size: 69.6 MB (69560410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efd8d041f5e4a0d2e3da752a35034635bb577c2de84794b828ef342369a2219`  
		Last Modified: Sat, 08 Nov 2025 18:43:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dfacf23e367ea092af39b2d81ebf7300ebb4672c87a3bda560704b629e6524`  
		Last Modified: Sat, 08 Nov 2025 18:43:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f4d6b82704591a80c0afb56ef3cd36703711e1bc919e305c00dcf62d925e838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9c930df978c968514023577106b01f04061a16ff12bdc2e1ca48ce6617cc1`

```dockerfile
```

-	Layers:
	-	`sha256:3ec30c76dae23a7e183c8b20fc6de070a8a44b6660072f7a880ef50ccbdc2920`  
		Last Modified: Sat, 08 Nov 2025 19:35:31 GMT  
		Size: 5.1 MB (5119151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed2f2c7b1c7119a8f21fb24431253461860635b01e97c55e8b4622711e1e44f`  
		Last Modified: Sat, 08 Nov 2025 19:35:31 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:45de003315e579995de03b2e7e702cc1c114496ab964bf6cac87dc26b1ff28ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252108597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50549e025761d9904d5dbe636ff0db97c6c60681f2d684c52e94d0c4b5095627`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:14:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:14:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:14:55 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:23:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:23:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:23:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:23:30 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:23:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc3022c7410c457d51287dbb7e81e407dc7badac69c919f9c8b9350ee668d2`  
		Last Modified: Sat, 08 Nov 2025 21:16:18 GMT  
		Size: 144.5 MB (144525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e3369a986ff7cdca76c5943addc82fde6683645fd44512cc6faa039da737b1`  
		Last Modified: Sat, 08 Nov 2025 21:24:19 GMT  
		Size: 75.5 MB (75513514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa5da15b25fff94598f774842fd7c4e8c4848b4272cdd92973a50484244a03d`  
		Last Modified: Sat, 08 Nov 2025 21:24:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec5efcc9e610cad5f8af2cf287a4abbfde32dcfcd4be6900700ae24bbc3e457`  
		Last Modified: Sat, 08 Nov 2025 21:24:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4636c6554449486dae84992fe75dd1c5da3e094e1fd7f6ab9e7edccb8165e80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4396e685bc0ef987dc0adeed1a308af78e6a7c194110413528b856c4ad5e68`

```dockerfile
```

-	Layers:
	-	`sha256:f46f3cccd4714b0bf8ed8e06f659dfa5beb9a14c5247d390a0ccb8b062e5fda3`  
		Last Modified: Sat, 08 Nov 2025 22:41:17 GMT  
		Size: 5.1 MB (5118548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b203d12e63d848e32eb8f8bdb99905192e22732d46de23aa4977056b8a5e9b`  
		Last Modified: Sat, 08 Nov 2025 22:41:18 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:85385a7c2f1e87f9ccd68d55b98e72469233f0b32f54ed8036b37f9806dc13b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230235200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b34ddfb3a3ac624cbf871955191b804b9b3b9616b5942d62d7adda6e837c871`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:36:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:36:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:36:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:36:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:36:50 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:42:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:42:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:42:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 19:42:42 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 19:42:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336253f18c72c35afb6b4d26a3718343fb563b23438c2a33f099c29342a0ed12`  
		Last Modified: Sat, 08 Nov 2025 19:37:29 GMT  
		Size: 134.9 MB (134859055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8397c7be642e581497a6294343141f787f6526cb35ae64bb2c54654fc3c36a6`  
		Last Modified: Sat, 08 Nov 2025 19:43:16 GMT  
		Size: 68.5 MB (68490552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a56cf268b0484b4b32be3440498fc15ff362840cd068cbf0a7fc0cb6053b9`  
		Last Modified: Sat, 08 Nov 2025 19:43:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0038524ff801087bf71624bc3eb7aae648d5d8bd66d638bcf92de037414163ad`  
		Last Modified: Sat, 08 Nov 2025 19:43:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e83c51ce5a7ae9d060dcdb9c5a87f4a0fd6969f26ce443f24c754abc4788b2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b5f975ea1f1b50c63f020aabc5b36f7a62e0b55e0a3d66e3e0812687ce9cb9`

```dockerfile
```

-	Layers:
	-	`sha256:f283e735210ab9351860e3b47ca4d4f3eb68960e2295bbd5addf883398311a1a`  
		Last Modified: Sat, 08 Nov 2025 22:41:23 GMT  
		Size: 5.1 MB (5104711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d1c303e2f447be8512240e5b2fa85f7b991b00c4a31e6e59f2f6de6870893f`  
		Last Modified: Sat, 08 Nov 2025 22:41:24 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
