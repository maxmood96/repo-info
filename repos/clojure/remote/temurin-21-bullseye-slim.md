## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:a29e98a78d25e537b1f044cc02bdd64666cf22b0126b662f5a34379dbfe7fc36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d93e837c75dccea456acfb92073388e8def1e1c67d9175d59c41616e6606042e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247216298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bf61564d632ec8f57e6c68d886145ebcb838cf1cb45d9b965dd4f97f33b0f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:31:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:31:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:31:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:31:56 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:59 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f657e8519b78b308cd685a5f2cfe22fe50dfeb44386f2628f961224f5e94f`  
		Last Modified: Tue, 04 Nov 2025 09:51:41 GMT  
		Size: 157.8 MB (157804776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7b7b44402d998021b603092b7381e3e55e703b2d917935cef5bd505a434fe9`  
		Last Modified: Tue, 04 Nov 2025 00:56:41 GMT  
		Size: 59.2 MB (59151885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714d97dbb13008199dc68b863ce39e5f4487cc7a9ad2ee5ae65d8af2a59bd5a`  
		Last Modified: Tue, 04 Nov 2025 00:56:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883e635c17fc43ba40f5f5a0acdaa4387bc0d0f426a6655cc501d51ef0b93753`  
		Last Modified: Tue, 04 Nov 2025 00:56:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8f5d8ef9f6d7e31eddce5396c43786dd0c9fde38a88ce90dea03889fd01d4e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5326204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95c73713e70b9cdf249d27127a90f8d58b4977e0eaca0128ea062093204c6a3`

```dockerfile
```

-	Layers:
	-	`sha256:c616b6b8ce1823c99726de3ccaf23f20c24312af6b551c055d22ea577897bdf6`  
		Last Modified: Tue, 04 Nov 2025 10:42:38 GMT  
		Size: 5.3 MB (5311169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cbc34cc6d0fbb946d036ae5b438b61afdd2bf2b0a4de489840587a2f988439`  
		Last Modified: Tue, 04 Nov 2025 10:42:39 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa10c5fa07a8506f11bb65f22d31ec7568b9e6bebb57274241a71fe33c22beba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244118502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecfffaae91361edae54ecf7368af581460d871fe17da99fcb6cdf4ad1a91d38`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:56:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:56:41 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ad124f34d3108f7b47dcbf18f92d2e0076ce9396b25527f7e6eb31fbcb3949`  
		Last Modified: Fri, 07 Nov 2025 14:55:26 GMT  
		Size: 156.1 MB (156081237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9e4b9c9f98c47e2227a20a42f0f3fca8eb35ebb4aadd7b12bb7791d6d291ce`  
		Last Modified: Tue, 04 Nov 2025 00:57:34 GMT  
		Size: 59.3 MB (59287674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af696e5adf92213b371cf37ddca8f67989274eb6da9a5c2ec33953c708207864`  
		Last Modified: Tue, 04 Nov 2025 00:57:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64abfc257ce7164e1f68a625d70cde8cd1aac04ba67179f0ff8e173e723f648b`  
		Last Modified: Tue, 04 Nov 2025 00:57:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2119009c5227ddee1042761d32465e16c2d2fdd02f542e9c1a488ac408d510e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92f36c42057322722d784f6f79ded0b3754eb61d1ab4df93e0b60533d4a1511`

```dockerfile
```

-	Layers:
	-	`sha256:926d9fa7ffeca86c681b3a7b7c5a523f06a96e8279a4914804e0f40d7a6c60fc`  
		Last Modified: Tue, 04 Nov 2025 10:44:25 GMT  
		Size: 5.3 MB (5316901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890b74ff394e7fdcb459660b625dfd10655e45267865778d0b3960fda69e087a`  
		Last Modified: Tue, 04 Nov 2025 10:44:25 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
