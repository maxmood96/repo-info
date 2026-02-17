## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:e64d3b3373817dba6da8f26522a2a61f3a1ce1fd7ebd7c653adf002773ea203c
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eca4073952a162cc8c0854d133ac3c86d8b83e25fde55e3e4435bd6a6b3684b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247404172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db97e9065a09ae2bb2b0b10ee56d06292c1b4114d26260a54779524900a788f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:43:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:40 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:40 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08d0405204991a3f11dd753f39f088586fc820997f0ecfbecccb800fcb7780e`  
		Last Modified: Tue, 17 Feb 2026 21:44:18 GMT  
		Size: 145.6 MB (145628753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeaaefad6ea62a3bc928497fb42c0c1b418ea1248c7342aa1061f58ab30b7bf`  
		Last Modified: Tue, 17 Feb 2026 21:44:17 GMT  
		Size: 72.0 MB (71995779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df45c34025c31213c1fd0f1d9d2ba9e5cc708b5ae89054119fbad87d1e35b3e`  
		Last Modified: Tue, 17 Feb 2026 21:44:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7912e6f4de8327a15c30b130811b187b8896e0d4699e25df95b072fb1564031e`  
		Last Modified: Tue, 17 Feb 2026 21:44:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:68eeac78626d70da0325c8d8b120df9399969a134deae7bf054ea068fafacf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc1584f3e9f22034843d48e9b0fa3625aee1c42aee8c5260f6e6753f2c1254e`

```dockerfile
```

-	Layers:
	-	`sha256:ba465665f3f4de3a7abc812075be891c905f7f947d401c130fdf39d3f9b43da3`  
		Last Modified: Tue, 17 Feb 2026 21:44:14 GMT  
		Size: 5.3 MB (5257551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8c1d73f9758231aac23d3e16d5ba5ff04b8aa306518ac1d7ce605aa9568c29`  
		Last Modified: Tue, 17 Feb 2026 21:44:14 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d51e2634db9204ec7d638fdb822533e181cf7717451ba84e751bc6342cdb0627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246383843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddf35cd405046beec53efe0c132b68299a4c7819497a9c7dd7156f30c51ebde`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:43:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:25 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a726ba3df80aea93c8bd5990146a1b171b6ddd496fa43ff4667bb4ffcda3dc1`  
		Last Modified: Tue, 17 Feb 2026 21:44:06 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc06d58b45acedaad7d0a38b94665e82df313e3766259e5eaa856fe27a64ad6`  
		Last Modified: Tue, 17 Feb 2026 21:44:04 GMT  
		Size: 71.8 MB (71806492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8828b987e45d941e01eceeb1e47a6d666834ed685399ce791cf4993319b2d147`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcdbca345874aea7d90148ccd0fb417924533271e4ad3ef571dbe1a156ad5c1`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c3e54ac4f233724ba3a397dcfa0290952e03b2ea3768924172a56091af8ca4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064e3b1583cc7e7ba27ad4296f0a6c1eaed35024d0dda9917b91cdab8ca83078`

```dockerfile
```

-	Layers:
	-	`sha256:273f0b85587fcc83d825a2ed7882cfb38ba11d743e67f4d62a2666433f438372`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 5.3 MB (5263320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f60b3db2e94da9f8be449cad6b8d3ace6e7331dc6b1a6e7a6dcdc7d7bdb3c60`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:abbfe06c54dff10a51b0408096100e1b55a21b75e73ef4a9029caca3b19b29b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256429881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd864fe5696f713f00fbedf9bbbf8ff25f08adc1f01af4bd6127ac7121fc97e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:25:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:25:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:25:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:25:39 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:32:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:32:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:32:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:32:52 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:32:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806148462c30ed1bfef62eebe515a501af99978464a4710c612e54794c9190dc`  
		Last Modified: Fri, 06 Feb 2026 00:27:41 GMT  
		Size: 145.4 MB (145438280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98487951ac4bc2c715fb3a90afb8dbce0526938a979bfe906080c5e2a7c2ce6f`  
		Last Modified: Fri, 06 Feb 2026 00:33:39 GMT  
		Size: 77.4 MB (77390376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f7a4bc63242979f9837e5153c2b2b2112983b766e97692e975dbe8f1d5968`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6630d7a0a5063957f0e08aa33a2c9dbd548d96f7234b4038196cb67b7dd7a5`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0403b2bfc3017739928e66efc4ce0974710483d03e49fe6f4f63007d24c09264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0da7de586c452dc3481a242975843f28557e3c9281d9cdb2236191b8315bea8`

```dockerfile
```

-	Layers:
	-	`sha256:11d8eb5c57b5ec8c3cdcf61a58cb356801212571a6cbfee92710469877a6d611`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 5.3 MB (5261922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:887b1e053490263de49f4a511bd53a2cfa9fe4a9291c07373209502e8f727722`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:d1cd417db107dc293c6e5b34d8702864d088a6197ab7754c03fa71a175c44256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241819828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282df457eb6469bc1e26d2663751784a8597e6a43e0b6289a455ea63f308bf6c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 11:42:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 11:42:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 11:42:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 11:42:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Mon, 09 Feb 2026 11:42:05 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 12:05:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Feb 2026 12:05:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Feb 2026 12:05:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 12:05:19 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 12:05:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9392be11579f1db561dbc39d809f5cd0745e52295280784399207c85300c2b0d`  
		Last Modified: Mon, 09 Feb 2026 11:47:49 GMT  
		Size: 142.7 MB (142662977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103f0c02cd2b311b9bbefc0b731c9cdebf532e80eb54977f49fb9eee4038d659`  
		Last Modified: Mon, 09 Feb 2026 12:09:03 GMT  
		Size: 70.9 MB (70879415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccc656f21790e6ae7c73fbb6abe0e15884f2464767aa779c0289b62388a7670`  
		Last Modified: Mon, 09 Feb 2026 12:08:52 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770aebabb8a0981d394797cfbe45c4d8de7ad88298a1a0feb81fcea4348dbde5`  
		Last Modified: Mon, 09 Feb 2026 12:08:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f471a5378ce2cca596fbb52127a7c412af2002aab30cc163a0530ddbbdffcbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5260956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2a63a5d2fb10cda2955be0920f247986863aa7b1b79c216b2359c143fffb46`

```dockerfile
```

-	Layers:
	-	`sha256:ef10db932145c80382dd3d665a2e7b8a298330ef42f9a407d313b9e1e99b6997`  
		Last Modified: Mon, 09 Feb 2026 12:08:52 GMT  
		Size: 5.2 MB (5245096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c380843e37c0fddd289f1f52b706a11216e46ce5fd76de800db4db5da64c6b`  
		Last Modified: Mon, 09 Feb 2026 12:08:51 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7692eb18132417fb28230302ba322532fadc884c2153ddb4bf3b7e5a783125c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238419110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c746db211ad7253f780ae293a051c8026a83a255062306b2985bf19e6d13996`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:04:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:57 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d9217a8722bf1575b25697aa59ca55388f0c47c3f649322398b3a70f4c8b2`  
		Last Modified: Thu, 05 Feb 2026 23:05:43 GMT  
		Size: 135.6 MB (135627061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4765376ecab37b294d36bdce3d93f6ef82961601992da4ccbb47b86b25d0ef6b`  
		Last Modified: Thu, 05 Feb 2026 23:05:42 GMT  
		Size: 73.0 MB (72952859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4c25a224c6cdc1aac75995b7e148a598a90ddec972a33dca2387be3e53c77d`  
		Last Modified: Thu, 05 Feb 2026 23:05:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244d56e5b19a2fb77c5ca62a097f06c9e4ca5ad0befb9eb9b3d1fbd81cfb4df7`  
		Last Modified: Thu, 05 Feb 2026 23:05:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f6dd0d9811066ac04c92ab158be8309c617370cb15d1d68c2a534e3cb59d227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36a796a25eadfde5d645f70ec6b0aaa09dae4a418c24f00d4f41f66f046af25`

```dockerfile
```

-	Layers:
	-	`sha256:6c5b31fceff859497866c28af84dfc1661068c826d30fef478961d5765741caa`  
		Last Modified: Thu, 05 Feb 2026 23:05:40 GMT  
		Size: 5.3 MB (5253475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6b525721c32a202800dceac60fdbee5c0b98b688821ac1f32c5fcd5e040e75`  
		Last Modified: Thu, 05 Feb 2026 23:05:40 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
