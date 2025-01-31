## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:ac5a550a5d3744b2e06db795f227293a0e7013e2307a981a7355671fc70a210e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0c50168a567fab02c4f7fbe01089b6719d2891988d1c0d7304fd29f8aaf0e0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246627389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e709362af63b6f512d02cd7273ebf28e757aa9b43b3bca6fbb960419d3e55d12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d4360239b1797887a9d99d900562943ada3e2bb6847ac0c0da48071538daaa`  
		Last Modified: Fri, 31 Jan 2025 02:18:16 GMT  
		Size: 157.6 MB (157585908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0d73361fa7928759b963cc4b54b27bec18b2d5af555bdeae26d86fe206203d`  
		Last Modified: Fri, 31 Jan 2025 02:18:15 GMT  
		Size: 58.8 MB (58787775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615e463ee2d840090bda6961e172d082ae5a705bc5bc9e4a0ca0a84e977ca48`  
		Last Modified: Fri, 31 Jan 2025 02:18:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b36cf7ad16fba3596f384aed6ce5e34dcc5c3dcf22b243d15d7d758e6f1484`  
		Last Modified: Fri, 31 Jan 2025 02:18:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b78600c08840296fb1d050ca642843639296650bfe3ca2a4540d493d9d0e76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10f451fcee448cc4096a4e915d68d779c439f1259f9db248073ae2c44e12272`

```dockerfile
```

-	Layers:
	-	`sha256:fe63e7a92f5894e2fb949a7acae6b28503cd35f9a2179cf9aec3f4c5a9c352a5`  
		Last Modified: Fri, 31 Jan 2025 02:18:14 GMT  
		Size: 5.1 MB (5120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:960ed126214a0e157be3bfc6c894a86b5014fb77272d33651b184d9389d45959`  
		Last Modified: Fri, 31 Jan 2025 02:18:14 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ccc44e959b2487368f5c48109f36af4d33d63d8d9e964e206f6e19571d5cfe38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243514429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14576c7489440a871a0c7eca30f94234eddcecdf2efd74082ce5b56f05a9c2b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc3ea4febeac18700dd0fad07b719e7b913376667b87dc7052c14b9ab784817`  
		Last Modified: Fri, 31 Jan 2025 05:21:51 GMT  
		Size: 155.9 MB (155859332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f75f2c81d912fcec5c1c3db6c9c4d830f44e0ac996d49f824a2e7d3cddf4d70`  
		Last Modified: Fri, 31 Jan 2025 05:26:29 GMT  
		Size: 58.9 MB (58909143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed572e9edd7f545a466f2c81a060f2dd1b60659b89e5b4a6a1beda1bf3316de6`  
		Last Modified: Fri, 31 Jan 2025 05:26:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e2a4b7264471e63b76123d7fbf638a9c7365643e4450c7dd6b075bb3e612b6`  
		Last Modified: Fri, 31 Jan 2025 05:26:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29a928306371b66814127d71b736952215c7bca0a36c9abab138883df7535474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa26cd4cecf314be7e261c4452bb2b6c6e97e53d77061489dee5216c6a9a2ae8`

```dockerfile
```

-	Layers:
	-	`sha256:8299d9636b563e9974c6d4f5145dfd28f49d68e0599e97bf0952a06d63240041`  
		Last Modified: Fri, 31 Jan 2025 05:26:26 GMT  
		Size: 5.1 MB (5126621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add9d1526d2aaf000603bff30af59dcf33d4f4907c0fc1be50ffc582736c76ea`  
		Last Modified: Fri, 31 Jan 2025 05:26:26 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
