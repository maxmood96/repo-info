## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:b4cc5c8d3f61c9169d5eed17665cebcc46a09dfd72fcdb260b3212397ce93eed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6007ae82e1d5b519a267708cb6f347462e0a6fd2cb17361988ab0b42b3cd7cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274040640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac3b662ce81676a08680157840864ee8d6911be872c7ae352dca6b09e2d69a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea58b7264f17ce5191bbe0e99cb4796e1348485afaaacad15a001210e699b97`  
		Last Modified: Tue, 04 Feb 2025 05:21:25 GMT  
		Size: 144.6 MB (144566550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f96c97cff4099c1fddf79e381ede706add355863d33e81e47993e6b6869673`  
		Last Modified: Tue, 04 Feb 2025 05:21:21 GMT  
		Size: 81.0 MB (80993363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797c6c36839c665383894b642599f5dc7db78f4bede706147885f6cb7140616f`  
		Last Modified: Tue, 04 Feb 2025 05:21:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523e3c7e786ec7c051a70f853d4348c816cf82470d1ededce5c49b58a255aa38`  
		Last Modified: Tue, 04 Feb 2025 05:21:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fea94856ff506d3580adf1d55dddf91463ece182c553da80664d8f8f17a90c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cad14d53ff96c2b3ed34453d45c19bf2e311f16878d14b4df88d076c0a0bd2`

```dockerfile
```

-	Layers:
	-	`sha256:54e1048455c19c7c62371b43c69730b3c55116dea7f39712dcaa9dbb54e957fa`  
		Last Modified: Tue, 04 Feb 2025 05:21:21 GMT  
		Size: 7.2 MB (7171078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5789678b6f9bcea2ef4675b09a04c77506d712a66595e3a7e424700d92f1e66`  
		Last Modified: Tue, 04 Feb 2025 05:21:20 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8889258811e4631ebf08cf94aa00591cf2a7126a73c468c62f45b681e50ea694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272607880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c882aaf18bba32b7da7e12518726aab52ae10e6f981f52724031f17e65e3122`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece757aa0497472085ecc56d9989c1c60e5e6753869c29bf01bb2400f7d2e1ba`  
		Last Modified: Tue, 04 Feb 2025 23:42:45 GMT  
		Size: 143.5 MB (143454729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8323ccccf23488b484dd009c52a53a7ec51530dfea9d4d4e6512c8fdeb58159a`  
		Last Modified: Tue, 04 Feb 2025 23:47:27 GMT  
		Size: 80.8 MB (80845558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0359852274de0b4218227149cc2564761ebd2513e4ff9bb31eaaea7a8b5ad0a`  
		Last Modified: Tue, 04 Feb 2025 23:47:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ce379e87c57ca3a87f4d1a4af5f78f3182264f5b72b77a93daeb39cd9d04a`  
		Last Modified: Tue, 04 Feb 2025 23:47:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e093b1f9ac33aadc898dd227655ac5ef9809afb34e65c0bedcaaf9c202d7c262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbb719f1e5b1e8845bceb426b4fde9d221ae1e065a8c90d7df70094b81ce09e`

```dockerfile
```

-	Layers:
	-	`sha256:ed90cacd025d7ce42fdd2ff045a0feae2d79494fa86b4a7b5edb41fb07b96a8f`  
		Last Modified: Tue, 04 Feb 2025 23:47:25 GMT  
		Size: 7.2 MB (7176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05242015f5cd1b383024c8acbb203f73a744f047ffa6a979c697648b4bc30efd`  
		Last Modified: Tue, 04 Feb 2025 23:47:24 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
