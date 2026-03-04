## `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim`

```console
$ docker pull clojure@sha256:35899e18be8a6e10b31b5f27522d5463eb648b936534dbd6f9e05768f028a54f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:04ffeec876c98c8ac21ffdb3cbec169cf3b76c0159a33c8caad8e6dd9b27ee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259644485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83ff581c8f6defe1e8bf8bfabb197177a5383927e46ef8d6e239798704574e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:47:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:51 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:51 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:06 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3c550653d924df5e26a0284a7fa0aad0900b8c813fbd8748391ae52816b25e`  
		Last Modified: Mon, 02 Mar 2026 19:48:27 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36d065e2f6294761c32081066374b40e2a29df18fa293a0bf5a46b86e0eadf2`  
		Last Modified: Mon, 02 Mar 2026 19:48:26 GMT  
		Size: 72.0 MB (72007711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a570d92367266b52148c00b42325b5b5300255733e941c3cb96c21dea8c118bd`  
		Last Modified: Mon, 02 Mar 2026 19:48:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fe7b6a1a307d208228a977064efe46b1bc31b7bca56709db79ccd5dfb2e209`  
		Last Modified: Mon, 02 Mar 2026 19:48:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59650386806de2dbadcc2e37d4715ccc33bd68fb958f2db03c01dab0a506b4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c575dea55d4e19d1d386e1cbbe170d46b89267f2741fd9a933a6dec1be1507`

```dockerfile
```

