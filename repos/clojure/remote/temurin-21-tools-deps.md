## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:4500ad1b92fbcd9211200f5b114e62697ea29064c4ddc33d1ca4c90320f61b96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps` - linux; amd64

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

### `clojure:temurin-21-tools-deps` - unknown; unknown

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

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:07ab6b8ab8f06456f42b12d985340ceaa700ee6c508d38755f7e1a10b7621426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285012966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28108f332fdc30b7e4f9e3223c9374076d07fdb61304ede2cfde58f548baaab`
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
	-	`sha256:0c34e075e37e524b436802c62baf0679e4472bcdb458b6ac93c635e1e1afa9b9`  
		Last Modified: Fri, 31 Jan 2025 04:51:37 GMT  
		Size: 155.9 MB (155859318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b1364cbe24c3f518b6585c597b31c577d224da4b51225cac01a4d39e88f5a8`  
		Last Modified: Fri, 31 Jan 2025 05:24:15 GMT  
		Size: 80.8 MB (80845714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed19fe02177bfcdf4e3c1d87f4785530a429e8a9620ab0babeebf12f593a3d3f`  
		Last Modified: Fri, 31 Jan 2025 05:24:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543c98abed75c063284479c557354f45f19e4c789be146eb7ee6b87d40c4d5cb`  
		Last Modified: Fri, 31 Jan 2025 05:24:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:589bbeee94be98884ab039c178f16201db19a3f0d25173be067261b00f2d020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8025a0ef1a0f160b5ad36e8a0f8956269826cc8e42d5ef886c9f7ffe018fa130`

```dockerfile
```

-	Layers:
	-	`sha256:0269aa65877db5c5aeb48cd10b646b482c887c7cab7c92afa2bdf877a896a425`  
		Last Modified: Fri, 31 Jan 2025 05:24:13 GMT  
		Size: 7.2 MB (7182015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14891f96fea4cbb1d4c0afa70334aa1f4bbcdaa0155bc48884107c65ef2a6190`  
		Last Modified: Fri, 31 Jan 2025 05:24:12 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
