## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:579d962ef0042e77df50e18f545fdc1ae27e7ae7006680959b65e471f3a9e26a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1d20fc84992f54f3135a0b670290277053e08374fb3acd37de4ad6c9533b14a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280784416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9126c20feeecd3afa0065ee7452ffde3470f093a1bc65aae929afd13d8706cd6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a890068bf1806a44acb308eed42fc802e900a56e5a5bc157868bf13c7f5a5e53`  
		Last Modified: Wed, 21 May 2025 23:33:33 GMT  
		Size: 157.6 MB (157634458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f185aea90b4822509ce949fc98c9f06f36d2fcfca2f0efe1db7d2bc3303693f8`  
		Last Modified: Wed, 21 May 2025 23:33:32 GMT  
		Size: 69.4 MB (69398723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2c0ec17e508f66362e297803c79d3a52af458ee7e98585cc39507da5da382`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c9175cef5584b4dcf17a368db66d17324bf0895a25d1fa519540fd9bb243c5`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:21e403932ab647c5a2e3d79b77707a92653079c620f8ab741e242ebd71fca52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7274865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d76bc69073af1cece2a36cbf5b467f110253305b55ad4d046cc7634e6eb91e8`

```dockerfile
```

-	Layers:
	-	`sha256:64181c04152334dd81f5f39d05cf7d543b6fcf3f2b530a68568243b74fbf5c86`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 7.3 MB (7258368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe750d9b7d6cc8069968339dbf0ea6fde1e0364cfee4949ef055474e747b113`  
		Last Modified: Wed, 21 May 2025 23:33:31 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:585218be596f0b4af61f345f9f2c0c75347a07bfc58d50ba324c250043d3e976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277708448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1072e8d1b324ccdfca15284dde817dbf4d73ae17c9a05cb8718c2abdd0f94385`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e20865038b3b3ce624032e3975061a0946d41c6f1ee3d2697460ecc4305a60`  
		Last Modified: Thu, 22 May 2025 08:30:47 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005da2dec97fa7ff8f2a1305f1eea5573cd9141dd7617064381a9a43a13bca9`  
		Last Modified: Thu, 22 May 2025 08:35:40 GMT  
		Size: 69.5 MB (69530828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c455b1df422b08c9776526f62ca8a3b1c76e2628bf10aa5cc415347b346332`  
		Last Modified: Thu, 22 May 2025 08:35:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cbd9c9c8fd0bfa345a1472a5b194b0ebd04bb8f89e319345c6ac2518728b84`  
		Last Modified: Thu, 22 May 2025 08:35:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:46f4c808c92e5ebc22a4965400519d6c7ece4fa2603a77babfcd7eb39c5238ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7280130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ead25bd940e202c58f1ea8e62c375230b718bb9f5a843b6cf9f8e311f11bdb`

```dockerfile
```

-	Layers:
	-	`sha256:c708f13c603a7df8ee9200e4b92f683cb911c2366f959e23e146c947e1694cbd`  
		Last Modified: Thu, 22 May 2025 08:35:38 GMT  
		Size: 7.3 MB (7263491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7d088ecf47e5478ffa11db80cb42fbcf75ea1ff81fd013a58b1d3a91a14a4e`  
		Last Modified: Thu, 22 May 2025 08:35:38 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
