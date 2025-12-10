## `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:ec725eeb66ceb6e4b63fe8ee14f12cd36217e793cb75f613cdcb60d267e49e29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:28d8f0a1a1a9876fa35faf9594bf9500206280fde54575e581cfb053a3032cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152641923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae1723831c062eaa493c4fc3c9b13965b17da22ffe4b7a0f81ff8045692fd4e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:50:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:50:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:50:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:50:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:50:01 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:50:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:50:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:50:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc64fb9e4c8904524c0e6a81dfdfc06c1bb180140216432296eea166c5df800`  
		Last Modified: Mon, 08 Dec 2025 23:50:42 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4695450708192c76b7d15b0f85019ba337b45fd3e253265d2f614bb8ee6cc304`  
		Last Modified: Mon, 08 Dec 2025 23:50:46 GMT  
		Size: 69.7 MB (69679492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c831e2d64b846512c26c9bd85a7937ac11d307c95f25a0aeeb4c6c77775379f5`  
		Last Modified: Mon, 08 Dec 2025 23:50:37 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29a666c60aa3f0f82a826cb1eee7023fa07e89e0fd7cee1557fc064ede4659ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3793cb8ddd6708206a2a499a996cabd27b3a9b5334cd34ebcb9db5a64724286`

```dockerfile
```

-	Layers:
	-	`sha256:cbe2e894016e216e279177cd1202e54efd6f90788a7ecabaf8e3b1ba010c6228`  
		Last Modified: Tue, 09 Dec 2025 04:47:54 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a229d1cfae9234dd81487cf629302b98a35df9aeb84416b2863f5f8bf7cff6d`  
		Last Modified: Tue, 09 Dec 2025 04:47:54 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:554a40bad6a73ad972acc44feb45cb1e8c34ab9ee8e5f2da2ffeb544bfdb32d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151478406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f04f2db495c6ad058b8879d975988623e3bc4c06f4c988fe91eb5453c3a309c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:57:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:57:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:57:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:57:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:57:43 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:57:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:57:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274cedd3e61efbe7cfffcbe266c78293280b4bcd0b4800762283a9d60f55ec3d`  
		Last Modified: Mon, 08 Dec 2025 23:58:25 GMT  
		Size: 53.8 MB (53814983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5f10da43c2ddc6e268cfa96312ecec0a76269ba3f66f82ed2cb42411c937e5`  
		Last Modified: Mon, 08 Dec 2025 23:58:26 GMT  
		Size: 69.6 MB (69560547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad92ca50e94c36ea9dc311d7b46b64525ea07d649c60de1c423421c2c01699f6`  
		Last Modified: Mon, 08 Dec 2025 23:58:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:030274a16f93ddfb3b8a1247c9867a0b28b391056fb6f64f8a9312235c91ac47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bab67628e3ff30642ff58c1fa8a8e6f4f4f293329b2672bd3e903925840576`

```dockerfile
```

-	Layers:
	-	`sha256:fa2001df006173cca3fcc453ffe028c9cafa28b0399d1b5af4888370074187ac`  
		Last Modified: Tue, 09 Dec 2025 04:48:01 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897798c197d720ab6c71b2b5a4529d59657449e2f79da8282ab5d7ad8ea83924`  
		Last Modified: Tue, 09 Dec 2025 04:48:01 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:76166ff557c38d1c940d946248f1bcd137ae5f4ed9701d740fcc950ad28c254a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159758481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c96d9d5cc2c5bf6201640067b66b80d478efe9250ac73a0106076c44b98c772`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:15:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:15:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:15:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:15:13 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 16:15:15 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 16:18:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 16:18:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 16:18:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f64fb487d3e6808b902444ad63dfe41ea36c5a144cddfa20a3772f42fbf0c63`  
		Last Modified: Tue, 09 Dec 2025 16:16:47 GMT  
		Size: 52.2 MB (52175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44609dd9eacf91495858411db4b263dfedf776b97bbb2fb7715d3d09e4b0109`  
		Last Modified: Tue, 09 Dec 2025 16:19:13 GMT  
		Size: 75.5 MB (75513830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d70c900fda931793372f028dcd47ad7d9079b56e02d7c368b2a20b820bce856`  
		Last Modified: Tue, 09 Dec 2025 16:19:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3771a90f278dce17452d5975981ea2b76eb5f6008fda0499192817bc73d3e673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897ca7174987cfc7e9f6bfcf1c8765e22ddcdd567b48f6b8bdd551c7ff18614b`

```dockerfile
```

-	Layers:
	-	`sha256:83984d5f52b1b0d37649f9642eb5851bbcf95f7e0fb3c1cff9ec9fa3c9467f36`  
		Last Modified: Tue, 09 Dec 2025 19:38:05 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a56b77b185aeda7ccadb8681b80fceb0240c1716c125cb83fc22a0e619797f65`  
		Last Modified: Tue, 09 Dec 2025 19:38:05 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
