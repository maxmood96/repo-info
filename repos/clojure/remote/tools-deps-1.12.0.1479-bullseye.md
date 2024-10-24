## `clojure:tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:db44a7e6a8b24df7ab16dc8b4dc2a5364f3e3379655ccdd6c034eca2d47b3119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1479-bullseye` - linux; amd64

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

### `clojure:tools-deps-1.12.0.1479-bullseye` - unknown; unknown

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

### `clojure:tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dcc98db4e1bc066188e139319ba7ef3a05429d0e178ea3751cb3c450170432c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279949018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc95d820294a4581a1c836c46f7530daf110500d1ea473e5dd08d1687441e91`
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
	-	`sha256:8e6c724a7bc6cad4a23ca6399b659781378a31f3d057e3a52e35e8a27699eb41`  
		Last Modified: Thu, 17 Oct 2024 08:21:06 GMT  
		Size: 156.7 MB (156746197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2104b5d73fde5f1676859ed83f39dfcf41d2a5e444888a2e353b80038b206ce3`  
		Last Modified: Thu, 17 Oct 2024 08:24:49 GMT  
		Size: 69.5 MB (69466888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a15bc81ffb492dd77d700da83122a171e009ffcde72294b9d913051498373`  
		Last Modified: Thu, 17 Oct 2024 08:24:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5b868f65e25b6d32bdb0856ac334ab99c118039c51526bf22053332e5d5bcb`  
		Last Modified: Thu, 17 Oct 2024 08:24:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3e688408612a0fbeaa305c267c482b0a4c9a4ebe4f289c0ad058853facd8f0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe982acc740f4901cd8c6b9375488ec8f9c8e8ec96cfbde95940e0519c4f995`

```dockerfile
```

-	Layers:
	-	`sha256:154468ebfda0abcbd37367d568ca5f742511456392d8a8b46312f4da4bac47bf`  
		Last Modified: Sat, 19 Oct 2024 12:16:21 GMT  
		Size: 7.2 MB (7224742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581b1b5e9531bf4b37416f084e971b5ffb70da6e0c769a5d317b62eb89765cd4`  
		Last Modified: Sat, 19 Oct 2024 12:16:21 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json
