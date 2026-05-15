## `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye-slim`

```console
$ docker pull clojure@sha256:643bcdb4932af390e830a954c772679d8a9206f3db9ce7c29c6d6d8dae857077
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:031d5ab4fcbdad78464f7b74d8abd3aa4b2e16b0e35c9312c346ca0b61715c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235355014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b8420393baa1e10eb866d44e811ce6fb9e03f74cc68facdeb1de1976608fc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:14:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:40 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:14:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:14:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af443c2fe4190892d80baada67a27ca0cf98565f1d7a13c7a9b65762e37f7e`  
		Last Modified: Fri, 15 May 2026 20:15:15 GMT  
		Size: 145.9 MB (145905467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7f75844e0d6d2a081f728aaf97bfa1528e751ff9bd080245261d5582aa708e`  
		Last Modified: Fri, 15 May 2026 20:15:18 GMT  
		Size: 59.2 MB (59190545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b874f7dcabbc9b7cdf657536691c4186565230ac4b790354cc08f4e4aa01057`  
		Last Modified: Fri, 15 May 2026 20:15:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4351a8b9e2ea0dc0e2371df0f75872df0956e3ef858f48844f279f25ea696e75`  
		Last Modified: Fri, 15 May 2026 20:15:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfc007ac68f369a5dda5e40c07b059b5d09e372a16348ea832e28893f288e45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb3bbf0774bdf373b5769e43e3220ed8fd667eca1dcfc45bb932b70b9f2fe0d`

```dockerfile
```

-	Layers:
	-	`sha256:8cd9e84ec96139015e0f23aaf5f24f486c8ea78b20b1506be245aa7660f78026`  
		Last Modified: Fri, 15 May 2026 20:15:11 GMT  
		Size: 5.3 MB (5320678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a2d6afba2e26e38f9f8cfc5849aa794a93cfbca3bbe6911375004bbe11a286f`  
		Last Modified: Fri, 15 May 2026 20:15:11 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ec00db151abaa977e5a9f33400feec6843158c1a4ea38deb7fdc677dd3cf22e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232828037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607255ce1d507fb06ffb5bff850ac643d889e43d9ad1f4779e09eede1e059b1f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:32 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:14:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:14:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75559c4ff0dff17b64d47a980d4222d11b36a7f07908bdeec57751e1301ad10`  
		Last Modified: Fri, 15 May 2026 20:15:10 GMT  
		Size: 144.7 MB (144724337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4549c958f202736f6d30932881b702de576ba4dd84f20ecb8b4701c5092120c3`  
		Last Modified: Fri, 15 May 2026 20:15:07 GMT  
		Size: 59.4 MB (59360064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb45f3dc613c7f0ecde06f6898174e144343c1a5395adc0a8230959e294ce5b`  
		Last Modified: Fri, 15 May 2026 20:15:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054028c5329323de8ae31acb40044fbb30af1f1015a00cf2ad2b4a54bfc34be8`  
		Last Modified: Fri, 15 May 2026 20:15:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff42ac701ea50ddcfe518215d169b7bec5680ea25166a872a739b95746e9399c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441b540860bb835dd34add2772625e2de3b2954913c36b19436860025ce447b5`

```dockerfile
```

-	Layers:
	-	`sha256:d0f723897bdf76199662422594a1396ad68704ff74e1c6181a99b1f65be47a15`  
		Last Modified: Fri, 15 May 2026 20:15:04 GMT  
		Size: 5.3 MB (5326410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b84ed4753724832b264c1cea92bd4a76e68c5197fa68f8540d473a98da9f22a1`  
		Last Modified: Fri, 15 May 2026 20:15:04 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
