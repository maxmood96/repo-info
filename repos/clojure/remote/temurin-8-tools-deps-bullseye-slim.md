## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:f2e4bb6440fe98548a4cf8a1123f7a438a96fd6864ffcefa8060e8af387c53c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ef6d14e98b6ef6cc138c6c9f80993b1879315572a86e126d5f4d592fae0164af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144643093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350bb4d893861b415d5f3a1c50bd70e4bdac210593512e554a04400455b47557`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Tue, 12 May 2026 21:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:46:03 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8078db0da69a7af85351c732ca8e2ec3d9910514372e2beb4e4068af824583f4`  
		Last Modified: Tue, 12 May 2026 21:46:31 GMT  
		Size: 55.2 MB (55198701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efa8b9e6abf6fbd94441dc82fa9493672350249b404237ac5519e317eb1952c`  
		Last Modified: Tue, 12 May 2026 21:46:31 GMT  
		Size: 59.2 MB (59185786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d93936ff270d0fdb94cbf25721275394031b378da5b9a508b1fe3ceda0b5c8`  
		Last Modified: Tue, 12 May 2026 21:46:28 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bfac3924ccafdbe1a0c4f040d5577e0b129129eb049a53c6d0cac2e0928f70fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6add852e1e0b30e2f84693b525ea0eaadb1f95b7177198ca319c02754b77a5`

```dockerfile
```

-	Layers:
	-	`sha256:93c6924ad8a7f281230e2a2d81adb4eb7f0ed8fd3e214156403490c0776ffc93`  
		Last Modified: Tue, 12 May 2026 21:46:29 GMT  
		Size: 5.4 MB (5441040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3f7263b0f966ad488a9f310461303bfdd1f59becb858dd1b7c554cd9eae6e3`  
		Last Modified: Tue, 12 May 2026 21:46:28 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad60e3198041fe343e9a1ee42d1a807bf8d28c399d9bc2e75a292083fc9890be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142347374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a211d5e88be49233e7cb9b6805d8859f935d42137567616215748ea1f965e7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Tue, 12 May 2026 21:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:45:51 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743475f5a7167841294af18dfa9ae2d880a11e3977424e24f9d78220096005ad`  
		Last Modified: Tue, 12 May 2026 21:46:20 GMT  
		Size: 54.3 MB (54272928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4076117d4f692bf0f212eb8bc5f0422144c1dca46fd648be12c0724396841e97`  
		Last Modified: Tue, 12 May 2026 21:46:20 GMT  
		Size: 59.3 MB (59331208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99b72380d8b70be5af039479eb9b18c7acffe62c8649bac7c94bc3606552d86`  
		Last Modified: Tue, 12 May 2026 21:46:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e446b5ac74c271fa1d2e1d0935f7ebf76ab1365ad0cad3288c4772706ad7250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fe7cfc68381292849deab5f5bb25cb2d40b3cb37d4f6f217091f0edafbc46a`

```dockerfile
```

-	Layers:
	-	`sha256:387b8f0086b949fc109a1b8f42bdc0b99f6243d5596c64a0095753815bcc6a95`  
		Last Modified: Tue, 12 May 2026 21:46:18 GMT  
		Size: 5.4 MB (5447472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c4936fb107b6e0ddf9a04ee84b41de319be6ac29c728e0a20709bf8f44a89e`  
		Last Modified: Tue, 12 May 2026 21:46:18 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json
