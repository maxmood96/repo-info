## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b1eb5becd2280ed0e7c599500a9b38a37e2c003ec3916d4cfd389a1828656462
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:21bb9700fcaddc72ec070169cfefbdf25e22debe42de1925fc1c2c5cf82be04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235073964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be9ac9ea1321c94b64b0192ff047c013df8e2f31f7ba542f7a56959c23c553a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:18:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:18:41 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:18:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:18:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:18:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:18:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684582baea6c4b561a58e71e059b85349f61691ecd6882143f82e03c0a191c2c`  
		Last Modified: Wed, 22 Apr 2026 02:19:14 GMT  
		Size: 145.6 MB (145628768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a806bb8e8127b70e4bcc32dae4ed21e9ffbafb492f3a3a737bc5ad932942f98`  
		Last Modified: Wed, 22 Apr 2026 02:19:12 GMT  
		Size: 59.2 MB (59186217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b17f70f213394a1f433c62b830834268d307f6bb14189b6961394abab482c48`  
		Last Modified: Wed, 22 Apr 2026 02:19:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ffce264681d2884f6ee52a2a82cd1fd6492a0895f0ce6e6b39a37425bdc23b`  
		Last Modified: Wed, 22 Apr 2026 02:19:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6faa8bc870dceab94bcdd39ed8387fa71f14b8c9cce7af70bfa568a6079732a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3e10d6ca5b800afd6807e630f455f504afec6f15b3255f6f08eb0c8cdb20a0`

```dockerfile
```

-	Layers:
	-	`sha256:3a9c6b4606ec606a6f68877b3d9525b995039077aa147439f4f4a2b13c5d26f2`  
		Last Modified: Wed, 22 Apr 2026 02:19:10 GMT  
		Size: 5.3 MB (5320053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96ef8f7c6a67209fc416b39386a5e77f4fd5c408214028326b1391bb22a6a747`  
		Last Modified: Wed, 22 Apr 2026 02:19:09 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8bed05e03e4778375052979f4676182d13377b4c04c84eae890a5672fafbcf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232510871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c68965fcd5bd5250e449a100b038d9a0faf8b6fe96fa79c360f3a22c4eefa0b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:53 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca66113d91a0e3eab2f159e6e6509499f8ef1e9525180a9674951ab3698192b`  
		Last Modified: Wed, 22 Apr 2026 02:22:29 GMT  
		Size: 144.4 MB (144436243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5338c3ab91fa8e283db73fe0f9b9c154eb3f1374044be8b50b0cb8cfc7093f9f`  
		Last Modified: Wed, 22 Apr 2026 02:22:27 GMT  
		Size: 59.3 MB (59331078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a1e87cc3d612ab6be252e148ffbd5b855aec63bdc163ca303bf3add9a1e836`  
		Last Modified: Wed, 22 Apr 2026 02:22:24 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1717ec1025de7e37fe311b24fab0a79df4242cd460f878d67157dd03d2b15bfe`  
		Last Modified: Wed, 22 Apr 2026 02:22:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d14ef4ac2de990e11b27d91228eaa0409f882269e477c4b1c135009d6aed5ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6fe5fd51d1400d962dce164c1418af33425be3bba71f97b9b28bead02fea8`

```dockerfile
```

-	Layers:
	-	`sha256:80f93f53d724eb852a1b5e9a9f11eadf42fda920ec9978d35dd2002a9b74e990`  
		Last Modified: Wed, 22 Apr 2026 02:22:25 GMT  
		Size: 5.3 MB (5325785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74944cba80a4075b4646fd390c18548f016c78a0c2d3b8e34d1475f5d98cfd04`  
		Last Modified: Wed, 22 Apr 2026 02:22:24 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json