-	Layers:
	-	`sha256:b620f80c88467b7af8477215f8aae94f21e9070676a19ee038812b034905f076`  
		Last Modified: Mon, 02 Mar 2026 19:48:23 GMT  
		Size: 5.3 MB (5260916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1849dcc5ec1da62186e2c59c88c9543d2a97c3dbf478a4c51addaae63251a1`  
		Last Modified: Mon, 02 Mar 2026 19:48:22 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c327159f65ba733ac5fa6f4da23716e61c5331d10dee6149418d1a25b9325979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258098121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342a576617e0aa66b1a0218a0dc5e9edf9fcda4c05c21f7efa968f77db12fb9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:48:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:01 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:01 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:19 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c1f6d6f40afb79fe778de93333d6c438057b943b1bf3c7037438ceeca1a978`  
		Last Modified: Mon, 02 Mar 2026 19:48:42 GMT  
		Size: 156.1 MB (156133064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff6b03dd61ce4425f1a5a12e58c640182f874d2ffaf0db335e4fbcfb851d8e6`  
		Last Modified: Mon, 02 Mar 2026 19:48:41 GMT  
		Size: 71.8 MB (71823914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da68fb7099b4fbc16ddb55491f4eac60397c1b2e5ebe1b23c6f5bafe07301d3`  
		Last Modified: Mon, 02 Mar 2026 19:48:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830fcd5d9b4d3f8577ea83bcc07833628f9a7ec24208896d082b94b7ffa97da2`  
		Last Modified: Mon, 02 Mar 2026 19:48:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:777e09dbe3a231ea511f9a29aa4ef85f796c1c66f8939dc236bd2af16546dacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf6b717def26ffa415bff5f3373516816223536929c7354d260009950236435`

```dockerfile
```

-	Layers:
	-	`sha256:0ac44f29c9da78c6cb1233e4af4a26ec018402a7a5d82f1c1460fa8e902d8ed4`  
		Last Modified: Mon, 02 Mar 2026 19:48:38 GMT  
		Size: 5.3 MB (5266685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac315acc97386de8252cd4aca5f29c50d99f7ae6c8c0152ca82f745fb5b48743`  
		Last Modified: Mon, 02 Mar 2026 19:48:38 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:76567d79b8238b7599153a4b65be347c93e52f6e9b148f7239d7b1176b3a4c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268998140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d1d8b932cf0e8441a55255c87a7b621bdb8c318a6efeb5c02bdb325468df52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 20:05:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 20:05:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 20:05:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 20:05:38 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 20:05:38 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 20:06:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 20:06:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 20:06:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 20:06:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 20:06:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7d91e4e50375aa80770d72215d7ba7e3fc2b6b59ee7f7cca06c8c63ba5edef`  
		Last Modified: Mon, 02 Mar 2026 20:07:37 GMT  
		Size: 158.0 MB (157977504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af08f40bc987b3c8dfe33706f0d5771a6dcd6496d56d0b00be4a7dd7304d095a`  
		Last Modified: Mon, 02 Mar 2026 20:07:35 GMT  
		Size: 77.4 MB (77419377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f603b0672392034d1208545873477f09358f9a19bf3802c08870dbc57b68396`  
		Last Modified: Mon, 02 Mar 2026 20:07:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9551db34dcb39e360f1ece04412d4807c4b3172fc531cd93394b446688e7ca5c`  
		Last Modified: Mon, 02 Mar 2026 20:07:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a2862fd7fc1dd3b2e3b2c4c87f309da26738c410177ae1274c69480f056a3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082ba81fbab7d81c1624fc4e6afe8f1150948e20008db04a37539bcdb1d45c26`

```dockerfile
```

-	Layers:
	-	`sha256:3fd9edb7b5a965acf7cd75746ca36af0bdf195623afb5e5715bb15413a9d9392`  
		Last Modified: Mon, 02 Mar 2026 20:07:32 GMT  
		Size: 5.3 MB (5265287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53878b2368b73d4d93430223b9d4dc7a63914e18dc5d6834ebf3ba2d07c3b938`  
		Last Modified: Mon, 02 Mar 2026 20:07:31 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:8c6181b8b4c0c64b3e06d9c4e847060b2c32f2e91a67da9e9c91ba480c42ace0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256388401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc47af090bda1fd404b852225616f9abf95b8a9ef399365261d122d465dcfba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:23:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:23:46 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Wed, 04 Mar 2026 11:23:47 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 11:26:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 11:26:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 11:26:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 11:26:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 11:26:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6f2d4c20cb87ce38553ebd9ee153c1d2ba4124eefd89d1277f7fcbaccfbfa3`  
		Last Modified: Wed, 04 Mar 2026 11:31:31 GMT  
		Size: 157.2 MB (157216904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad88cb8b1373f7463a804959d475aa7ecf8a969ba6cfd3c519094ff9b12a011`  
		Last Modified: Wed, 04 Mar 2026 11:31:18 GMT  
		Size: 70.9 MB (70894038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d93039c3954c23198de3b33f7983ed3a3361732414cdf91f6128fddf293e52`  
		Last Modified: Wed, 04 Mar 2026 11:30:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d16d63915d7072749c4d610cd21eb6a76425d3677e36c7805998b160b67a6e7`  
		Last Modified: Wed, 04 Mar 2026 11:30:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ea9156e49e9227ccb7e2cab56ca179911b8da88f9fa652e80b5bf7150f8c78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a9c4ac64cf16494c849691975d37adba627fd261cf1a7b5069a3fbae6cdb6e`

```dockerfile
```

-	Layers:
	-	`sha256:e6ab3410c54853b4ffd37ade106d235d87fd9914ba6790076b93e00dea9ec42c`  
		Last Modified: Wed, 04 Mar 2026 11:30:59 GMT  
		Size: 5.3 MB (5250380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2b634da91e1a6aea02af4911a8cc9afdf955ba3507c64b90083e5f31bb1796`  
		Last Modified: Wed, 04 Mar 2026 11:30:56 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:319f40e9d1beadf676bce83946e5d51ed5d796a1e719bfedf251c211af113bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249916441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb4272d23369bf8c3b6258444216943c2b6c089ec90d86a853808c3e834e1be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:48:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:19 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:19 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:35 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbb0c0eb80bdda9322aba40c7a1860c3bb40fa898fc73b90cede02adc28d4ce`  
		Last Modified: Mon, 02 Mar 2026 19:49:07 GMT  
		Size: 147.1 MB (147105249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327c6c2e046b1d7e6ba5ada2a985e2b7f0bae7aa6a9ec276718b18c3a740c435`  
		Last Modified: Mon, 02 Mar 2026 19:49:06 GMT  
		Size: 73.0 MB (72971972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a398751272bfc319ee5736fd8af3aa7776f10b750ac874e7688e3c03ab655`  
		Last Modified: Mon, 02 Mar 2026 19:49:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dace63eb657576c91bb239798756221d29318961ff71fa505dbd2ed174c7fbfb`  
		Last Modified: Mon, 02 Mar 2026 19:49:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b367587871eecd2c16e7624c537fcd17ca141e914bd302c41df510e53ee1b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b19b82faa8d641be926f0ff0b04ece56af523804670ea47a30869ac9e7cb555`

```dockerfile
```

-	Layers:
	-	`sha256:23a6fc33d9fe9c0e3f837b0bb6c6cce473a4a2e1c38bf5a162d983ed5c15add1`  
		Last Modified: Mon, 02 Mar 2026 19:49:04 GMT  
		Size: 5.3 MB (5256840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f5ec7979819f1f2ee3556da4309938a47320fd421a29f389f32808662cb014`  
		Last Modified: Mon, 02 Mar 2026 19:49:04 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
