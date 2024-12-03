## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:6ce82a79417c3ad7290ce26b17cde95846bf4137d6abf075cbbb9b8aa97af3b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:613fc7f582329abf808d6c399a5c6d429021dafc2572056778ba536005086b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288194639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06579794b01625e7c4aace3f25a228aefc82a42747218dcd1011c71d51c9ab55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0918f1eb549dfc6bdb6ccf7e5abeb0cfb05d68cf9ff5341d3f75274a6a3dcf9a`  
		Last Modified: Tue, 03 Dec 2024 03:26:12 GMT  
		Size: 165.3 MB (165295086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8420d0d862917e0b562f9dfc5c99f50e1566c14d4453ece1f1261c0b346461`  
		Last Modified: Tue, 03 Dec 2024 03:26:11 GMT  
		Size: 69.2 MB (69159369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44675d7fafd219c837cb476b73a1cc565fde7f2d71eacd64ffd4abe8da478af4`  
		Last Modified: Tue, 03 Dec 2024 03:26:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fb45f6b3617cec2b98db343a5d070cb93b57f3cc6422c8b4ac8a429de3ecaf`  
		Last Modified: Tue, 03 Dec 2024 03:26:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:17b32d6547458496a57e8494a4ebd718cf9ad0cc38d3fb992597ab40dd3e3532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c54e4c9a7a4d088acff1a29960b771b8cf87f1904a47998f560291264ea85`

```dockerfile
```

-	Layers:
	-	`sha256:8ab38f1c11f3139ef5745d41a52dee958c1bca438a66906d26ce2b71992a41da`  
		Last Modified: Tue, 03 Dec 2024 03:26:10 GMT  
		Size: 7.2 MB (7219080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6e4794132e5fe9bdb8c7ad0900fe50b6701c92fcac055dce5058aec987bea1`  
		Last Modified: Tue, 03 Dec 2024 03:26:10 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9cd59b07f17287af9597046e26e65a3c85be720436db66038e9a396800b3c9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284814545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395d4fe682932d3fa30351cf173f46469304ab8157031ffcab0315652ccc172b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c8e918cd2fa2f476de90384d529eaa69e1864493a438326b02dc1ef14b0a54`  
		Last Modified: Tue, 03 Dec 2024 15:34:06 GMT  
		Size: 163.3 MB (163281807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edadd1751380d3b5dcb92b6d0f7b582a3368df416114bac752a563fb403f9c4c`  
		Last Modified: Tue, 03 Dec 2024 15:38:13 GMT  
		Size: 69.3 MB (69285701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00371b9bbce58db30c8fb3a38326cc42b5c6b49be2437e308c15f961bb0eb00`  
		Last Modified: Tue, 03 Dec 2024 15:38:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3533cb011bc5caa899997bb664965021a702f53b4bd4710b9349accbdf7300`  
		Last Modified: Tue, 03 Dec 2024 15:38:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:eb76b6e32b281a0cac1df7673226572361de85367e388b97efaba2b9c5a7d6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7239499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ed882846772dbbde651dd4ff29333e2e986e1f3469b5dcc216b81bc5b887ef`

```dockerfile
```

-	Layers:
	-	`sha256:691591bc4410078247613a2e20e1dd723938a44be9945a466c04d92e154281f8`  
		Last Modified: Tue, 03 Dec 2024 15:38:12 GMT  
		Size: 7.2 MB (7223561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61db430659c38e07303a0599b33648af1270509d8eb08a967dbae5b0feb8f226`  
		Last Modified: Tue, 03 Dec 2024 15:38:11 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
