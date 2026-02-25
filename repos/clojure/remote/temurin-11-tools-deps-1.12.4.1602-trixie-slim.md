## `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:d7512c8b164b6516f3e9d466aa9cdc24616710ac89d7f9dfc95b02be05beb4ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0dda55e26a39b87a90deb1886d04b7b982ee7658e2311457661b292f9196c475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247580208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e3f1da39a363f2352e6b612a92fe4f499d22dd14d1d3e93e6609c1b493a9d4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:54:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:54:37 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:54:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:54:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae567c9ad885cb8c13393c568a4bc37d5452a750d8ae7022230419e78da0668`  
		Last Modified: Tue, 24 Feb 2026 19:55:18 GMT  
		Size: 145.8 MB (145806749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb9d796ada83e7a4bbe12a71efba33cb76d97f35da2f25916dfaa37cec824b0`  
		Last Modified: Tue, 24 Feb 2026 19:55:16 GMT  
		Size: 72.0 MB (71994184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0045e207aebe77015b7757c33e6044bfbdc65f804d8d526c3a7710c3c81b86bb`  
		Last Modified: Tue, 24 Feb 2026 19:55:13 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a366e9465771a55a995443a7bbdf3e4fa66021c62b31e6b78dc1450c1691332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9809fb45d2fa46e2ba279561501d9a8e510c5eed30849e9604168b77190919c3`

```dockerfile
```

-	Layers:
	-	`sha256:159e9ed72af9b9e4d17e6bb1601d3c74c92bc3ff55301db8315e68248cd87a8d`  
		Last Modified: Tue, 24 Feb 2026 19:55:14 GMT  
		Size: 5.3 MB (5277692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01ff53f0f65bf2a7c8ccd6e46d7d1a02ec2c20129b69592906c7c8a1ea2bcc37`  
		Last Modified: Tue, 24 Feb 2026 19:55:13 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b492e699d6190771b7854aa233ef1af4bf72af6887f7c8e36e96f24944e174c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244450242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356bc63a5e72bf4a1480a66b0aeddd042dc861ceba780b5fb8eafac353804548`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:05:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:05:04 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5832d85a6c75b7379d03869322dff4323c39ae58f9e9d4d4344f20cd8de75c3`  
		Last Modified: Tue, 24 Feb 2026 20:05:46 GMT  
		Size: 142.5 MB (142501412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f29df623a2c45365fed7caa0c1c391a4df059b856cd43da52580eab3c60a36`  
		Last Modified: Tue, 24 Feb 2026 20:05:45 GMT  
		Size: 71.8 MB (71808088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11fb6add92ad2897e529c7bfb6783beadeeca1faba74153928dbd89a6510bf`  
		Last Modified: Tue, 24 Feb 2026 20:05:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01d81e28bdf3d04ffc955d26cceefad0b167a9476855235aa8268b40d9f32b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5298440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700e409808ee81b1ca1dd4a49d03539a9d6fe60112877acec4bc7b17545e0936`

```dockerfile
```

-	Layers:
	-	`sha256:7a9e6aa65465a008b6c51c01c3e7c81ab428df5adabaaf3d25a9cc39a8195b17`  
		Last Modified: Tue, 24 Feb 2026 20:05:41 GMT  
		Size: 5.3 MB (5284079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aff50fcc5c73a652f3be2087f74f2d82bcf5cf08751d2271bb725a63c58bb63`  
		Last Modified: Tue, 24 Feb 2026 20:05:41 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ae90b5db6ecdde65b0da3e9885b8e06ea0535d6fec968520d4824a09ee95e66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244005961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9e4ff58d5751c84501d9097fd0993278e7559f19201eb8aea18831082b87de`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:51:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:51:10 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:56:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 01:56:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 01:56:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21426e09421bed3f9e9b43d31a1a5b3e053a0afe29ad9d5a421aeefd9dec6ac2`  
		Last Modified: Wed, 25 Feb 2026 01:52:55 GMT  
		Size: 133.0 MB (132997815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdfef29c69ebcf16aed0391b2f0191a41c3781dabe53411f7bfc68e3db1ac74`  
		Last Modified: Wed, 25 Feb 2026 01:57:10 GMT  
		Size: 77.4 MB (77407285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0c5b0af423e7146f5a1cbf19e7d6771ee3dee67bf9dda5dc7d099b46975463`  
		Last Modified: Wed, 25 Feb 2026 01:57:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4cf8e0647f4ad490920db45615e73e72a86a4357b9aa2f29da91ac87f30a098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5295739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4ea4b2d5dbc0d5e4c5ddaa26e9e1d82bfdacb93dc04cd27df174216c408f78`

```dockerfile
```

-	Layers:
	-	`sha256:75810e8b911b04338a01b7c25a9748bb2bb9b3852b6b6699ba9b74d2a8ee2410`  
		Last Modified: Wed, 25 Feb 2026 01:57:08 GMT  
		Size: 5.3 MB (5281448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46a7f83a759c4971e11a3e6891a23b1bfdd10869a665448bebd24c2cf9009d5c`  
		Last Modified: Wed, 25 Feb 2026 01:57:07 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a3b7c3dcfcbe377b17a9364698e1aa4cc210963c1b5f55fecb62d3703b56fae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229360157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1587837f6c8d24f7e67c9ec72c48d45e265161fa0d659f3505469efa7d403a15`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:13:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:13:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:13:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:13:08 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:13:08 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:15:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:15:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:15:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773136b18489da474dab6c335e3fb6d61644f01d540ea474ac9f79a4dfb431fe`  
		Last Modified: Tue, 24 Feb 2026 23:14:24 GMT  
		Size: 126.6 MB (126561996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252edb226682743c07ddab4df458b3129464d0f15f97806791addb719ac227e3`  
		Last Modified: Tue, 24 Feb 2026 23:16:25 GMT  
		Size: 73.0 MB (72959335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8815333d123b112b5b4de7c6bc004229a464907be6eda1ef55cd8d015e1ded`  
		Last Modified: Tue, 24 Feb 2026 23:16:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b98c6296af6719f5a1110f3e5f9d1755ee8d1d3a6f9fa3f769e096bee7e798c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6273339c1f6fd61046b6dd5799859bccfc41977ee0ffa40c1194ff4112b920d`

```dockerfile
```

-	Layers:
	-	`sha256:00c58ff72bf181d9b9d9347e4ddb1bdd9ad09fdc5ebc6be73f4c46625cf5edb5`  
		Last Modified: Tue, 24 Feb 2026 23:16:23 GMT  
		Size: 5.3 MB (5273620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43d3037df854094fd318e8b5462d821a7fd68fe9c8e273d2beda267caa9f6053`  
		Last Modified: Tue, 24 Feb 2026 23:16:23 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
