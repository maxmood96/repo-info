## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:ef4f3f5cdbea9f2209ff96ea91d67d255f36769df531843dad02e9c921502ff7
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:61393822d87ca0d73c6ea8e32b69cab63cf1df6b4d8a14a40ea16923d713d2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255713670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e167b0151cc7827e60de1410de4038e19c6eea1254af0de819cee0429ba233c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5ac146aeea2f5168bfdabdfe8954ad7858c31eec8b86b405a9350cb3ed7150`  
		Last Modified: Thu, 02 Oct 2025 12:47:36 GMT  
		Size: 157.8 MB (157804820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7b30507e4f6501c7f8b51a2b95d0b33a1726ae49158db0f2eed5029bff470d`  
		Last Modified: Thu, 02 Oct 2025 09:00:19 GMT  
		Size: 69.7 MB (69679473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36af15e1aa9187047c0f22c5a1ef3bd3d52913f47d526ad1d8ce38194ae7a12b`  
		Last Modified: Thu, 02 Oct 2025 09:00:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cd8e1e8ea1b48c4266714b9d01b63fb6426812d9e1db12277b79811a097ab0`  
		Last Modified: Thu, 02 Oct 2025 09:00:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb1a2fa8d78e2deaeb049809d417f3733b8ea94a8132b7b232ec27dcdd4ba972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3326dde288c3292f0f91a27adabcbeb9dae07664c5e09390f995202c42cf365d`

```dockerfile
```

-	Layers:
	-	`sha256:b244ce3850591f2d4c54404cd57a998fd09b096a2ba672552399bf15ac025efe`  
		Last Modified: Thu, 02 Oct 2025 12:40:35 GMT  
		Size: 5.1 MB (5116490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c298a0eafc203e7f1d35925274e2b816ec11620b5231fa59ef916a92501fc0`  
		Last Modified: Thu, 02 Oct 2025 12:40:35 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:92a70d29c971b0ac418098adc7b9787fc91b632bf6d9e84fb912e1ef41e6830a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253744781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3669e66ff2997121adb33edb8f155953a408fa373c0b1870188cbaca131f5bd1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f9e6ab9b32d673081fe4746ee1c44d0184fea0b73f14aff5292b1b3b7e396f`  
		Last Modified: Thu, 02 Oct 2025 08:27:30 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a755ccc3dc84af040a6a67127d69f7e4c5589e050ef21870294366f52fdbef`  
		Last Modified: Thu, 02 Oct 2025 02:46:05 GMT  
		Size: 69.6 MB (69560408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353d9c52760328b581015edb05af82db8ed70232f5df8f759157c79145db17ad`  
		Last Modified: Thu, 02 Oct 2025 02:45:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82c36a189e65c7c2c7a21abc81693f051e7f65fb443dac9ce0ce69f48d668dc`  
		Last Modified: Thu, 02 Oct 2025 02:45:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:28ba9425e44457bc6b5cdbf8e11ec8ab44d67a76969b2b5611a848685fd5db0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c517307597779d7d46f6719b6602c76572e6894cfa9cb8f1041e388756575c03`

```dockerfile
```

-	Layers:
	-	`sha256:a4ce6b25cdfa8cd6c549c7e15ade15c62f61cb4f57141bc1e99d9fd1f2c1548f`  
		Last Modified: Thu, 02 Oct 2025 03:35:52 GMT  
		Size: 5.1 MB (5122251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7385cfb277b4583dcd9d9f51c3459223dbc0766dbce5266297c5ec12e97ca6fc`  
		Last Modified: Thu, 02 Oct 2025 03:35:53 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8107b4e92ea6af822d0ab5070cbdd673b994786b064fbcd309194bce991fec76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265546018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65024386148d76e3f54fb1a60dd2a32cf9f432b0b77ed53a9f4e2ee0a543a93a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece9d28cfea28a59a1ae7922bfe566b7cd35de790865bec66649b26725f225c0`  
		Last Modified: Thu, 02 Oct 2025 09:12:08 GMT  
		Size: 158.0 MB (157963456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3d76d1916c12966c5a69ae148c412f2fe36341aee9d85dd19b348eebb12e45`  
		Last Modified: Thu, 02 Oct 2025 09:23:09 GMT  
		Size: 75.5 MB (75512827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e68ecccf7fe959519f47dce2c1d6727666a26a240733297ad32160b2ba6d58`  
		Last Modified: Thu, 02 Oct 2025 09:22:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335450f099c69d8ff417bff3d607405c9fad58c247fd6d8371a585af74cc8257`  
		Last Modified: Thu, 02 Oct 2025 09:22:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ef788d287a777deb05ffc3cc11c2bedb43f9145dca611201b376a724a27edd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87e5888c843421ff9c2a16b479fceeba756769cbb062753b7de6f4a573c9d49`

```dockerfile
```

-	Layers:
	-	`sha256:94c2c155afd12514c6bf2fdc88f05959fd41d927ab49de1c5a2eb1edaf3ec422`  
		Last Modified: Thu, 02 Oct 2025 12:40:43 GMT  
		Size: 5.1 MB (5121648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666b05a0ceb301f1f3dc262c93db7fbd0573a33891ad56582889597776d0157c`  
		Last Modified: Thu, 02 Oct 2025 12:40:44 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:53e448d4df73c70881555225b2a797c22f669dfcafea9549a24a07a99dfb0f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242402848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23c86220730fc46963a7ec1dd443765b459eff8e23ed3a4cd2b78588f484709`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46457b106c194ce8339355f24794bcd8460518fdebce246c268c0e44097291ed`  
		Last Modified: Thu, 02 Oct 2025 04:43:08 GMT  
		Size: 147.0 MB (147027015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de30b5f8681c2689e5b35d6e22ea6d37b006f573d2e215b9fd76c58ed8908df7`  
		Last Modified: Thu, 02 Oct 2025 04:49:02 GMT  
		Size: 68.5 MB (68490476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fa1ad859fcccfc3fea432dda053a41d2c332386a5d08e058814a557dc2086e`  
		Last Modified: Thu, 02 Oct 2025 04:48:55 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2713c00a22f2e7a369857e7ffc26afaa0c67ff2e1e8e3bfc37f25d0decd4dd8`  
		Last Modified: Thu, 02 Oct 2025 04:48:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bee7011aa3f97477de9ecf79928973e835b9db899c72b60758365ba541a02820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2738644300af791a6a7623c9ef64ec8548774e06faf43a3446f03c4ae3e61f41`

```dockerfile
```

-	Layers:
	-	`sha256:e6f8f851b3445fedbff82316adfe3f94e3e41b6ddeda3c062abff2fe32f86dd8`  
		Last Modified: Thu, 02 Oct 2025 06:42:47 GMT  
		Size: 5.1 MB (5107811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e8b6c724ecbe865205d7e752f09fdf4f2bf23cda9296adb86628e0a67b240d`  
		Last Modified: Thu, 02 Oct 2025 06:42:48 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json
