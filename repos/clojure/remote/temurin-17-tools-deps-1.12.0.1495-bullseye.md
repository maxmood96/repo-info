## `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:9029e072a3a4d9183e89594c7e91238d3bb320cba4dba589ae45b00bc9d2f12d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6644954f17ba1448d5d92d4739b6af3db7ef085aeeb9ce8f6603d192e54d05cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267455488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931bed186185795a593f85bcb66e0546624e4b54b95ee2e39fb2bfd008fea5a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8242f423d75ebf7f76848baef3eeece481a8be52508eaf61d0e6ad887cdea4ad`  
		Last Modified: Tue, 14 Jan 2025 02:44:25 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d624a5781f8a0f8570c1c49141ec1e5e944808a8aea403757f44e7a8520990`  
		Last Modified: Tue, 14 Jan 2025 02:44:26 GMT  
		Size: 69.2 MB (69178568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3d7f74309cf3a5d7eb685fe8c7511d53f1959d2800e6ce2184d94ca051500`  
		Last Modified: Tue, 14 Jan 2025 02:44:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747740e0b6ffda8c6b55f8c897a803238d5bb71e0ffd99895d956315aa82e575`  
		Last Modified: Tue, 14 Jan 2025 02:44:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9ee2328b138030c3e143dc9625f44c65f423e94a69496d55bb756ca86e625259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d779f393879a7fca7c8df9ef6a48f6618cb7db174ce372c6b2cda39b412d4393`

```dockerfile
```

-	Layers:
	-	`sha256:ce7ed1c13e907dde793fe054b5f1b82c49ff2697d13b67cbd2ceb75fbb558999`  
		Last Modified: Tue, 14 Jan 2025 02:44:24 GMT  
		Size: 7.2 MB (7204557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbfdd08afa1b79b4788da11d9b84bdcf68a10ab0b2805a74ec777955ec346196`  
		Last Modified: Tue, 14 Jan 2025 02:44:24 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a103a7d45f404e54074c51bd3b933b88a91f0b1929faa6f9c63cb86ae94e04ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264912195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61350bd5d4601b97b494644418da17d00b7fc4ac386bb9d9e36edd3a3aae2eab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dce462c22105422e138f6d754df187041f54e682066c38e939203fda7d53c73`  
		Last Modified: Wed, 25 Dec 2024 07:26:24 GMT  
		Size: 143.4 MB (143360983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f37e36813eb806137f72237dedf4c41060ef4eb6f261b3c0ac28ff992f17e0`  
		Last Modified: Tue, 07 Jan 2025 03:28:28 GMT  
		Size: 69.3 MB (69304472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c89e883012c075fdcb3fea7e6ca99a20201560220fa8167a996d67de756f489`  
		Last Modified: Tue, 07 Jan 2025 03:28:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d0e43d7f4889e2b0469023202ab310790fce520374a4c03a7e5747b92af65`  
		Last Modified: Tue, 07 Jan 2025 03:28:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:814b09ba400a040f3079eb898d304ac920eb84f8fe3a3613a48c633cd10fd7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c4af2bd9a51896d44115e90c058fe85c91d6c8f34fca1c87ace3c88271dc1c`

```dockerfile
```

-	Layers:
	-	`sha256:400503bc0a24f89c5148b96c4b0b90d9ed46b0345491cadbb6f7b6e14b3bc18f`  
		Last Modified: Tue, 07 Jan 2025 03:28:26 GMT  
		Size: 7.2 MB (7209656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab5813db75de4d975798276ad4ed4bd2cd6e8343b5ff70828e15529ff8211d1`  
		Last Modified: Tue, 07 Jan 2025 03:28:26 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
