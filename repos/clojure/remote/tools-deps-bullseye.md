## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:65c3619cfbdef2a1972a8cea77911ac1b8f4af4b3d633f1c9ebc7442e213bc96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0096dc2b1d109fe7f755b8d4b42ef0a9e45939a152fcbaa8d43cd98a20c26cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280515830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9624dd55593ac46284e52fb41d409c35c407905bd52db89883f626378ebfd4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51a9ff09a2ef9e5643dbaca822663b8de4e68073cc196a9cc5d4da358d08179`  
		Last Modified: Tue, 25 Feb 2025 02:34:42 GMT  
		Size: 157.6 MB (157585922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b47683951ae213710b3c81073a98d4114ab195b4746ec1be43e2ee2d62270d2`  
		Last Modified: Tue, 25 Feb 2025 02:34:44 GMT  
		Size: 69.2 MB (69187466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff286a2d8fe8d45b5514c41ed1c6196e3018b81d84ee03b94f94b57391fd6b9a`  
		Last Modified: Tue, 25 Feb 2025 02:34:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55ec08ccb180b51970103dd56f22d17fbf2c6170f2c3c336f1e1a3d08f301e8`  
		Last Modified: Tue, 25 Feb 2025 02:34:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bfd949374a42c63364a79a57a75494ab9e2704a09584fc7781c00083d3df9263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d3affd8826da64f5f5fe1d58439941648b2c98e9ead6ff89956b2527c21a28`

```dockerfile
```

-	Layers:
	-	`sha256:838828e55c5ad944dd7412bdcad5399c4c45d1dc28f25dbd197ef12cd8570b1a`  
		Last Modified: Tue, 25 Feb 2025 02:34:40 GMT  
		Size: 7.2 MB (7208333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beb88540352f64f33753b659ebeb2e396fd8ae698959da2238b21cbf58b99b58`  
		Last Modified: Tue, 25 Feb 2025 02:34:40 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2725bf7c3ba17a8c97b62b3c5fb34ee5e683627f23e2e57da9cdf7ea73b1c4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277418250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e447bf71f0f6cebac484f87b84f9bec13d036718636430dd7b0c3e7f4663dafa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1679db646a48b98433b52ed3f649e6c9776b4ec08a5a4726e08b07c77e834b9`  
		Last Modified: Tue, 25 Feb 2025 11:10:30 GMT  
		Size: 155.9 MB (155859249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02614d28f800592e9f91511830d210d316c57f7181dff91410c1c870b1e7492`  
		Last Modified: Tue, 25 Feb 2025 11:13:32 GMT  
		Size: 69.3 MB (69309313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c6d1e91e1f3d2641e15ab82556910dcf10adb48aea52f1dd806a2c305bd0fc`  
		Last Modified: Tue, 25 Feb 2025 11:13:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bba68e03ead9ad6f9ed72c87831445fd70c1740b53421dad92897885a0cf50`  
		Last Modified: Tue, 25 Feb 2025 11:13:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:099f9302bdcf7106ec01fd46c139b1b6e83a5e3a2f073e221cb63ef1f85d8402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfa5d86952fe17c0ffa41db16bf6eac017c8b31435a85bd2b0281176997391b`

```dockerfile
```

-	Layers:
	-	`sha256:a6d3bd82cfeb5cae52bcc9ca5034aceaf894dc92a54e649eea12e00f5bf35daa`  
		Last Modified: Tue, 25 Feb 2025 11:13:29 GMT  
		Size: 7.2 MB (7213456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde350dd2a6cac2485305eed5a417ce3b42e1a88130a96a7ffde68c566bb6bc1`  
		Last Modified: Tue, 25 Feb 2025 11:13:29 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
