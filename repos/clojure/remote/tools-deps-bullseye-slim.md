## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:d20ea7cfe456601f534c4f257e1b5e207b7e065a770e4600ffca44a18982f358
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:64b16c80ec835d74108b8b4cf3430cb12ab6a3ea7fcb6c99d9640b5cd095c427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181701648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce3d19394fe92a4aebafce57f998a98e79d07e07df52d6fb8b53f34cc7310cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:09 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad6468837cb0e0b2b6d13f5d2afef9a22c943c3b2c444e217deea4e208cc2ff`  
		Last Modified: Wed, 22 Apr 2026 02:21:44 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892196aac3bcba49aef68c3755c4f24be1b19eba3fd352efc7cb11c941e85072`  
		Last Modified: Wed, 22 Apr 2026 02:21:43 GMT  
		Size: 59.2 MB (59186342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc053fb7a10229e39ad9b5a5a187894beb319474f9c649027195aa09abe75da9`  
		Last Modified: Wed, 22 Apr 2026 02:21:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c13cb2f24f7acc09897737c99d8d257fe22232c5dea8c2e1a1020bb9ba68c1`  
		Last Modified: Wed, 22 Apr 2026 02:21:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77c35de25df514c7d97a0f989f076c3f382aded808e67546f410842954cde1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa9a7e83668702e4e4dba7b3cfe2a42cf5194eb3662afb621e125715346ca01`

```dockerfile
```

-	Layers:
	-	`sha256:07b6520550444455ad6cf303d67feeb0bf79639df82a36ccb8fb3517e0c960cf`  
		Last Modified: Wed, 22 Apr 2026 02:21:41 GMT  
		Size: 5.3 MB (5288147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a11cae53ce5a41d3ad3834fd5135c6a82a5ba36c7f5e7df6522ef1cbc8c1f9c`  
		Last Modified: Wed, 22 Apr 2026 02:21:40 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21f0ffddaaa9c45d55cbc20a8eca6b52ccfa04ff015057720498d2725ba11261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179362786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011ed81b23bd796ba13f04b5527a7976904ffc3bc441da6b3ad551c29734cf57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:24:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:24:05 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:24:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:24:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf4f26b5d61cce487fe187671c0eaad9cf02390a1d37bf69c8f3d9535f60c36`  
		Last Modified: Wed, 22 Apr 2026 02:24:40 GMT  
		Size: 91.3 MB (91288310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e08a035b9434842ad6cb44ce179c08da1933ae84ec91575fe669fc195636902`  
		Last Modified: Wed, 22 Apr 2026 02:24:39 GMT  
		Size: 59.3 MB (59330925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0203ffe959206d57dc6a3a099a29efe4798d5ba9bddc4b1eb412097045b9a538`  
		Last Modified: Wed, 22 Apr 2026 02:24:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6392c544db5244f965c7c8c32d724356bb2142d3e4825fc12069b3806b59adab`  
		Last Modified: Wed, 22 Apr 2026 02:24:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32bb79e669ca135c2603f5e135606accfa00c4618795a23ae9d94622280696f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5310567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5028f76a784f42a67825918c5ddd2b80e13a50132e6e10446726e94454acaea`

```dockerfile
```

-	Layers:
	-	`sha256:a3beaf2a834453f8d4706e4c7131ee16957bacf480cd46b2eedeeed0119f2d58`  
		Last Modified: Wed, 22 Apr 2026 02:24:37 GMT  
		Size: 5.3 MB (5293900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f6f15c1d647ccbdf6b31dd2c89b81b9ab5fbfe83a85d2f0daf124582c52539a`  
		Last Modified: Wed, 22 Apr 2026 02:24:36 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
