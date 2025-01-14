## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:6b874c6f2eef0d405aad562c449022d20b2e9b952fe619747ac9f65b85ba55da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

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
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
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
		Last Modified: Tue, 14 Jan 2025 02:44:47 GMT  
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

### `clojure:tools-deps-bullseye` - unknown; unknown

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

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c0f5443d958def930c0458bf472b257ad344a023aa7ccb5ac4e2149a50740442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277344229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9d76f025467c822675f131d97052c69dde6a31534fe2e8a48f073c9d93d5e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694535f4ad58a5e07a98ea1c2208c2a6006b008b6802972d46ab6cf2062885ad`  
		Last Modified: Wed, 25 Dec 2024 07:32:15 GMT  
		Size: 155.8 MB (155793090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b25f2de12917a0c291287c2e8e1399084c83070a19662f813ecdf2b52d5829`  
		Last Modified: Tue, 07 Jan 2025 03:32:58 GMT  
		Size: 69.3 MB (69304405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55563c90b9310c77534f3f7b5a9ffe22ec3c282404050e531c312d3dd3895ccf`  
		Last Modified: Tue, 07 Jan 2025 03:32:56 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f046257ba2b51ff7612cd2d9407cd02adbf25f53b5c39047eab3fbd5ed857613`  
		Last Modified: Tue, 07 Jan 2025 03:32:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7cdf9ac374e78de0d73c9d2f90ac3fb6216819ba9b4b0216ee011aca4ea08db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3076fb3d2d2cfc2ed214752ea211d220726b94f3a9fbdf42a24b0f7011a5b7`

```dockerfile
```

-	Layers:
	-	`sha256:40ecd507b10cbd41ec3eac82ceead04c09dec26f05be607d468a24d2a24cd865`  
		Last Modified: Tue, 07 Jan 2025 03:32:56 GMT  
		Size: 7.2 MB (7213458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c3ab72ae8bf7137819d80d49672fe9813abfdcfd712a2c709303e1f304bb1d`  
		Last Modified: Tue, 07 Jan 2025 03:32:56 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
