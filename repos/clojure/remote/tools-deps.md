## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:cdbbf5bbfd2a686823f5ef1c19119c2968aff569b98a4a04b7bbdb0ed170ca57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:9b3a1def5b4db60d9a099a8f7fb5aef89b408f3d65cd4418d498fe5635fab31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289426641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dc1bbd614cdaef34b9652dbaf11dd1a03c42a5bba84b2255cf34196bf0980e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f034b0308d1e2fe51ace71e3e8ca8c3405b6eec9b23977b3d1d67c7262803a`  
		Last Modified: Wed, 23 Apr 2025 17:16:31 GMT  
		Size: 157.6 MB (157634413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6781ff396fa0bcaab8713a7f7f6521eaa7c23a9879bdea0875b61b80b93186`  
		Last Modified: Wed, 23 Apr 2025 17:16:29 GMT  
		Size: 83.3 MB (83300644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdff747b602360819cd96f854a0b62a7739ba1509e8a42d705f37dd3a9a8cbe`  
		Last Modified: Wed, 23 Apr 2025 17:16:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc9ae7e5acfcabed101ca3424d89eb767b43e1eedccb521ec7f726e9bddbb2d`  
		Last Modified: Wed, 23 Apr 2025 17:16:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:35ee3b357fec6cc1b03b4f41926396e5f5a802b021fbbd879d90a8b2b344bd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7195399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf406e8ba845d79d6e2eacb92f29f3546b2ee62727955aec5810c97ed14cd6c`

```dockerfile
```

-	Layers:
	-	`sha256:c430d6aa10d2eb2c8783822c256c5cf1e963856fccc895820950b8cbaef2929d`  
		Last Modified: Wed, 23 Apr 2025 17:16:28 GMT  
		Size: 7.2 MB (7177578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:031f87c190ce92756a05f7c7f883c55f96fab927b32c31ec1b89ca6e2c6c2ff3`  
		Last Modified: Wed, 23 Apr 2025 17:16:28 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd3607b576fb7d0e52617d2235bd7aa35f180f28c225d101c718d9f0222601d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285030400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff22fca85d3e00ec045294f257c95a6a516cbbd269485787050b8f2aabe6c23a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c9d1eca0c6f0c11c056bd1a9c0a6fc6af61a9d35f24ad12f42bc4153e746a6`  
		Last Modified: Wed, 09 Apr 2025 17:10:48 GMT  
		Size: 155.9 MB (155859270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab30a8b70d2528ca3c9743bf543a60c16c375e3858f2a11045770d1021e5076`  
		Last Modified: Wed, 09 Apr 2025 17:43:05 GMT  
		Size: 80.8 MB (80842617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b8e0dbdd1044cce5c303c39ca20ad68b0e09e05515ce5fb4f13987716d914`  
		Last Modified: Wed, 09 Apr 2025 17:43:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725f2329e1af2567a1b2753668ce06de2a9de3987e31aa8825c38f42e7ff441e`  
		Last Modified: Wed, 09 Apr 2025 17:43:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:efa7f1f8a375a5cc33693df6af92d3c90f48c93109beb5dca68a5b12fa184254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b4c4d53747494f5a4accc9b81c1ffb0de0515c5fbc5f5f4261cd131babac98`

```dockerfile
```

-	Layers:
	-	`sha256:7185008c133eebab1f6034b26a49bf988e2f1e0488f2682670c2616c4a02561d`  
		Last Modified: Wed, 09 Apr 2025 17:43:03 GMT  
		Size: 7.2 MB (7183413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ee9239954eeed38e76914439647052f725a58e334e3a7a73a41f87b292f573`  
		Last Modified: Wed, 09 Apr 2025 17:43:02 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
