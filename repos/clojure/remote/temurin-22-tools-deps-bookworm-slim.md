## `clojure:temurin-22-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:5b23f3b4f5400ae0cd24fda4f9173c15ebaff29a7c7f9a96f50ec4085e87b110
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:09002fae69c19446cb61ad897c34eb1bb7eadd50eff5a64dcfe8649d681abd4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255091813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5730aca254739f5de2ba9cf7298503e2661bf347841b6e9019a978c920f278`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782ac4883076250d708f24bebf5bc8ad05092e801bbec2546571e2b43e729304`  
		Last Modified: Tue, 17 Sep 2024 01:59:18 GMT  
		Size: 156.5 MB (156481644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09391d477923ac47ea4b81b75faf69a6bdd4004189bd858550d5a038f36ece1`  
		Last Modified: Tue, 17 Sep 2024 01:59:22 GMT  
		Size: 69.5 MB (69482640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c05b7e39ae6d37573371da7888cffb155f8e7a961109c306c5cdb094293576`  
		Last Modified: Tue, 17 Sep 2024 01:59:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534b8ef0e365566ce8859bf6f0b0295cdb0210085577f296f2ee4805c2806d77`  
		Last Modified: Tue, 17 Sep 2024 01:59:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d317cdb03deb8c840b7f301d769834db9a0e7887d53f31927c270ff1b7f85811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6939ef785370c9a746d9adbdf66cfe4ddb91ac02556c20f4bcc0c5c38b93415f`

```dockerfile
```

-	Layers:
	-	`sha256:fdf20f2f76741735d45f72a9b35689a16bc471f945848e16cc7e4dc05073f0c6`  
		Last Modified: Tue, 17 Sep 2024 01:59:20 GMT  
		Size: 4.7 MB (4745186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:813b70a3546dd5dbdd0e694bef9bee2e50e6a367d140dbe56f11239a81abe50d`  
		Last Modified: Tue, 17 Sep 2024 01:59:19 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73fd6ef40156e337a33fae791b5167c0b43d8c50c2baca598bd2c9117cfcd749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253005974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598dd4c6b12c054eca53c683cc8921e9622943b9fa1c083673b9fdb00c92be85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b2ca3ad02bc27e2d696418f91068457394caea057919085f588b3e25db52ec`  
		Last Modified: Tue, 17 Sep 2024 04:52:52 GMT  
		Size: 154.5 MB (154503758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237e40a46a0cfaf7c94b908c7531bdabb5a3d8380a5b356f97e62a91ef0b1595`  
		Last Modified: Tue, 17 Sep 2024 04:58:34 GMT  
		Size: 69.3 MB (69344626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f0a2dd615d0baa971571545532df298facf68ea314b701cb48f381af5b621`  
		Last Modified: Tue, 17 Sep 2024 04:58:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac166d6befc53dc196640a95a01a9e04cc003e63ad3207d6534372e90c81cd`  
		Last Modified: Tue, 17 Sep 2024 04:58:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fb4e4111fd7efc135d4ee852f3d116e173a4fe8691a21632f71d46c334f0124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aabe4cdd6ee00fbd7d332edbba166c04860cd2148f6af816a1118ed537dc9d9`

```dockerfile
```

-	Layers:
	-	`sha256:91265c1eca341cf90dd3d8512c1ac7c6c9f8efbb229afa32ab73e2a9ab02157c`  
		Last Modified: Tue, 17 Sep 2024 04:58:32 GMT  
		Size: 4.8 MB (4751571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61a9b44aedcf6617872f6dbcd1f63d6750c8f678b41009ddd8acbdcbbad2a773`  
		Last Modified: Tue, 17 Sep 2024 04:58:32 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
