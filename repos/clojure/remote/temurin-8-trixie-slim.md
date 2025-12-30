## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:2cc7caf95c5389a915f1db8b1489b52e7eb50ceaf806a82a924f9cd0e5951d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4b18ca6f7d0a38867eeea8adf1406cffe7f0bc83e9d440d95cf96eec40cc7f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156501952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c86792b0352fa3d10b5c7424880b12378bb1979a398ca1ce12f8452b340df13`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:53:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:53:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:53:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:53:12 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:53:12 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:53:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:53:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:53:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1ae66f5f06abbea1f94bcbfdc7e4857ce5937cf1690614b05b75a8dc29ebde`  
		Last Modified: Tue, 30 Dec 2025 00:54:01 GMT  
		Size: 54.7 MB (54733370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640346e7fa1cdd6227caf06830e97482a5a4d4f4fbe3fae5d7cbe6cc5b0c121d`  
		Last Modified: Tue, 30 Dec 2025 00:54:02 GMT  
		Size: 72.0 MB (71991406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c13e7bd76a4dd0e9817a2d4e9c40878c37f6042b07ef242bb0b6ceb46b4b284`  
		Last Modified: Tue, 30 Dec 2025 00:53:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20421efa7dc328479b740272abf487b763ed97352a4bf874818d7deb0cfc6ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785e97c3be47464a0ecce682f21fc771bcf152f1541313891fa6f5a3ffeb788d`

```dockerfile
```

-	Layers:
	-	`sha256:2a44cefd31c38a28ee4d291473c0f9fb5f94a352270f8903bf96ea07de52df14`  
		Last Modified: Tue, 30 Dec 2025 04:50:11 GMT  
		Size: 5.4 MB (5377807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e344edec3631e8cc7392c9e714b911acb99722a2ab9bd843b09609526e9505f`  
		Last Modified: Tue, 30 Dec 2025 04:50:17 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee6603eef8f555ba78f21b6ce60023d680a77d4f1061627a86369ba3e249abe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155761152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208586eb4d7a3fdd541e4e291659e4f38875fcc4b7c71394188348c6845f06bf`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:55:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:55:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:55:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:55:42 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:55:42 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:56:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:56:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:56:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe854133b7e4a0904840f857748dd9231b1f117b1ed66957668111845d560dcd`  
		Last Modified: Tue, 30 Dec 2025 00:56:35 GMT  
		Size: 53.8 MB (53815013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f239421015a7b137fd853e50694f1a9f38871ed7380769baaa841dbfe8bdd085`  
		Last Modified: Tue, 30 Dec 2025 00:56:33 GMT  
		Size: 71.8 MB (71806860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d037e74a0a39a6ebadb3496a87e29e7940dad7b08f84cdd1325ed97b62884a7`  
		Last Modified: Tue, 30 Dec 2025 00:56:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a5bd29553be4de93517c111350086ae81b6114145c78c279eadb82d06070e9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bdf96e22d1a59ef3671736368f1e862e450a5d1d761fa6c2b5999cebe388cb`

```dockerfile
```

-	Layers:
	-	`sha256:add76ab99b66ee13fc5191af3547658eb4e2fa67d968252ec1269426ae99bcd3`  
		Last Modified: Tue, 30 Dec 2025 04:50:22 GMT  
		Size: 5.4 MB (5384274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8ab447e315dff5c060b2e705f5d356077376769da791237b5f9b81086eb921`  
		Last Modified: Tue, 30 Dec 2025 04:50:23 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:18f3646a012146e14ca55b07f990077ee1a55c0b92f50f8c2f74fef5dec27221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163159739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d47a8b560cae156a0a03741b158b0166daf7f4c9d2a9ef7c7d8dd2ece73704e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:46:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:46:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:46:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:46:38 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 03:46:39 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:48:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:48:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:48:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9ec5d91b1da27248b6474c55829b4ad5637900f96134ea7cb65096baa6ecbc`  
		Last Modified: Tue, 09 Dec 2025 03:48:24 GMT  
		Size: 52.2 MB (52175138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784452e94d901c952e8cb438b870fb05e7dbd5e497eaeec9ccca57349da1dc31`  
		Last Modified: Thu, 11 Dec 2025 22:49:16 GMT  
		Size: 77.4 MB (77387064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90d9667f29fe0a0243c185bfff2c1e163ea445967e2a9068dc0848539640d3f`  
		Last Modified: Thu, 11 Dec 2025 22:49:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1fe3faf8e2068e088afd10ecb26c30afcb79ba413a30002e79503fc7a9d21733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d949e577decd53cad4847e028c7954eaba8de1911afcee85d6936fefb2df4109`

```dockerfile
```

-	Layers:
	-	`sha256:2ed3adaef2d19bd3eed2e371c16cded07fe0f976d2dd4f76c81c43b186910e25`  
		Last Modified: Fri, 12 Dec 2025 01:48:03 GMT  
		Size: 5.4 MB (5382771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200dc0d21cbdd721d6f331a98a97c7170454a1979a5b4bc7aa7e7fa79f709e1b`  
		Last Modified: Fri, 12 Dec 2025 01:48:04 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
