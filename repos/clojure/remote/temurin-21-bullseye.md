## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:e45692c8d84d4edc7d1d843cfa2d28ee9f19068e98b180ff5783f4a9e748104a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:efb4ffaf40a75ad927bb2b9c5492f66bac361f0ac2bf09114e96b0eb72367213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284330642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07dd5d89df755a454b03a0c5a6de1adef1050cb5a3294c5153b7745874e68ba6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbc681a73db9cbb61659c1d116af58e3f64b0d2fb43896352dcd38fd2e5762b`  
		Last Modified: Thu, 24 Oct 2024 02:00:41 GMT  
		Size: 157.6 MB (157568686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7c49f1476f91d7f491cbeed40bfb79d5d5bc7c207c184a3b52c2f3065a6ce`  
		Last Modified: Thu, 24 Oct 2024 02:00:40 GMT  
		Size: 71.7 MB (71680305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6b32ad2db56b1dc9ca68d6cfa640c3d3810776ab3a75b86682b8944f2b517b`  
		Last Modified: Thu, 24 Oct 2024 02:00:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16341bb0df8c903dc5774813e1ee7fe7ec69b7a6a58cd35d3538983ac8383731`  
		Last Modified: Thu, 24 Oct 2024 02:00:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7ecb29d597d4302d2da62b044aa196de22f6878187b289c83325f4b1c1f25fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26086c31b7a80f36f6cbcf20bce28d3fc7fad325506438a2f5679ec539d4b8`

```dockerfile
```

-	Layers:
	-	`sha256:67f8786ff98bc82976f7619ce1c7321e6c40cfed20b9678c7b9050a0fa8e3a27`  
		Last Modified: Thu, 24 Oct 2024 02:00:39 GMT  
		Size: 7.2 MB (7219617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c88c5572d35c50ab32b1f488c6ffe4150a862c6e659436cc3b74a154cf3eecf`  
		Last Modified: Thu, 24 Oct 2024 02:00:39 GMT  
		Size: 16.3 KB (16322 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1069e696d1c8ad246a285efa91bd771c054d0371e0bb22168c106d4511c72714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281300656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db7bffcd955e7dcf38e4649b81210477248a449ed79a78afc62525e54646d69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda1f5042875c6cd55ec9afb14d7d146178d30c5c91dbfde893cd3a021c8420`  
		Last Modified: Thu, 24 Oct 2024 09:26:33 GMT  
		Size: 155.8 MB (155793065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21796739361946ac45b4d37ee3b83266453c459ab57c41133f3d0a6610a1b014`  
		Last Modified: Thu, 24 Oct 2024 09:32:26 GMT  
		Size: 71.8 MB (71771658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b10ab76587a047c127759aaffbb428170f7d17b9862b2f7850a035fda705f76`  
		Last Modified: Thu, 24 Oct 2024 09:32:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eb303a070a9037c6ce9b3380cb4884c6a00fe5c1f4e1e250785edd49cf5642`  
		Last Modified: Thu, 24 Oct 2024 09:32:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bbe29fc04e555f3a3808e5b92c0a08fa6ecdfb7acf3228989d713a080c8f1c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f61f4242e1ad71456a9398caad7a746d18d908927574206a162d982764ebd7`

```dockerfile
```

-	Layers:
	-	`sha256:1114014b40989bcbb7b58685c5613a6f9ffe4ce641213e73b269dd59be4d3446`  
		Last Modified: Thu, 24 Oct 2024 09:32:24 GMT  
		Size: 7.2 MB (7224744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751c80c4c0de3279d2ea01a8527d0860bac8a7b39589b58004a6a8283a2ea324`  
		Last Modified: Thu, 24 Oct 2024 09:32:24 GMT  
		Size: 16.5 KB (16458 bytes)  
		MIME: application/vnd.in-toto+json
