## `clojure:temurin-25-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:437cf397d38fb9fae5310c29137aa496d61d8930a0eff63652876c8b459a77e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c68cfb690d80200c2aca49fae4d86035cad190a640f8ed7c524ce0c9dc85d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181441551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2640f74a0fde3d3edfdd1d98caa56511ad8ce7ccdba1024ace44d66830ea1e55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:06:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:42 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d6808a7b2c79b683807ccc64102eb6ac5ae8a43a44f939b71e5b06b933a4e7`  
		Last Modified: Wed, 28 Jan 2026 18:07:14 GMT  
		Size: 92.0 MB (92045330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d10e444b7fffe49b97762bf80a3f84d74ccfddc4426df5b747e41ebe219513`  
		Last Modified: Wed, 28 Jan 2026 18:07:15 GMT  
		Size: 59.1 MB (59136682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6dc9a42c656120c2d616b327085f409cb1b37dac9cbe71b880b2e54b264089`  
		Last Modified: Wed, 28 Jan 2026 18:07:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71dd5145156fd3eb1d4a4fe33104ea2f5b3bcc8ff516b0ef3351d0ae915a074`  
		Last Modified: Wed, 28 Jan 2026 18:07:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f936ae7a7e1253cf3034098fb34a7b84366038dedf0dfd79c8db923299fc0322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5fe9c76d74718246723be745cdedec24acb447e36caff7b955117801746591`

```dockerfile
```

-	Layers:
	-	`sha256:49f9db458e70769506752ab7a5f8c304ef43b6d9f2c9e214f32253a1b0daa01a`  
		Last Modified: Wed, 28 Jan 2026 18:07:13 GMT  
		Size: 5.3 MB (5260226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26014e69e3ed0e4c1833c0a24198312d8b9b30cc6f05ac3b9e8bd4026ce079e3`  
		Last Modified: Wed, 28 Jan 2026 18:07:12 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f408e3e6e069a99895aa330d4777ae36e64a66a7a1baa834a262b619694b8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179090138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8955c26e184e57a8b836bd2ff4758182498b5c035b41f34328244a42a4561`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:06:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:43 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cfc08f2b59c0e6c654e0e1aa09038fe7f300ebcc162c3bc588a67942ba352f`  
		Last Modified: Wed, 28 Jan 2026 18:07:18 GMT  
		Size: 91.1 MB (91052475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec30c440e253e0247ac667e029d0f766f76eed6b2023a521635e683c7e69035`  
		Last Modified: Wed, 28 Jan 2026 18:07:17 GMT  
		Size: 59.3 MB (59288103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbb740314e2e4c00147ea780fef32a631df60f5f54536c055f78ff742959253`  
		Last Modified: Wed, 28 Jan 2026 18:07:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338f1ac47e3e4bff4bccf20304d11753ed024410c90f9a330196450a97cfd753`  
		Last Modified: Wed, 28 Jan 2026 18:07:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e8b4b6c05fdfc29db66733662d1160cba51fcee4cb975005b507bf447956a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484f40cf6a15f2ac9c52df7037444aa93b5a96b7026c84d2f6bdadf691551ba8`

```dockerfile
```

-	Layers:
	-	`sha256:99a29df85cffd61be09b0d5a641750b1e19f84d40b47fd4445544e8ff121c8a5`  
		Last Modified: Wed, 28 Jan 2026 18:07:14 GMT  
		Size: 5.3 MB (5265979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26a77e7b010a5615d01c384a8df5349a4bdc8d8d70e055dcbf042ac2bba05e5`  
		Last Modified: Wed, 28 Jan 2026 18:07:14 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
