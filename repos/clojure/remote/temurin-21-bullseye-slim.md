## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:db6efcac4338fbe6e145ad089d2270d699223da294d80820ba66a328d0e015ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:955776a6296ab93bbb19ab590a4a52c3fda685cdbdcf109c17fec65369a5896e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246885788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faac1d2ed2978962624328c382720d535d13189f10687ecd5b11548d03c345d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e982ca09eef8b3f27f6333071135d9d3f3979b940e371327568b5100f4325e0`  
		Last Modified: Wed, 23 Apr 2025 17:16:45 GMT  
		Size: 157.6 MB (157634511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e5a329b90438e21769458fd2f96b402e31ceaff47a501137b5543e5e4eb0e3`  
		Last Modified: Wed, 23 Apr 2025 17:16:43 GMT  
		Size: 59.0 MB (58992812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aced7f2573e9c5e95d844065733a8528ccdc6d16b6d01a6fd8e49fa9f16030`  
		Last Modified: Wed, 23 Apr 2025 17:16:41 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b96e690ef13a68a07da5417c521190a11345ab11ca7713d5ef8bcbf123ed7`  
		Last Modified: Wed, 23 Apr 2025 17:16:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b61586af6856d128973c8c7b6d6d567c0e2a48c6ba7b881154ed4c06eace45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7d682cb341e55c3391a7eb347f5482e252e9a79fefb82660c650b66ebbcc13`

```dockerfile
```

-	Layers:
	-	`sha256:de9404f78fd36e911b64fd82132338464762f57ae0a4a41abf99e58edd21d7d6`  
		Last Modified: Wed, 23 Apr 2025 17:16:42 GMT  
		Size: 5.1 MB (5122811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2362c33f9e31fe39a3bc5e5eab90be244bd55697a00b740c0c3da536cb92550b`  
		Last Modified: Wed, 23 Apr 2025 17:16:41 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:94f9543cb3bc9f7a5674768181cd6327a25fc18ff6e995dcff468dfab5132010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243737125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6d40abf3518dfc3adc8f46b65ad7f6945ea32da9779c171feb4b06924e9cc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3092970dfc6ff6b5baaf45f0ff4fdbdd2c181b6e2eb0565cc8b269a2c08eb8`  
		Last Modified: Wed, 09 Apr 2025 15:16:05 GMT  
		Size: 155.9 MB (155859263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f381ab644954eebca77f35b2c1f17f2ea172c38d3e8551bf46cca46629f1ea`  
		Last Modified: Wed, 09 Apr 2025 17:45:18 GMT  
		Size: 59.1 MB (59127322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584ffb57c8e7ece5c9ea51fffd522f3d168283bcfabdbbe26c20336f4120f8ba`  
		Last Modified: Wed, 09 Apr 2025 17:45:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afae8e48754a1cddb4bb4ed7c4cf1a153ac5b2937e959587116ef752a6166c41`  
		Last Modified: Wed, 09 Apr 2025 17:45:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3738da240289d95b40e56859cc3ebfeb0116fd6709eb574a6892d23921b6f74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100ee9b1f6b6320441d4773f5df7103387a14d10548966743006883237819ba7`

```dockerfile
```

-	Layers:
	-	`sha256:44786b2d0fb260f8d5b86d6e6742a2c63a5d7b1dfdee6a8f4a08837d10b866fa`  
		Last Modified: Wed, 09 Apr 2025 17:45:15 GMT  
		Size: 5.1 MB (5128567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12efbaac369b49f21f5dd37c92b2bac13f6dd5b25579fb2f64f73d4eb5061170`  
		Last Modified: Wed, 09 Apr 2025 17:45:15 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
