## `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:921921995c9bd9a4a669b0ce936879b5f79a5dd44fb4fb496df302b616ff64cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:76224fd8b3c4f97dfb4eae08047892ce7d5d65cd855d638426aa2ea233771c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288194912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b26fbf8af5cf3fb3baa933f815f11b1bb8e16bc5d4426c4aac4e2e293e4939`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43171f0fff6d7e05220f57f247b8664bec92091003532f51eec3ac0f95d09a7f`  
		Size: 165.3 MB (165295091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7819d9d6ad050d621d5e365fc1a6b580edad68b079a0bd0b0bfbe76ccfd9bd2d`  
		Last Modified: Tue, 24 Dec 2024 22:39:14 GMT  
		Size: 69.2 MB (69159825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b62a70726a6d22109c85fe4ccbe00522a82be69673dcc1ee248560460653af`  
		Last Modified: Tue, 24 Dec 2024 22:39:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e04045375256adeaabd151d9e8663e7a85e3adde1ca767694364eb83f9f0ae`  
		Last Modified: Tue, 24 Dec 2024 22:39:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fa1a22771799b244443d26a071c7d53003cd0976145e92054b1a3dba3de0fada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdb81edc812c7450b4738b881d2a534c52035e125a414cbfec135fa0049dcae`

```dockerfile
```

-	Layers:
	-	`sha256:c28f4009255e5e613632d296a8f85a52e5688f8d9f4c33bbce54b25d1566194f`  
		Last Modified: Tue, 24 Dec 2024 22:39:12 GMT  
		Size: 7.2 MB (7209500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7091eb782da275644ea9fd1128964350060f519599d48ab72b034ccce7cc6b75`  
		Last Modified: Tue, 24 Dec 2024 22:39:12 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aa97a7e816a07cc80cfe67ad856fb66e1c48ad9c404d4fdde934f30eea5fcc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284814332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bb49171d39cddf713503eab03e866ce2560f064f0a4f444aa7b1a7545a53c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6695db2a9af9c621e2afd751a22f972795b62d6695e9f4d372982636e107ce9`  
		Last Modified: Wed, 25 Dec 2024 07:38:55 GMT  
		Size: 163.3 MB (163281797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d588326635de5735f25ba3e4bd1c362a537d18c406d156470851a243421ab01`  
		Last Modified: Wed, 25 Dec 2024 07:42:06 GMT  
		Size: 69.3 MB (69285798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534e5d76eac561e7b607a61d7430c9f32dc2e7c878eb7e5e5db8496fc5aa197f`  
		Last Modified: Wed, 25 Dec 2024 07:42:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebebd1c0d2ce3c4335b106d0636d51b5a4ea94aba0c6fdff2d2d74a2a77fd077`  
		Last Modified: Wed, 25 Dec 2024 07:42:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:78fe273dfaf33e789e6706af0a0ee8e3db36358daad58349229804b955853875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70851bd9ff73e21d401c42826ca0a6f339319cbe3e5d4d8cae1ce180e8289642`

```dockerfile
```

-	Layers:
	-	`sha256:205b5820aa9271a6cfc0b4aaeb5ca197520196d4325e252d280ef503ac93de27`  
		Last Modified: Wed, 25 Dec 2024 07:42:04 GMT  
		Size: 7.2 MB (7213978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c251eb4cdbb66475d5ea946abcbd044655257cadc45cda2da22b654033de1c43`  
		Last Modified: Wed, 25 Dec 2024 07:42:04 GMT  
		Size: 15.9 KB (15937 bytes)  
		MIME: application/vnd.in-toto+json
