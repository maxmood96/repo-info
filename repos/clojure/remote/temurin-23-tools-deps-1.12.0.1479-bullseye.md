## `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:85f70078ef4c8af3e86f07a08502a8ef4656b52d16286c4798de90e7315742b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8ccd78ad67b069cc194d4a349ab4052d42dd4de3f17eec61270799bfe889a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292056789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce84d77a22aee23743a8eebeebdb00950f60685bd3edbd0765fb5c94406eb54`
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
	-	`sha256:ebb4f5a4cc339643ef766a5b1d19f72fc33ea13bbba812cbbc41464d79f2a428`  
		Last Modified: Thu, 24 Oct 2024 01:56:57 GMT  
		Size: 165.3 MB (165295134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c846d96cb60365f2231623deedcb30f57dbd6684b1105bfc2fba3428bfd9761c`  
		Last Modified: Thu, 24 Oct 2024 01:56:56 GMT  
		Size: 71.7 MB (71680001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0773a969f68a620df69aae1362891deb6f1584916a7cefb0f4b0ebf996d994c`  
		Last Modified: Thu, 24 Oct 2024 01:56:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a729d417aefd9dfb81c250627142f3439fb2e2dc6663bc62c6d88725015f449`  
		Last Modified: Thu, 24 Oct 2024 01:56:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:373b14d6a3f03dffba4586f37444a2208ad48c8a6c98801e61e85e8c7e8fd62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bad4f185d7411a62ff0bd2ae905eb320678d37c8c209e30137149c891139c4`

```dockerfile
```

-	Layers:
	-	`sha256:da846d32d159d250e6a2e4f460357caf34412a91b41e60d711001dd55fc2b60c`  
		Last Modified: Thu, 24 Oct 2024 01:56:55 GMT  
		Size: 7.2 MB (7220847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c11c0ebd5e6a5b7112d041f845a13316b826649f3b148d6d3cca78b91d295b7`  
		Last Modified: Thu, 24 Oct 2024 01:56:54 GMT  
		Size: 15.6 KB (15643 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a856eeb71d5651a80d0fb29c0aa680a17dc13903522530cdc62263ec197dded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288789344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d089e77e15e2c5e5433a547146982bb8973f73ebcf91d365e107faf304640f`
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
	-	`sha256:9f985f8cdc870263d7c9c2eb30e17d5f7eccc559c94fa90f2ce64fc3cced1912`  
		Last Modified: Thu, 24 Oct 2024 09:38:21 GMT  
		Size: 163.3 MB (163281826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73d45682e07c937796e42c666fa7c5babf18ba7847eb2ebe29d5660aa01f4ac`  
		Last Modified: Thu, 24 Oct 2024 09:44:32 GMT  
		Size: 71.8 MB (71771585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dcc4d3c30e0858e06e31a63355d8fbac0a5816f27b784185b7b2d671fb8911`  
		Last Modified: Thu, 24 Oct 2024 09:44:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b7bc2609ceed5246a62a883b6f124c8d7e94027b02951da9220cdb0a5a2014`  
		Last Modified: Thu, 24 Oct 2024 09:44:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d82db14bd2e3cb0285201e679c186abcf9b803a71501f9b6707c08b2eb23a5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e47189526ecaba5ae1fd5962da28b82497c4aa5d77ce37c4802dcf971cca36`

```dockerfile
```

-	Layers:
	-	`sha256:822a11b25406672b5a3512d50858a55a233cefcc955878cf948a63945213807e`  
		Last Modified: Thu, 24 Oct 2024 09:44:30 GMT  
		Size: 7.2 MB (7225328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e22a9bab44a90ee30b654cfce78503a0ca03b7a8b997edabc5665a5c47da9a`  
		Last Modified: Thu, 24 Oct 2024 09:44:29 GMT  
		Size: 15.8 KB (15757 bytes)  
		MIME: application/vnd.in-toto+json
