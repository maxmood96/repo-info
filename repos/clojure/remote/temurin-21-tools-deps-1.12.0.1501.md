## `clojure:temurin-21-tools-deps-1.12.0.1501`

```console
$ docker pull clojure@sha256:a00c61300ddaecc2d8ef4a1b3041db70773885acfc196c0647aeb642232edde8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1501` - linux; amd64

```console
$ docker pull clojure@sha256:1a64eb71e01c9b921f2aa49fd759a67f35617451da6dbac3b390c6df86e76b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287060610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b1e6af75c764b0c7dfb6c2990a332e55f2f1b1b0b9605a7d63f3b722ed9ce2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499548e7ad6be6ac7091a0dcbc38c45e3d8f8d6326fd0cdd725b7d3e5e6b588`  
		Last Modified: Fri, 31 Jan 2025 02:18:12 GMT  
		Size: 157.6 MB (157585902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902174eca99fa23dcf0e7bc8c3b1d5081c661b84ade7caeefc1caf31a9c58620`  
		Last Modified: Fri, 31 Jan 2025 02:18:10 GMT  
		Size: 81.0 MB (80993705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9decc8816f156f7aeecfcb4e1f2e09f55d9296deff1c7b46b48bd1b710b08136`  
		Last Modified: Fri, 31 Jan 2025 02:18:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31122e88c1e49278ce7341f317fed62781272b9d1ae52758ff79e211f72ad4e6`  
		Last Modified: Fri, 31 Jan 2025 02:18:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1501` - unknown; unknown

```console
$ docker pull clojure@sha256:17aed5e23d12af3fd14bcd24c43d7bff8b0467bf175a0bd857ab47d8e34aa232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33195a2a4a91adae2aab47a6dc1713d766ba9d3e49aaa61599dd97375a9f07e2`

```dockerfile
```

-	Layers:
	-	`sha256:b9abac109fb2094b0a065bac4544f9af2aab6d9e71272b08ba892bdde1f4a5e4`  
		Last Modified: Fri, 31 Jan 2025 02:18:09 GMT  
		Size: 7.2 MB (7176180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2b44a64889986425e3accdaadad0d5bf3a7f6ca5e0ce360e4a3e84a4d06a07c`  
		Last Modified: Fri, 31 Jan 2025 02:18:09 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1501` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a18b5ea251502e450f6427fc5d5a28636982a78f698e1e41c6e9f099499e9699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284946601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0b1c43b5a5768f6c18767931d56d73f0f04b6d6e6104f43499c1643ebfdcfd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3830f3f6245cfa167f19c2d8c8ab9554a513712b3d2d6fbc73a32920db0c9270`  
		Last Modified: Thu, 23 Jan 2025 02:24:23 GMT  
		Size: 155.8 MB (155793094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed2378b130d4e1893797f2f12609eb832185b8413519a456525c89de616a907`  
		Last Modified: Wed, 29 Jan 2025 20:52:49 GMT  
		Size: 80.8 MB (80845568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659ba122ff5d7e89c5630b45eb1c0f7bf2b1acfd0da483cbded2da24716bc0d7`  
		Last Modified: Wed, 29 Jan 2025 20:52:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a5e05a12dcb7e098f1092194a73a84271b0fca8e95a8005a68543daa6d18cc`  
		Last Modified: Wed, 29 Jan 2025 20:52:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1501` - unknown; unknown

```console
$ docker pull clojure@sha256:ea19324a28e3b6a2596f14f0c89f9106624008ea0c47e3a66bb2c88cee8da3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035f7d07fbe9b72a97f631c54ecfe305ce8d4fa8636a34486c63be46d4cd3902`

```dockerfile
```

-	Layers:
	-	`sha256:1fbae1a543662c91c68f4f2f1d24bd3d6e487a2ccf848cc8867a9bb7148d1243`  
		Last Modified: Wed, 29 Jan 2025 20:52:47 GMT  
		Size: 7.2 MB (7182017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d980341a14d1d9411deba63ed3022c15fc661fdd4d465bda0ba2e770d8f3262`  
		Last Modified: Wed, 29 Jan 2025 20:52:47 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
