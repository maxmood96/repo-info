## `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:b4cf1278cd304d97e2140dbd88ac300d8d2cc262325596552e2c95d6bb25fabd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0840afabeee3ee4adec269dacd4d407aebd81e2899020578bca6af1223649f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247612385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161b5ddae866f64607e594b3f44fe7f215e09860ce92917c0e5acf779203be1f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:16:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:16:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:16:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:16:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:09 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346cffc81ac8de2d231cccbf762d4d5a4b24efbc1957e59e948d8ae324e69be1`  
		Last Modified: Fri, 08 May 2026 00:17:01 GMT  
		Size: 158.2 MB (158166935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4ec2bf9b8bb04ab80b446ea4c52bb183df69d9e980c54600b6da2f01b7a348`  
		Last Modified: Fri, 08 May 2026 00:27:39 GMT  
		Size: 59.2 MB (59186476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f791d87902930fd1486ea1f7677a1b1f5cc82a0d4b2b1aaefccd753c623f91d6`  
		Last Modified: Fri, 08 May 2026 00:27:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af193585d95651499aa3f1d5e76393785cb9c73f2fcca54db482582758b8e9f9`  
		Last Modified: Fri, 08 May 2026 00:27:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d4da4b6878d15acd3db64c24b5e851323614d51808bd39795e39002991434646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5219cc7636f7055d7a9cd91aae582a015673bd7e7b982e9902efa8ebdad53b`

```dockerfile
```

-	Layers:
	-	`sha256:310621411f8d7eb57419a9288de2ed2a8a5ecabf7d8e5aec60a027cd4790233c`  
		Last Modified: Fri, 08 May 2026 00:27:38 GMT  
		Size: 5.3 MB (5322532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e8b9f3743b8307db34412bb79d72a183c9c4c661f9be05054b3d42bbf7230e`  
		Last Modified: Fri, 08 May 2026 00:27:37 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c5a48c5627010ac472bc8c27fdb2ee78ef3dc4597c77aa37947ee3869a39fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244535915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92733cd28410225c2c73c0b579f4e2d9b85c1f9edfe6d8a41ad013a42f2e626`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:26:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:39 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:26:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:26:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf2f299b35f3aa2555348553f122da909630c304c4c6f7eee6c731cb2b93bca`  
		Last Modified: Fri, 08 May 2026 00:27:19 GMT  
		Size: 156.5 MB (156461247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151fa76a2dc6cc61e37ddead7e0e81cfa7228519350a077dae01c7ccb177794`  
		Last Modified: Fri, 08 May 2026 00:27:18 GMT  
		Size: 59.3 MB (59331115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be3f74f84b4423b61d05371dd77b51bbb11a5a5efda0e4081d191ebdac5ac`  
		Last Modified: Fri, 08 May 2026 00:27:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a06c36066fe15fb911b0cfc08adf2a3febdf0c77d3b9d342b29dd7c2046bc0c`  
		Last Modified: Fri, 08 May 2026 00:27:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d894d1a5b7ecc6d305db41b4386652e30160ce2ce58d99c3dd411870d7234193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5344372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eba352581c89975cf3e4297ad624f8eff0ce779677d041d623518d0e4c55bd`

```dockerfile
```

-	Layers:
	-	`sha256:37fc55a401df54821b3c4b33fe60f535ea402130b7be8401c245a4cdfd40feac`  
		Last Modified: Fri, 08 May 2026 00:27:15 GMT  
		Size: 5.3 MB (5328264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b7361363723c7efc5a23f69fb5299d038c896d48f656ef31c9896ffba6d52f`  
		Last Modified: Fri, 08 May 2026 00:27:14 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
