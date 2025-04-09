## `clojure:temurin-24-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:7b9a99f3b5d3fb82097f41cd284023174cc92162062767010ed72bb0b709c89c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:48e58881bba10f0f41490dad77e51746a0860b1457241932d2cfc66bb74df6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219434903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e521fd926e94c7dd252c62949dfc4b7dfbbe858ca31249d5a3650c4df9ce21dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fc9975e7fad3704a55fdf6228e858326023062a058bb7a21c728ea0a2963ce`  
		Last Modified: Wed, 09 Apr 2025 02:19:34 GMT  
		Size: 89.9 MB (89949048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f792f6f78ef80cade9bb1d3200f2e8c38625a83c1df7ee21f410aa9d239c59`  
		Last Modified: Wed, 09 Apr 2025 02:19:40 GMT  
		Size: 81.0 MB (80994272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce02f9a39dc3c6a67f21e0efd73a16e0702a3cab0df7a694019891008800597`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155fddfee57acf1316d5468c7bd36c79ab8808b932992d3a68d44ed9a8e48bff`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e99268cff7a0cd3b7d45b81f3db761c68bc6c8aff8c689d1a0d49178eb16cadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7140289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f8b3c14a9fb37f0869d27e55dc149b77d967e0b84644cde59394e38f3d8b20`

```dockerfile
```

-	Layers:
	-	`sha256:81a411852027d3c1ad613579245319bab6ec174daeaae66b326e65bfec98127e`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 7.1 MB (7123792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0827cfe4b60a8b94e79915e2d913191541976b332044be00849b5e7ed6c01d82`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:074f3496836ec44b49c5264d4f32c13e25637955e723c45c211a61d6416ff6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218263727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd367bb511a2f8cc199d08c0f73cca414ca9bf60f13b79072f19d4cd95afd63e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056da6c0260d4ec3328806ef52e521e6ccd120e28592a75f2d7011ea55faf71b`  
		Last Modified: Tue, 08 Apr 2025 11:37:08 GMT  
		Size: 89.1 MB (89092720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19585910ed355a32971353e47f4d6bc79dfe0b5fc68140aa4efc7f7d5530f5c1`  
		Last Modified: Tue, 08 Apr 2025 11:40:20 GMT  
		Size: 80.8 MB (80842494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e19d689e3d61007a90ffdb9fc99cb9ab51caccc8ba773054b5ff57d369538b`  
		Last Modified: Tue, 08 Apr 2025 11:40:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ba507ef3b55ae1eb7b9f2a9bd8b02440b0e9aa581ceb90ad04b3f87281f8cd`  
		Last Modified: Tue, 08 Apr 2025 11:40:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:957f7630fb14f806990ecaba115406fa3b65f875cf6a01f730aadc6b09051aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7146216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe3cedd29e0dc41fa4c4cf66e4ce14d3d1474f0ed3af7cfa1db091fe12dd7e6`

```dockerfile
```

-	Layers:
	-	`sha256:e0a9f847c33ea5fc32b0064a525bd8c733d874a44029be239e3ffbe4d4d2b126`  
		Last Modified: Tue, 08 Apr 2025 11:40:18 GMT  
		Size: 7.1 MB (7129576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d2e50a7464cb895ed3df360bcb67496d43243f03f694fdd52491907eb18233`  
		Last Modified: Tue, 08 Apr 2025 11:40:17 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json
