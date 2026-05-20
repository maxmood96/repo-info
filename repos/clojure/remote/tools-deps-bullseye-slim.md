## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b9b563667f59449fff17b61492a870fdcb7eaa6831dba876e87d136395d3bac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a069f27501f0f6731cf918d4afe56f680ad968ef7bf85c97a9ea9f0be3f94334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182023825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e717796f7d6bdfa69bc0e17663e0e52ab5d3149b5682598c6980a2396c545624`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:01:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:39 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:01:39 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:01:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:01:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356b674fae7527c053156fb7e19b21b861aabffc2897a7f9f14daf5723bdda83`  
		Last Modified: Wed, 20 May 2026 00:02:12 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075b85bacd8e7c03c6465cdd4987140847ea2f6e25620643e53ca762cef68b0e`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 59.2 MB (59190621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caebe5d27d937794e1f7d7fd1841060d0eb4dc77fdccb0ef94e53c4a713fefb4`  
		Last Modified: Wed, 20 May 2026 00:02:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888f3a7f81f43db5505ae58abaacad3552a9d3abf266a96c858c43acc2cd7f0a`  
		Last Modified: Wed, 20 May 2026 00:02:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e0901bd4505130a3cacb54aaacdd6d97d022dc47fe81a47a4d1a4eb27d090fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afb4f3feb0cab61c99b1be4bffc10eef3c96f2c094aff140e9b43a372b0f4b3`

```dockerfile
```

-	Layers:
	-	`sha256:65fdafab66d2f82f0c246c7ba567a3baa196cb8850e1e1fafeb8533969031028`  
		Last Modified: Wed, 20 May 2026 00:02:08 GMT  
		Size: 5.3 MB (5288768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332d92d5f738ef3c7085cb1cbea57764c379bd1b2e68e61091418fe364aac3cd`  
		Last Modified: Wed, 20 May 2026 00:02:08 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dac6430bd8dafd15d0b7bcc9e4c5d67aef7da90e4c87c56971c1d6b2e5349361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179646634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c88f23f44f1e982b15d2beb0e881c7fc70cef64a58fa7d6546c861ffc29a642`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:08:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:24 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:08:24 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:08:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:08:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ce3dd0057a2a2ec4a603eb373e747d6b9d1b79507268496f43627a5f7d237e`  
		Last Modified: Wed, 20 May 2026 00:08:58 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4fa5b3ca3f3abd32b7d03177b2c381d15e1ef25927c0b1b71ac5a141b55e95`  
		Last Modified: Wed, 20 May 2026 00:08:58 GMT  
		Size: 59.4 MB (59360365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c537e4d190e4f94b95c798268ff91293c040b2e9ee5e357a5e9f141415806c0d`  
		Last Modified: Wed, 20 May 2026 00:08:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4d8f40d06b5269c64de74ae5faeb3172ecbf17b93c1a21e607899b866334d7`  
		Last Modified: Wed, 20 May 2026 00:08:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d05fe9547dff70d87075f59936cef8f7e23a20ee8f94f77a4b0aac7aa4abb8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230bbdfb66157bc2771c08c04781b46f04aaa3279f6323a81b0082884c54499a`

```dockerfile
```

-	Layers:
	-	`sha256:af8fd806d67b41ca50386e67bf088a8c96fbd8c1b043a199ede20270e118ba0c`  
		Last Modified: Wed, 20 May 2026 00:08:56 GMT  
		Size: 5.3 MB (5294521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457d4b385c56fc9f818923919bb63d73323e4cd090c5af0efef85b673ec83c19`  
		Last Modified: Wed, 20 May 2026 00:08:55 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json
