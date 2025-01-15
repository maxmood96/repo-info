## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:db85f11d3d7cf70aa1761b8704f7bb823c02f51d6407207541675bb9dc01ea62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7ae9609192f35ef6f0aad2622c5d7e1b520c8d9a4092e718e9ddb2e37301070b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280487464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bba63d2b2975898a6c922c426de3c2cfbfbca64c3102c50d39858d00cc176e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 20:33:13 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31edb1f5ad00b397fc6a45e6c1402178084dcfb434647e7ff40ee9a1368388b`  
		Last Modified: Tue, 14 Jan 2025 02:44:48 GMT  
		Size: 157.6 MB (157568721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaaa2220d06fc504927c33c65e6a615bffdc183247725902801b26346ae2077`  
		Last Modified: Tue, 14 Jan 2025 23:14:55 GMT  
		Size: 69.2 MB (69178539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c2e24536d977e6d94ae80a5b73d3c61a0d44c1a8797911ad8c778bc4a22424`  
		Last Modified: Tue, 14 Jan 2025 02:44:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8ba52f264a63e5567dca715d72313793ec0e969b7cb88672e86fc647ba7c64`  
		Last Modified: Tue, 14 Jan 2025 02:44:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f160f9165e8cbd20365e895f4deb62d0d81346599818ed904c4380584e0ff190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281046e5b35573b46ac81fca0d7fe40bc4c4b99b416d1156e84c99b9f10293a6`

```dockerfile
```

-	Layers:
	-	`sha256:e4324fa95d6f63ae2a8b749d83e1dfe5b4b96a69a3993f68e4b6121d0620c02a`  
		Last Modified: Tue, 14 Jan 2025 02:44:46 GMT  
		Size: 7.2 MB (7208335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52eec069903c7e4cde11a7488c652b7f03dd264afadc12646944b1f4b226e31`  
		Last Modified: Tue, 14 Jan 2025 02:44:45 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b25f48ac4606f667cb351174d18a7ce91bfa81d7d609d198c5e792ecd4b565f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277344924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daab9e6fa2fcecb964a2b231e0749f22b866d3607eeb810237748cca0c02321c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 20:36:01 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbaed61333d448587c75d37b7e4bbd48824a358426cc2231c04825daf1e805c`  
		Last Modified: Tue, 14 Jan 2025 12:34:46 GMT  
		Size: 155.8 MB (155793168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25093e468939f2f4ae56587f51d23f632dcba4e17b738fde5b0c90681b66bf58`  
		Last Modified: Tue, 14 Jan 2025 12:37:09 GMT  
		Size: 69.3 MB (69304659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd6260537e9d38fce5bc52866633755b45a316c9e50b9893ec79386b1102e39`  
		Last Modified: Wed, 15 Jan 2025 00:27:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd740b62c98fcf12c71ea090c70b60600dd8435c6dcc962dd34b90523f32b92`  
		Last Modified: Wed, 15 Jan 2025 01:14:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:30868e467b0d89507fd3e62afaaf3f689b4fc06a7cc76f7214a17d661ed8cd78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b5c70aa71160967d4fb3a739c2abafdb485cbf3044000e236583632ad8ae6a`

```dockerfile
```

-	Layers:
	-	`sha256:a2675d8d894a88d108d1d59cb6636e810aed74a0bc466b8a6e85971d84701cb3`  
		Last Modified: Tue, 14 Jan 2025 12:37:08 GMT  
		Size: 7.2 MB (7213458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949295a56189a3cf4f36dc1ddc10b3df33a753d02eb16823cb0902ab4be535f3`  
		Last Modified: Tue, 14 Jan 2025 12:37:07 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
