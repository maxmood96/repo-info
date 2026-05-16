## `clojure:temurin-26-bullseye-slim`

```console
$ docker pull clojure@sha256:ad5d85067fc4d8f226da036031f2bd083be475c63f21b1244615501988a99048
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6e74002dd3981c56198b9250d38bcabe2cc599f511cbf11192a974b5abbac35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.0 MB (183973951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7634e0ba070fdb10d86160851434d095569b182db8741083b0f6c04fe58fd0d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:37:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:37:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:37:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:37:30 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:37:30 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f584e9d855f5283bcfad3ca085a072a0c5388ba061781cd7e3ce308f8590c287`  
		Last Modified: Fri, 15 May 2026 20:38:05 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e40ed28d29841040835b93bbbe2cfe051b0e9005885ea66f728b7fe2ed0651b`  
		Last Modified: Fri, 15 May 2026 20:38:05 GMT  
		Size: 59.2 MB (59190580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbd826efb36f23bccb94ca4f266a96682b147fa50428286e1688cd496d94be9`  
		Last Modified: Fri, 15 May 2026 20:38:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02756c078bf225adf052efc8b6501a68ffcd9bc2037492f791bcd43a4cce5f4`  
		Last Modified: Fri, 15 May 2026 20:38:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7267e97e3e7125d1629142d4fb77a9ab3d53549d370d33ffef5822fbd2dad0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf9263aef737b5657b20af8220a88caa63871cbf5cff5e4740df98572cd344f`

```dockerfile
```

-	Layers:
	-	`sha256:ee1f1c4081b1633aae4147db10d3146e05415f6cd5b68afbc247e45e83b86692`  
		Last Modified: Fri, 15 May 2026 20:38:02 GMT  
		Size: 5.3 MB (5285569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b1f4a562b57b9a7b66d60dd3060714a6a7789ef9f99322aee17b9b28ef2adcf`  
		Last Modified: Fri, 15 May 2026 20:38:01 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:088dd40c3330a1bcbf8845f81db96cf9c1d1d47dea1027c954858a38feb93862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181607757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a959ed0119ea43b38f01d3bdc7567516171d392accab093000540c701880f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:36:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:17 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:36:17 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37787db71b9cf81d1713c7469a8cf735ae87be523cdbd02c273fc22bfccdf1d6`  
		Last Modified: Fri, 15 May 2026 20:36:51 GMT  
		Size: 93.5 MB (93504415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1482c89022d1d38acd4e4959bba5853c8236a262c9a0a72a24e3f2d205f2d571`  
		Last Modified: Fri, 15 May 2026 20:37:26 GMT  
		Size: 59.4 MB (59359707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b961dfc321185b85275820e8281f08027cab78cbd6746a2681018aa0c7401e0c`  
		Last Modified: Fri, 15 May 2026 20:37:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f8bc233bd6e419c6db666708841a1b366a5b16100d8f4bbfd3271f3f4b7d49`  
		Last Modified: Fri, 15 May 2026 20:37:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d2e3e8108907d7b8a33c2300b75ca7fe1b98f539f3074372413d2ce69eba7572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f31d674b376886b468fb5ff9efbcf589ff45597c1aac3aa0454b28698095573`

```dockerfile
```

-	Layers:
	-	`sha256:f00aa44eddfebdad2179c9f42ff7bf32fbcb9ec83782fa02cb2a83f666ba3d5f`  
		Last Modified: Fri, 15 May 2026 20:37:24 GMT  
		Size: 5.3 MB (5291298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39362e1af74fd3555bf1ea6ebda8dd5c987e0ca1f5b4ae23ad54947332087925`  
		Last Modified: Fri, 15 May 2026 20:37:24 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json
