## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:8bdd03b1aca47465c2ea210fbecb75c8be9c296454a5b2930b4cbef2fa575868
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4e1a5d012f7aa65e29cd2bd0aa223ff299f61d1d5de355dfea749ff1c1e28780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235536441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c8e1b522ee68c8ac5c48ab3648c0654328f616b6332bedbe79c6b2d5a3d0e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ad995427cdea099cfee6bb165741e1e35b437f97959525b6b939b6a4ae4df5`  
		Last Modified: Sat, 19 Oct 2024 02:59:07 GMT  
		Size: 145.2 MB (145166530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e433b7105f5df4859cccecaae8d4bbfe332690e2fbc578dea849b8849529ab2`  
		Last Modified: Sat, 19 Oct 2024 02:59:05 GMT  
		Size: 58.9 MB (58940072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59243820d5753c264d1351f781518ca9ac3ec500180ffe8d3488cdbd8cb6a5c1`  
		Last Modified: Sat, 19 Oct 2024 02:59:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e96e63ff3e5fe31131da86340ff37583dbd0f50efa0852dc30c2737f6ce60d`  
		Last Modified: Sat, 19 Oct 2024 02:59:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a70913f10c50779913945855efb61135543517220bc46cd89c8927e57b834c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aed94e246e3d07abdd711cd0b279b70b60cde9cafc7b789634383c33e03b3f`

```dockerfile
```

-	Layers:
	-	`sha256:cdff3dd8552a2d1c33b250f74f583ab1e2a3563c49f9da80c6a36f91ba50c829`  
		Last Modified: Sat, 19 Oct 2024 02:59:04 GMT  
		Size: 5.1 MB (5124680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48d4f9942ce50bf8a4a399cc174d30d594161a66ead944cc08621bd47721bed`  
		Last Modified: Sat, 19 Oct 2024 02:59:04 GMT  
		Size: 15.7 KB (15719 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3057bf59ad841303e095a7cea9a1b37f295e15d704c4c5322d5773a8ab42586f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233109096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678d6a75582775df45caca752ca9587cf4d6fb16935af070c055e7797eb0a1a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60746b2d48dfb19e043609b9b09417ae53dbcb13af929a26fa77a66ad395af56`  
		Last Modified: Sat, 19 Oct 2024 08:48:40 GMT  
		Size: 144.0 MB (143959478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6b3707f40fa3f13507c9fcf22dbc220a05a4b9ba0c11a7d3890db897f233f9`  
		Last Modified: Sat, 19 Oct 2024 12:08:57 GMT  
		Size: 59.1 MB (59072819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eac767e0b14747926380cd33b795b2bbe5d074d5da95a8fcfe6ce83e8b7358`  
		Last Modified: Sat, 19 Oct 2024 12:08:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c89a593d2586a9cbe578476aa584a54e6d14228b61cbaa340e5efc299d09ae`  
		Last Modified: Sat, 19 Oct 2024 12:08:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eed7ed0cfa86703ffa786b3c44f65b0f91b085b785940a91f7e9e950f4518a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b09b321b4c52bb765294dc39c291af31c6b2f4241a73c79c8de1e554b97ea89`

```dockerfile
```

-	Layers:
	-	`sha256:5b91a37a6a14357e3f45f4b107851c18f53dfb09db862a1fa68ed355ccd53a2c`  
		Last Modified: Sat, 19 Oct 2024 12:08:56 GMT  
		Size: 5.1 MB (5130417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5241fae364faea996811832af07be5daa68adf71f7b7e2873f801928cc6eec`  
		Last Modified: Sat, 19 Oct 2024 12:08:55 GMT  
		Size: 15.8 KB (15831 bytes)  
		MIME: application/vnd.in-toto+json
