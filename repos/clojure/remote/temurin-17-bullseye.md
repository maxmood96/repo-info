## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:ea08f004ccf599c8f52c3ae7cee3646f1358d02b705587b9fd4ee0a9b1a02137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:63e9bd12de0cd1eeee0bb2f2eef57a96fde267a9af08eaf3150265a6b12a7507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268974001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a5b123ca6736429fc6760a7f5801d0bd26e630fc7029974c355b2e29fc6d4a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:35:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:11 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:26 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bad0261e203a7d2664fbfa6e463c0ceb3a06ec58d13337577a7f201064d3931`  
		Last Modified: Mon, 09 Mar 2026 20:35:49 GMT  
		Size: 145.6 MB (145628704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c782543c1bfd770456e093796e088ab96edea16dbc896dc8038c51121a86c48`  
		Last Modified: Mon, 09 Mar 2026 20:35:47 GMT  
		Size: 69.6 MB (69587817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab479243b881bf3c75e6138c3fa275a18a3d6ca1d3d8e5e5150cea7baa2793a`  
		Last Modified: Mon, 09 Mar 2026 20:35:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1a3f58ed1e5c048188ca03bb189b60655d06619bfe45415297b25b46996709`  
		Last Modified: Mon, 09 Mar 2026 20:35:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4848af6413473bf8a0dfd64adbe8bd69066f74362535f29b6b8ca5bd410afdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08439e15239644064870e4ac5ba29a8cc5bd742201656b5f7e6f2fe5a5bf15d`

```dockerfile
```

-	Layers:
	-	`sha256:7b23b5cca86766f038726ce982cceb66af03f00abd6b8f279df1eadec0b7ae0c`  
		Last Modified: Mon, 09 Mar 2026 20:35:45 GMT  
		Size: 7.4 MB (7409277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a43158a5c5e5c3261b5c74fdcc8456ae71b78979337e7f53fbfd068df7a3f92`  
		Last Modified: Mon, 09 Mar 2026 20:35:45 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cd729e38f7b807ed2cfdef54816730b9bc44923a968dd187019b5d47e0a3ebf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266423881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38d4d4cd56bbd09a4527bbcd97d3ed25f142af3a460f1b20d116fa4f4538a05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:35:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:02 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:16 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af68f4ea187fc9dcccc7a2caa0cb02db1c20e946ea4d6922c6108481b093b71`  
		Last Modified: Mon, 09 Mar 2026 20:35:39 GMT  
		Size: 144.4 MB (144436208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439e81d1842505205a33d2e05709de4180eafb67ad01c2e60b0845079c078a32`  
		Last Modified: Mon, 09 Mar 2026 20:35:37 GMT  
		Size: 69.7 MB (69728237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbe6b371edc0ca36bc3ed9a1d2c49090a534355a6b7f1bdb89cca0a36cf6da2`  
		Last Modified: Mon, 09 Mar 2026 20:35:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2633b7c44d1bdd65336ec64dc587496ec9c4fcc9ac3f269050117ec28e754936`  
		Last Modified: Mon, 09 Mar 2026 20:35:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:782a0e68ad0ea6cd6075c7a3ec502614badc86e7cd7ce66329330320583f338c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5786f3db1a4e88d151a5339b0305f658969468b147e6d5731c3ce05d5dea69c9`

```dockerfile
```

-	Layers:
	-	`sha256:c0cbf3cc8c0451b0b4c4e34bc8dc9cc90948638fda3c5a8a78599693b5d2c875`  
		Last Modified: Mon, 09 Mar 2026 20:35:35 GMT  
		Size: 7.4 MB (7414376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae22e4e52353da15e98575147890b66a2a7d0d9311e56a119ad7a7b2fdd5f40`  
		Last Modified: Mon, 09 Mar 2026 20:35:35 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
