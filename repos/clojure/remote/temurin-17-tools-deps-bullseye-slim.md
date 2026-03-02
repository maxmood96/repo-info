## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:7424c0e57f6fa1ff54a6a3698dbf0d015c1dc45ee7ebb374934747025cc017a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7817cbc230daff4ee607c7aedbefe8f9652f103ad3f6d285f03a20d4626c2e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235064848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a6c0d0e1995e8128c9caeb3d563723dd0312e86a163357dd87d6785046e944`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:46:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:49 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:49 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:02 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a3631da109e9957a95ce21c6124e202ef7f857ccc599603724b4ff745db39d`  
		Last Modified: Mon, 02 Mar 2026 19:47:23 GMT  
		Size: 145.6 MB (145628702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7bebab21c6f1747e54e56ee9cea874430b44320bdbcee0f37b63ce9aadc74c`  
		Last Modified: Mon, 02 Mar 2026 19:47:21 GMT  
		Size: 59.2 MB (59176723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37517531070b003b95327dfa350b583c775aaece9b98e5f58402f3deb142b5c3`  
		Last Modified: Mon, 02 Mar 2026 19:47:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8851cb696aef84bf921893acd7b94c6d64fe0972fd2f317ec54958d6bc048d`  
		Last Modified: Mon, 02 Mar 2026 19:47:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e482bb6eba4e869a39681b807bdbe2c63a8be32340419f5fbd8746325ded8dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115746ebb0ec6f3cdefd225a79e543c23e2815699611cfb49ec05b2da74974db`

```dockerfile
```

-	Layers:
	-	`sha256:768af0b6489a42103346b664545424064c2640927b70a80ee0485e8a74d17470`  
		Last Modified: Mon, 02 Mar 2026 19:47:18 GMT  
		Size: 5.3 MB (5321677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d40c9b72dcbf256ee80bac27b582b6c5e2a17b37a88f685937005d3a75cb990`  
		Last Modified: Mon, 02 Mar 2026 19:47:18 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:67624fb2f02d0ef7fc5ede8bd8313c79b8af2b168dfae7331a1524b2db57c72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232498817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90a7f76a2c8269a229a6313bca6b4203b9f97e03365910434104e8c8f359d60`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:46:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:40 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:40 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b282b4af16fffe835bac35c6df0f6d2f6924c1182e3b837ed3c140286cb9e1da`  
		Last Modified: Mon, 02 Mar 2026 19:47:18 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e920893fb6b744b64581a635c371f5be0ed78a89fa412d441f34a594d0b2aa4`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 59.3 MB (59317107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d710d0afb5965c0c63a4cbc6da2f24d48afec93d53e7cc74d6e5b572492f6b31`  
		Last Modified: Mon, 02 Mar 2026 19:47:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2abebdd1d304e77f1dc900412c64bac6889fcbb15efc007e0d9ee46f410502`  
		Last Modified: Mon, 02 Mar 2026 19:47:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0e39b406d37cfc0cdf39b3da0e16eccafcc271464b6523a747f326d5005a3861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d8cefc98c5044e654c88e14aa900e96fddeda1290077b7e2ed313ec170cb14`

```dockerfile
```

-	Layers:
	-	`sha256:a97e44a00feda0c411221ecd4d816643ec3555227a6620f8efbb9d4c599bebd7`  
		Last Modified: Mon, 02 Mar 2026 19:47:13 GMT  
		Size: 5.3 MB (5327409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14dab9b076f2d1edb47e08385660a779637fbdbf7acac8371616acf204667872`  
		Last Modified: Mon, 02 Mar 2026 19:47:12 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
