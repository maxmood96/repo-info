## `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:ae268de9da25f3e2075ee452743d9f07122b380f091c0ff3aacf0017a5cf897c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cdb1e93d6535068383fe53aa796321d7c718a8bec9d53141505d3ac82a14f8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144614898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a50bdbc90111bd6b7356a3e8f8148a88940ad29f09ee7f373181c880aefde1c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:15:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:15:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:15:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:15:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:15:00 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:15:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:15:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:15:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3462115a602fcc7a8b0c33af24b95164709ba5794c54ee7f492485d0ef33f02`  
		Last Modified: Fri, 08 May 2026 20:15:31 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdb842ffc6e2ed3c9e6132ba1c1ce2aafb087d879742a4014529e16ef116062`  
		Last Modified: Fri, 08 May 2026 20:15:31 GMT  
		Size: 59.2 MB (59186176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d117c008d181bf43a80b6614acffa4ba74bcd5926d19735a9a8dd699f8f124`  
		Last Modified: Fri, 08 May 2026 20:15:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfbe9994a1dc4b2beecf9d5b30ef474a2de4870a5879c4e8f056a418f5ca9be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b305f8887f359cfcc22b40f50eb859078b2be4d2c37476818ecdf46137422ae`

```dockerfile
```

-	Layers:
	-	`sha256:946f867bc983d93726877ea45f2cff50bda874e2334f6ac5bb5da91e4ff765af`  
		Last Modified: Fri, 08 May 2026 20:15:28 GMT  
		Size: 5.4 MB (5441040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702137c7cc0464a3f828ceb25c282055fd2dcf0e9bafe61b953c0b07158de51d`  
		Last Modified: Fri, 08 May 2026 20:15:28 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7be0e19a2de26df9e6887abc7e9ce1ee76ed08a0f080daff8dcd058ae36eb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142325712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9421fdc476ec162525f57f1cb7b0553482dacdfb1c944698847f46135161d3c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:19:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:19:23 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb565d4f2f9cd77b6629d73f3ab8adae98a76f3031dc5fc8340b601f18178fe8`  
		Last Modified: Fri, 08 May 2026 20:19:54 GMT  
		Size: 54.3 MB (54251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f32cde3d3ba5980c1cea48809fe4fb1457c596a0a676904cbcece7cf447c83`  
		Last Modified: Fri, 08 May 2026 20:19:54 GMT  
		Size: 59.3 MB (59330856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b893342b1d62f241c9d43b7b4658d9932429d5bcbaa800f2d44511ad4d5037`  
		Last Modified: Fri, 08 May 2026 20:19:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e022689dfc1a07e5fdfe64026afbf2334943454dfa5aa4bc1975c4284d3b86a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331b73f62e98be9bc6eb006f5f51defc5fc7cc0501507f5e083414079f5b0035`

```dockerfile
```

-	Layers:
	-	`sha256:21702835f8825f385cd32220678e8dca82599dd179ecbf221caf07eabd0ebd54`  
		Last Modified: Fri, 08 May 2026 20:19:51 GMT  
		Size: 5.4 MB (5447472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99093e5af517a8b67582e71334455ab62a209bf04dc6ba0fcff5a42d7500c61`  
		Last Modified: Fri, 08 May 2026 20:19:51 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
