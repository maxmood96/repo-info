## `clojure:temurin-26-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:d3d6a54b36d3a7343d63a990f46f277ec7bed2a72e485789a6e8c08688876874
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

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:261285a626f19b2b76eaa9cef80ac3ea4ab1d41192a01de43fc388159fa44e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193262199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dda4bb5adfa9e0ef45556a6a2c90cb3cf55533e9f8e95ccee7ccc45b7b8f37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:22:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:31 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:31 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a11200d84ce1376e5e89ec3f1dc0edfc5645c88a90608ac004215743173cc8f`  
		Last Modified: Fri, 19 Jun 2026 02:23:05 GMT  
		Size: 94.5 MB (94524351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925a8aa64aa7c136f46dda51a760770b89b6866c51435f68692565c0e9e84a50`  
		Last Modified: Fri, 19 Jun 2026 02:23:06 GMT  
		Size: 69.0 MB (68951390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783059426e14aad9cb5e8479266a162af79f3d4f83db41f5408fccaab4c349cb`  
		Last Modified: Fri, 19 Jun 2026 02:23:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c4ffbec80571af6f6ae693cf498c6b936270dd0f513c0c5791527edf52ede6`  
		Last Modified: Fri, 19 Jun 2026 02:23:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7777b6224c50b57f960566a6aa4f6e7c0a4ef2452e10650643ad17562fdaff5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e5a1651ef6ac6dd4e811314ff1a163bbb10ff5f147addd406e10c675eddceb`

```dockerfile
```

-	Layers:
	-	`sha256:213720aa5af4ba97adf912a4a2946bbf357a3dd6d3eb226aecdb193c1b803929`  
		Last Modified: Fri, 19 Jun 2026 02:23:02 GMT  
		Size: 5.2 MB (5222133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ffa66473ed5c842ad8f41372c86b05b8493bfdaee3434a4e8ac447dc258be1e`  
		Last Modified: Fri, 19 Jun 2026 02:23:02 GMT  
		Size: 16.0 KB (15958 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6deaa21270ecf21c0cffcb1e5437e3102c193531736a540a41035753b207913d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192431361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad9f0d6f4493c8086c682f045b5b55726edd50f28cc50952cec3f54fd0148b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:22:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:46 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:46 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:23:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:23:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:23:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:23:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:23:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22375540b11219c060ba08087525214f3c6c802deb60af874d8be902f63a0a47`  
		Last Modified: Fri, 19 Jun 2026 02:23:24 GMT  
		Size: 93.5 MB (93504337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a4c518b18f0fb3f7bf1a870a357b37049f5fb125cc51502e37d10a8988c0c`  
		Last Modified: Fri, 19 Jun 2026 02:23:24 GMT  
		Size: 68.8 MB (68777449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11804ab09692618b65835d47deedd4044952a052358e32b875ae70e7181a0d2`  
		Last Modified: Fri, 19 Jun 2026 02:23:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596293e034c90b7af90908ad398738c09ecdd14b053439c48ed71bb969967165`  
		Last Modified: Fri, 19 Jun 2026 02:23:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bff101b7e18468761837df16a9b392ccfb2935a1c7a37d37cdfdcbf56340deaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a83ae6397135bb42fa9bf659773ece963d1d944e520e3b0e78ccfa1e63874b`

```dockerfile
```

-	Layers:
	-	`sha256:22999a36ea6cd5af253aaf4062ae7f66a6782e3d7ae3db4a7f60f661e11ecd30`  
		Last Modified: Fri, 19 Jun 2026 02:23:21 GMT  
		Size: 5.2 MB (5227891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06d97c911fbef008414efa511e86ac9dbaa04f783c1dd6b27ccf170b2ac2571`  
		Last Modified: Fri, 19 Jun 2026 02:23:21 GMT  
		Size: 16.1 KB (16077 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c711758a48adfb2eb0585070dd8331c3c7ceef4e7e5cf112edac1be98a9d334e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201878583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20880e87f03fa784ec2e48859f191db20da79d7ce34510726c6246fc7a8ee5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:16:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:16:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:16:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:16:36 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:16:37 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 03:02:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 03:02:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 03:02:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 03:02:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 03:02:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39924b9a0b3b71c629e701ebc624d301c203a2ae6fb0c2d988f2e31cf6d3001a`  
		Last Modified: Wed, 17 Jun 2026 00:19:51 GMT  
		Size: 93.9 MB (93902069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a6ed340e4fc70f02718bd867038b064b0c3bdacc11d3fb966bae3e38848c3b`  
		Last Modified: Fri, 19 Jun 2026 03:02:47 GMT  
		Size: 74.4 MB (74369133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ad7c0e8d86d71b69358bb07728882a89770165381a85e40c78e72f8d7ec6ed`  
		Last Modified: Fri, 19 Jun 2026 03:02:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b3b3478c3bcdebc007036e9d189e749f127058c24bdb7c0d8b27f7f7e183e9`  
		Last Modified: Fri, 19 Jun 2026 03:02:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e71f259bd5fea3035b6ab909fbc784cc1c07c3303d5dd6b42d3dcfc5d7971bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5226446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344eb6ea6c486b97d750092645175da84042722131dca30ae7c25b05c71a688f`

```dockerfile
```

-	Layers:
	-	`sha256:d7a2cf4b571adcec890c85925ec5fe46388ac7043460a19b50d09c3eee77bc94`  
		Last Modified: Fri, 19 Jun 2026 03:02:45 GMT  
		Size: 5.2 MB (5210440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22dce63fd1b4218a0487174097ed8a4846e14a9e4b536fdc1fffbb1974c4017f`  
		Last Modified: Fri, 19 Jun 2026 03:02:45 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f538f618123bd449a13cb25ecc7070533506057905b62c95087d369938a92697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190321796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff78d8f5a8578b0a7a6183b0efed541c9efc8562425954360522c499b6937d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:24:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:24:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:24:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:24:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:24:51 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:25:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:25:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:25:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:25:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:25:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e62863f185d31fcd2b4ca8a5cf77ae353a3a8db1bffa4a8fc225e26af242803`  
		Last Modified: Fri, 19 Jun 2026 02:25:36 GMT  
		Size: 90.5 MB (90536966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484c81984f3db045fdb8ea8bbefc6bdb46f347fbced7eac1f83f6ece02be8889`  
		Last Modified: Fri, 19 Jun 2026 02:25:35 GMT  
		Size: 69.9 MB (69932436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be784d15277f4f9c93ef5d011804b2d5221b7a37e967ff8935e52911c7d768d6`  
		Last Modified: Fri, 19 Jun 2026 02:25:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee5ef677075b2a5f15a9030bb5e49374e4936319c9c36623c647133c89ff423`  
		Last Modified: Fri, 19 Jun 2026 02:25:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:260e30b01ae0d767d16affba2ac4fb9e8b8d6101ed4f264e4f1054000598e6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c2537d32a307c830f63308e94c46d3967e4d784204294f6221e2936233c24`

```dockerfile
```

-	Layers:
	-	`sha256:d6cf88dc63b9aac9a805b81c4af3c5710c0e18eff5cc162afe3a3bf217b26157`  
		Last Modified: Fri, 19 Jun 2026 02:25:33 GMT  
		Size: 5.2 MB (5203243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3019b349b19c227e7d4022d0a7af5a049d49dba09e654ae327f8c2a023e506f`  
		Last Modified: Fri, 19 Jun 2026 02:25:33 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json
